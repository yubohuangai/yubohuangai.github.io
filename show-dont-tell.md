---
layout: default
title: "Show, Don't Tell"
---

<style>
.note-body { padding: 0 2.5%; }
.note-body h2 { margin-top: 1.2rem; }
.note-meta { font-size: 0.85rem; color: #111; margin: 0.2rem 0 1.4rem; }
.note-body p { line-height: 1.6; }

.fig { margin: 1.6rem 0 0.5rem; }
.fig svg { width: 100%; height: auto; display: block; }
.fig svg text { font-family: "Chalkboard SE", "Shantell Sans", "Comic Sans MS", sans-serif; }
.figcap { font-size: 0.82rem; color: #1a1a1a; text-align: center; margin: 0.35rem auto 0; max-width: 90%;
          font-family: "Chalkboard SE", "Shantell Sans", "Comic Sans MS", sans-serif; }
svg .ptitle { font-size: 16px; font-weight: 700; fill: #111; }
svg .node   { font-size: 14px; fill: #111; }
svg .cap    { font-size: 12.5px; fill: #1a1a1a; }
svg .mark   { font-size: 22px; font-weight: 700; }

.cmp { border-collapse: collapse; margin: 1.5rem auto 0.4rem; width: 100%; max-width: 560px; font-size: 0.95rem; }
.cmp th, .cmp td { border: 1px solid #e4e4e4; padding: 7px 13px; text-align: left; }
.cmp thead th { background: #f6f8fa; color: #111; font-weight: 700; }
.cmp tbody td:first-child { font-weight: 600; color: #111; white-space: nowrap; }
</style>

<div class="note-body" markdown="1">

## Show, Don't Tell

<p class="note-meta">Updated July 19, 2026, 12:38 AM MDT</p>

We write reports as walls of text. But prose makes the reader do the hard part — rebuild your
picture in their head, sentence by sentence — and every reader rebuilds a slightly different one.

So when you write a report, give your creativity free rein: favor rich visualizations and
interactive tools over paragraphs. A figure carries the shape of a result at a glance; a demo
video carries what a system *does*; a slider or an explorer lets the reader ask their own
question and watch the answer move. Show the thing itself, and the paragraph's job shrinks to
one caption.

<figure class="fig">
<svg viewBox="0 0 760 316" role="img" aria-label="A wall of text makes the reader reconstruct the picture; a figure with a demo hands them the picture directly.">
  <defs>
    <marker id="ahT" markerWidth="9" markerHeight="9" refX="6.5" refY="3" orient="auto"><path d="M0,0 L7,3 L0,6 Z" fill="#d98a3d"/></marker>
    <marker id="ahS" markerWidth="9" markerHeight="9" refX="6.5" refY="3" orient="auto"><path d="M0,0 L7,3 L0,6 Z" fill="#1772d0"/></marker>
  </defs>

  <rect x="10" y="12" width="356" height="292" rx="12" fill="#fff8f1"/>
  <rect x="394" y="12" width="356" height="292" rx="12" fill="#f3f8ff"/>

  <!-- ===== Panel A: tell ===== -->
  <text x="188" y="40" text-anchor="middle" class="ptitle">📄 Tell</text>
  <rect x="118" y="56" width="140" height="118" rx="6" fill="#fff" stroke="#d98a3d" stroke-width="2"/>
  <line x1="130" y1="74"  x2="246" y2="74"  stroke="#e5b485" stroke-width="3"/>
  <line x1="130" y1="88"  x2="246" y2="88"  stroke="#e5b485" stroke-width="3"/>
  <line x1="130" y1="102" x2="246" y2="102" stroke="#e5b485" stroke-width="3"/>
  <line x1="130" y1="116" x2="246" y2="116" stroke="#e5b485" stroke-width="3"/>
  <line x1="130" y1="130" x2="246" y2="130" stroke="#e5b485" stroke-width="3"/>
  <line x1="130" y1="144" x2="246" y2="144" stroke="#e5b485" stroke-width="3"/>
  <line x1="130" y1="158" x2="212" y2="158" stroke="#e5b485" stroke-width="3"/>

  <path d="M188,180 L188,206" fill="none" stroke="#d98a3d" stroke-width="1.7" marker-end="url(#ahT)"/>

  <circle cx="176" cy="232" r="11" fill="#fdeede" stroke="#d98a3d" stroke-width="1.7"/>
  <rect x="164" y="248" width="24" height="17" rx="7" fill="#fdeede" stroke="#d98a3d" stroke-width="1.7"/>
  <text x="207" y="243" class="mark" fill="#c0491f">?</text>

  <text x="188" y="290" text-anchor="middle" class="cap">The reader rebuilds your picture — theirs may differ.</text>

  <!-- ===== Panel B: show ===== -->
  <text x="572" y="40" text-anchor="middle" class="ptitle">📊 Show</text>
  <rect x="502" y="56" width="140" height="118" rx="6" fill="#fff" stroke="#1772d0" stroke-width="2"/>
  <rect x="514" y="118" width="16" height="40" fill="#d3e4f7" stroke="#1772d0" stroke-width="1.4"/>
  <rect x="536" y="98"  width="16" height="60" fill="#d3e4f7" stroke="#1772d0" stroke-width="1.4"/>
  <rect x="558" y="80"  width="16" height="78" fill="#d3e4f7" stroke="#1772d0" stroke-width="1.4"/>
  <polyline points="514,100 544,84 574,72 596,66" fill="none" stroke="#1772d0" stroke-width="2.2"/>
  <circle cx="614" cy="84" r="12" fill="#eaf3fd" stroke="#1772d0" stroke-width="1.7"/>
  <path d="M610,78 L622,84 L610,90 Z" fill="#1772d0"/>
  <line x1="514" y1="166" x2="630" y2="166" stroke="#9cc3ec" stroke-width="3"/>
  <circle cx="586" cy="166" r="6" fill="#1772d0"/>

  <path d="M572,180 L572,206" fill="none" stroke="#1772d0" stroke-width="1.7" marker-end="url(#ahS)"/>

  <circle cx="560" cy="232" r="11" fill="#d3e4f7" stroke="#1772d0" stroke-width="1.7"/>
  <rect x="548" y="248" width="24" height="17" rx="7" fill="#d3e4f7" stroke="#1772d0" stroke-width="1.7"/>
  <text x="591" y="243" class="mark" fill="#1772d0">!</text>

  <text x="572" y="290" text-anchor="middle" class="cap">The reader sees your picture — the same one you saw.</text>
</svg>
<figcaption class="figcap">Tell, and every reader reconstructs the result from prose. Show — a figure, a demo, a control to drag — and everyone receives the same picture at a glance.</figcaption>
</figure>

Same result, two ways to report it:

<table class="cmp">
<thead><tr><th></th><th>📄 Telling</th><th>📊 Showing</th></tr></thead>
<tbody>
<tr><td>Reader's work</td><td>reread and imagine</td><td>look and see</td></tr>
<tr><td>What survives a week</td><td>a vague impression</td><td>the picture itself</td></tr>
<tr><td>Questions</td><td>email the author</td><td>drag the slider</td></tr>
</tbody>
</table>

Text still has one job it does best: precision. Keep it for the caption, the definition, the
number — one sharp sentence under the thing you showed. Everything else, show.

</div>
