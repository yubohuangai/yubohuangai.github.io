---
layout: default
title: "Study Note: The StarCraft II Command Stack"
---

<style>
.sc2stack { padding: 0 2.5%; --line:#d8d6d0; --soft:#5c5a55; --tint:#f4f2ee; --accent:#b4690e; --box:#ffffff; }
.sc2stack h1 { font-size: 1.55rem; line-height: 1.3; margin: 0 0 .2rem; }
.sc2stack .meta { font-size: .84rem; color: var(--soft); margin-bottom: 1.6rem; }
.sc2stack .lane { display: grid; grid-template-columns: 1fr 230px; gap: 0 22px; align-items: start; }
.sc2stack .stack { display: flex; flex-direction: column; }
.sc2stack .node { border: 1.5px solid var(--line); background: var(--box); border-radius: 10px; padding: .65rem .9rem; }
.sc2stack .node.human { border-color: var(--accent); }
.sc2stack .node .t { font-weight: 650; font-size: .95rem; }
.sc2stack .node .d { font-size: .8rem; color: var(--soft); margin-top: .15rem; line-height: 1.45; }
.sc2stack .node .cite { font-size: .72rem; color: var(--soft); margin-top: .25rem; }
.sc2stack .node code, .sc2stack .side code { font-family: ui-monospace, Menlo, monospace; font-size: .76rem; background: var(--tint); padding: 0 4px; border-radius: 3px; }
.sc2stack .link { display: grid; grid-template-columns: 26px 1fr; align-items: center; min-height: 2.5rem; padding-left: 1.1rem; }
.sc2stack .link .arrows { color: var(--accent); font-size: 1.05rem; line-height: 1; }
.sc2stack .link .lbl { font-size: .76rem; color: var(--soft); }
.sc2stack pre { background: var(--tint); border: 1px solid var(--line); border-radius: 6px; padding: 10px 12px; font-size: .74rem; overflow-x: auto; margin: .5rem 0 0; }
.sc2stack pre code { background: none; padding: 0; }
.sc2stack .side { border: 1.5px dashed var(--line); border-radius: 10px; padding: .7rem .9rem; margin-top: 3.4rem; }
.sc2stack .side .t { font-weight: 650; font-size: .9rem; }
.sc2stack .side .row { font-size: .78rem; color: var(--soft); margin-top: .5rem; line-height: 1.45; }
.sc2stack .side .row b { color: #1b1b1b; }
.sc2stack .keys { margin-top: 1.6rem; border-top: 1px solid var(--line); padding-top: .8rem; font-size: .78rem; color: var(--soft); display: grid; gap: .3rem; }
.sc2stack .keys b { color: #1b1b1b; }
@media (max-width: 620px) { .sc2stack .lane { grid-template-columns: 1fr; } .sc2stack .side { margin-top: 1rem; } }
</style>

<div class="sc2stack">

<h1>The StarCraft II Command Stack</h1>
<p class="meta">Study note, July 2026. One picture of how a program commands StarCraft II. Solid boxes: the live loop, running only while a match runs. Dashed box: the replay path, working from files on disk. Playback relaunches the engine briefly as a replay device; engine-free decoding launches nothing.</p>

<div class="lane">
  <div class="stack">
    <div class="node human">
      <div class="t">A human, in the game's chat panel</div>
      <div class="d">Types text the ordinary way: Enter, message, Enter. A multiplayer convention as old as online RTS games.<br>
      Example: <code>Enter</code> &rarr; <code>build two more cannons at the natural</code> &rarr; <code>Enter</code></div>
    </div>
    <div class="link"><div class="arrows">&#8645;</div><div class="lbl">chat is an <b>action</b> (outgoing) and part of the <b>observation</b> (incoming): a ready-made two-way text channel</div></div>

    <div class="node">
      <div class="t">StarCraft II engine</div>
      <div class="d">Deterministic simulation in discrete <b>game loops</b> (about 22.4 per real second at ladder speed). Runs <b>headless</b> on Linux, rendering nothing: a pure simulator. Can be advanced one <code>Step</code> at a time.<br>
      Example: <code>Step(count=1)</code> advances the world exactly one loop, then waits.</div>
      <div class="cite">Blizzard Entertainment; AI and replay terms.</div>
    </div>
    <div class="link"><div class="arrows">&#8645;</div><div class="lbl">websocket carrying <b>protobuf</b> messages: typed, versioned request/response for <code>Observation</code>, <code>Action</code>, <code>Step</code>, replay save/load</div></div>

    <div class="node">
      <div class="t">s2client-proto, the official client protocol</div>
      <div class="d">Every capability a player has, defined as schema. Observations arrive as structured data (units, positions, owners, orders, resources), not pixels: no vision model required, no reverse engineering.<br>
      Example, one unit inside an observation:<br>
      <code>{ tag: 4346609665, type: Zealot, owner: 1, pos: (32.5, 20.8), health: 100, orders: [Move &rarr; (56.4, 64.2)] }</code></div>
      <div class="cite">Blizzard, github.com/Blizzard/s2client-proto.</div>
    </div>
    <div class="link"><div class="arrows">&#8645;</div><div class="lbl">Python bindings and convenience surfaces</div></div>

    <div class="node">
      <div class="t">PySC2, the standard client</div>
      <div class="d">Wraps the protocol. The raw interface exposes commands as plain functions over stable unit tags:<br>
      <code>RAW_FUNCTIONS.Move_pt("now", [tags], (x, y))</code> is a right-click, as a function call. The engine does pathing and animation.</div>
      <div class="cite">Vinyals et al., arXiv 2017 (DeepMind and Blizzard).</div>
    </div>
    <div class="link"><div class="arrows">&#8645;</div><div class="lbl">agent code: reads state, decides, issues orders</div></div>

    <div class="node">
      <div class="t">Agent process</div>
      <div class="d">An ordinary Python program. Reads observations from one socket; when it needs language understanding, calls a local model over HTTP like any other service.<br>
      Example request and reply:</div>
      <pre>POST http://127.0.0.1:8001/v1/chat/completions
{ "model": "Qwen/Qwen3-4B-AWQ",
  "messages": [
    {"role": "system", "content": "You answer StarCraft II questions, briefly."},
    {"role": "user",   "content": "Which building enables Stalkers?"} ] }

&rarr; 200 OK  { "choices": [ {"message": {"content": "Cybernetics Core"}} ],
            "usage": {"prompt_tokens": 26, "completion_tokens": 4} }</pre>
    </div>
    <div class="link"><div class="arrows">&#8645;</div><div class="lbl">OpenAI-compatible HTTP endpoint, on localhost</div></div>

    <div class="node">
      <div class="t">vLLM, serving Qwen3-4B (AWQ)</div>
      <div class="d">A 4-billion-parameter model, quantized to roughly 4-bit weights, on <b>one consumer GPU</b>: the whole loop runs on hardware a student can own.</div>
      <div class="cite">vLLM: Kwon et al., SOSP 2023 &middot; Qwen3: Qwen team, 2025 &middot; AWQ: Lin et al., MLSys 2024.</div>
    </div>
  </div>

  <div class="side">
    <div class="t">The replay path (files, not a live match)</div>
    <div class="row"><b>A replay is the input log</b>: every order by every player, timestamped in game loops, plus periodic state snapshots.<br>
    Example, one recorded order: <code>{loop: 2160, player: 1, ability: Move, target: (56.4, 64.2), units: [4346609665]}</code></div>
    <div class="row"><b>Re-simulation:</b> play the log back through the <em>same game build</em> and the deterministic engine reproduces the match, with exact unit positions over time. (Version pinning: keep a museum of binaries.)</div>
    <div class="row"><b>Engine-free:</b> <code>s2protocol</code> (Blizzard) decodes the order stream out of any replay without launching the game.</div>
    <div class="row"><b>Why it matters:</b> public ladder packs hold tens of thousands of anonymized games: recorded human decision-making at scale.</div>
  </div>
</div>

<div class="keys">
  <div><b>Three design gifts the stack gives researchers</b></div>
  <div>1. <b>Official, typed access</b>: no reverse engineering; experiments are reproducible against a schema.</div>
  <div>2. <b>Chat as API</b>: a working language interface inherited from a twenty-year-old game convention.</div>
  <div>3. <b>Determinism plus input logs</b>: the past is replayable, so replays double as ground-truth data.</div>
</div>

<div class="keys">
  <div><b>References</b></div>
  <div>Vinyals et al., <i>StarCraft II: A New Challenge for Reinforcement Learning</i>, arXiv 2017 (DeepMind and Blizzard): the SC2LE environment and PySC2.</div>
  <div>Blizzard, s2client-proto (the client protocol) and s2protocol (the replay decoder), github.com/Blizzard.</div>
  <div>Kwon et al., <i>Efficient Memory Management for LLM Serving with PagedAttention</i>, SOSP 2023: vLLM.</div>
  <div>Qwen team, Qwen3, 2025; Lin et al., AWQ (activation-aware weight quantization), MLSys 2024.</div>
  <div>Blizzard anonymized ladder replay packs and the AI and replay terms: the public replay data this page describes.</div>
</div>

</div>
