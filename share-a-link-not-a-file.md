---
layout: default
title: "Share a Link, Not a File"
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
svg .vlabel { font-size: 12px; font-weight: 600; fill: #a8481b; }

@keyframes softpulse { 0%,100% { opacity:.06; transform:scale(1); } 50% { opacity:.14; transform:scale(1.15); } }
svg .pulse { fill:#1772d0; opacity:.08; transform-box:fill-box; transform-origin:center; animation:softpulse 2.8s ease-in-out infinite; }
@media (prefers-reduced-motion: reduce) { svg .pulse { animation: none; } }

.cmp { border-collapse: collapse; margin: 1.5rem auto 0.4rem; width: 100%; max-width: 560px; font-size: 0.95rem; }
.cmp th, .cmp td { border: 1px solid #e4e4e4; padding: 7px 13px; text-align: left; }
.cmp thead th { background: #f6f8fa; color: #111; font-weight: 700; }
.cmp tbody td:first-child { font-weight: 600; color: #111; white-space: nowrap; }
</style>

<div class="note-body" markdown="1">

## Share a Link, Not a File

<p class="note-meta">Updated July 18, 2026, 10:48 PM MDT</p>

We still share our work by emailing files. But a file is a **copy** — and copies multiply, scatter, and fall out of date.

<figure class="fig">
<svg viewBox="0 0 760 316" role="img" aria-label="Sending a file creates many drifting copies; sending a link points everyone at one current copy.">
  <defs>
    <marker id="ahA" markerWidth="9" markerHeight="9" refX="6.5" refY="3" orient="auto"><path d="M0,0 L7,3 L0,6 Z" fill="#d98a3d"/></marker>
    <marker id="ahB" markerWidth="9" markerHeight="9" refX="6.5" refY="3" orient="auto"><path d="M0,0 L7,3 L0,6 Z" fill="#1772d0"/></marker>
  </defs>

  <rect x="10" y="12" width="356" height="292" rx="12" fill="#fff8f1"/>
  <rect x="394" y="12" width="356" height="292" rx="12" fill="#f3f8ff"/>

  <!-- ===== Panel A: send a file ===== -->
  <text x="188" y="40" text-anchor="middle" class="ptitle">📎 Send a file</text>
  <rect x="148" y="58" width="80" height="36" rx="9" fill="#fff" stroke="#d98a3d" stroke-width="2"/>
  <text x="188" y="81" text-anchor="middle" class="node">You</text>

  <path d="M188,96 L64,206"  fill="none" stroke="#d98a3d" stroke-width="1.7" marker-end="url(#ahA)"/>
  <path d="M188,96 L146,206" fill="none" stroke="#d98a3d" stroke-width="1.7" marker-end="url(#ahA)"/>
  <path d="M188,96 L230,206" fill="none" stroke="#d98a3d" stroke-width="1.7" marker-end="url(#ahA)"/>
  <path d="M188,96 L312,206" fill="none" stroke="#d98a3d" stroke-width="1.7" marker-end="url(#ahA)"/>

  <path d="M44,212 L72,212 L84,224 L84,264 L44,264 Z" fill="#fff" stroke="#d98a3d" stroke-width="1.7"/>
  <path d="M72,212 L72,224 L84,224" fill="none" stroke="#d98a3d" stroke-width="1.7"/>
  <text x="64" y="246" text-anchor="middle" class="vlabel">v1</text>

  <path d="M126,212 L154,212 L166,224 L166,264 L126,264 Z" fill="#fff" stroke="#d98a3d" stroke-width="1.7"/>
  <path d="M154,212 L154,224 L166,224" fill="none" stroke="#d98a3d" stroke-width="1.7"/>
  <text x="146" y="246" text-anchor="middle" class="vlabel">v1</text>

  <path d="M210,212 L238,212 L250,224 L250,264 L210,264 Z" fill="#fff" stroke="#d98a3d" stroke-width="1.7"/>
  <path d="M238,212 L238,224 L250,224" fill="none" stroke="#d98a3d" stroke-width="1.7"/>
  <text x="230" y="246" text-anchor="middle" class="vlabel">v1</text>

  <path d="M292,212 L320,212 L332,224 L332,264 L292,264 Z" fill="#fff5ef" stroke="#c0491f" stroke-width="2"/>
  <path d="M320,212 L320,224 L332,224" fill="none" stroke="#c0491f" stroke-width="2"/>
  <text x="312" y="246" text-anchor="middle" class="vlabel" style="fill:#c0491f">v2</text>

  <text x="188" y="290" text-anchor="middle" class="cap">One file → copies that drift out of sync.</text>

  <!-- ===== Panel B: send a link ===== -->
  <text x="572" y="40" text-anchor="middle" class="ptitle">🔗 Send a link</text>
  <circle class="pulse" cx="572" cy="80" r="34"/>
  <path d="M540,54 L588,54 L604,70 L604,108 L540,108 Z" fill="#eaf3fd" stroke="#1772d0" stroke-width="2.4"/>
  <path d="M588,54 L588,70 L604,70" fill="none" stroke="#1772d0" stroke-width="2.4"/>
  <line x1="550" y1="80" x2="588" y2="80" stroke="#9cc3ec" stroke-width="2.4"/>
  <line x1="550" y1="88" x2="588" y2="88" stroke="#9cc3ec" stroke-width="2.4"/>
  <line x1="550" y1="96" x2="580" y2="96" stroke="#9cc3ec" stroke-width="2.4"/>

  <circle cx="450" cy="202" r="10" fill="#d3e4f7" stroke="#1772d0" stroke-width="1.6"/>
  <rect x="440" y="216" width="20" height="15" rx="6" fill="#d3e4f7" stroke="#1772d0" stroke-width="1.6"/>
  <circle cx="528" cy="202" r="10" fill="#d3e4f7" stroke="#1772d0" stroke-width="1.6"/>
  <rect x="518" y="216" width="20" height="15" rx="6" fill="#d3e4f7" stroke="#1772d0" stroke-width="1.6"/>
  <circle cx="614" cy="202" r="10" fill="#d3e4f7" stroke="#1772d0" stroke-width="1.6"/>
  <rect x="604" y="216" width="20" height="15" rx="6" fill="#d3e4f7" stroke="#1772d0" stroke-width="1.6"/>
  <circle cx="694" cy="202" r="10" fill="#d3e4f7" stroke="#1772d0" stroke-width="1.6"/>
  <rect x="684" y="216" width="20" height="15" rx="6" fill="#d3e4f7" stroke="#1772d0" stroke-width="1.6"/>

  <path d="M450,190 L548,110" fill="none" stroke="#1772d0" stroke-width="1.7" marker-end="url(#ahB)"/>
  <path d="M528,190 L562,112" fill="none" stroke="#1772d0" stroke-width="1.7" marker-end="url(#ahB)"/>
  <path d="M614,190 L582,112" fill="none" stroke="#1772d0" stroke-width="1.7" marker-end="url(#ahB)"/>
  <path d="M694,190 L596,110" fill="none" stroke="#1772d0" stroke-width="1.7" marker-end="url(#ahB)"/>

  <text x="572" y="290" text-anchor="middle" class="cap">Everyone reads one copy — always current.</text>
</svg>
<figcaption class="figcap">Send a file and one document fans out into copies that drift. Send a link and everyone converges on the same, always-current copy.</figcaption>
</figure>

Same document, two ways to share it:

<table class="cmp">
<thead><tr><th></th><th>📎 A file</th><th>🔗 A link</th></tr></thead>
<tbody>
<tr><td>Copies</td><td>one per person</td><td>one, shared by all</td></tr>
<tr><td>Staying current</td><td>frozen when sent</td><td>always the latest</td></tr>
<tr><td>Cleanup</td><td>everyone deletes later</td><td>nothing to delete</td></tr>
</tbody>
</table>
</div>
