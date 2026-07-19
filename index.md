---
layout: default
title: Home
---

<details open>
  <summary class="fold-summary" style="cursor:pointer; padding:1% 2.5%;"><h2 style="display:inline; margin:0;">Projects</h2></summary>
<table class="projects" style="width:100%;border:0px;border-spacing:0px;border-collapse:separate;margin-right:auto;margin-left:auto;">
  <tr class="proj-row">
    <td class="proj-img" style="padding:1% 2.5%;vertical-align:top">
      <div class="proj-thumb"><a href="/motion-capture.html"><img src="./assets/img/motion-capture.jpg" alt="Motion Capture and 3D Reconstruction" class="project-image" /></a></div>
    </td>
    <td class="proj-text" style="padding:1% 2.5%;vertical-align:top">
      <h3><a href="/motion-capture.html">Motion Capture and 3D Reconstruction</a></h3>
      <p class="project-meta">
      A mobile, markerless rig of eleven synchronized smartphones.
      </p>
    </td>
  </tr>
  <tr class="proj-row">
    <td class="proj-img" style="padding:1% 2.5%;vertical-align:top">
      <div class="proj-thumb"><a href="https://yuboshell.github.io/led-sync-panel/report.html"><img src="./assets/img/led-timecode.jpg" alt="LED Timecode Panel" class="project-image" /></a></div>
    </td>
    <td class="proj-text" style="padding:1% 2.5%;vertical-align:top">
      <h3><a href="https://yuboshell.github.io/led-sync-panel/report.html">LED Timecode Panel</a></h3>
      <p class="project-meta">
      Measuring multi-camera synchronization to sub-millisecond precision.
      </p>
    </td>
  </tr>
</table>
</details>

<details open>
  <summary class="fold-summary" style="cursor:pointer; padding:1% 2.5%;"><h2 style="display:inline; margin:0;">Publications</h2></summary>
<table class="pubs" style="width:100%;border:0px;border-spacing:0px;border-collapse:separate;margin-right:auto;margin-left:auto;">

  {% for link in site.data.publications.main %}
  <tr class="proj-row">
    <td class="proj-img" style="padding:1% 2.5%;vertical-align:top">
      {% if link.image %}
      <div class="proj-thumb"><img src="{{ link.image }}" alt="{{ link.title }}" class="project-image" /></div>
      {% endif %}
    </td>
    <td class="proj-text" style="padding:1% 2.5%;vertical-align:top">
      <h3>{% if link.pdf %}<a href="{{ link.pdf }}">{{ link.title }}</a>{% else %}{{ link.title }}{% endif %}</h3>
      <p class="project-meta">
        {{ link.authors }}<br>
        <em>{{ link.conference }}</em>
      </p>
      <p class="linkblock">
        {% if link.code %} / <a href="{{ link.code }}">Code</a>{% endif %}
        {% if link.page %} / <a href="{{ link.page }}">Project Page</a>{% endif %}
        {% if link.bibtex %} / <a href="{{ link.bibtex }}">BibTeX</a>{% endif %}
        {% if link.notes %} <strong><i>{{ link.notes }}</i></strong>{% endif %}
      </p>
    </td>
  </tr>
  {% endfor %}

</table>
</details>

<details open style="padding:1% 2.5%;">
  <summary class="fold-summary" style="cursor:pointer;"><h2 style="display:inline; margin:0;">Blogs</h2></summary>
  <div style="margin-top:0.7rem;" class="blog-graph">
    <svg class="graph-svg" viewBox="0 0 780 400" role="img" aria-label="Blog posts grouped into three categories: Communication, Fun with Agents, and Study Notes.">
      <desc>Communication: Share a Link, Not a File; Show, Don't Tell. Fun with Agents: The Lab Management Workflow Revolution; A Menu, Visualized. Study Notes: How to Be Good at Research; Graph Tokenization.</desc>
      <path d="M107,200 C165,200 165,78 221,78"   fill="none" stroke="#1772d0" stroke-width="1.8"/>
      <path d="M107,200 C165,200 165,200 221,200" fill="none" stroke="#2f9e44" stroke-width="1.8"/>
      <path d="M107,200 C165,200 165,322 221,322" fill="none" stroke="#d98a1f" stroke-width="1.8"/>
      <path d="M349,78 C407,78 407,48 465,48"   fill="none" stroke="#1772d0" stroke-width="1.6"/>
      <path d="M349,78 C407,78 407,108 465,108" fill="none" stroke="#1772d0" stroke-width="1.6"/>
      <path d="M349,200 C407,200 407,170 465,170" fill="none" stroke="#2f9e44" stroke-width="1.6"/>
      <path d="M349,200 C407,200 407,230 465,230" fill="none" stroke="#2f9e44" stroke-width="1.6"/>
      <path d="M349,322 C407,322 407,292 465,292" fill="none" stroke="#d98a1f" stroke-width="1.6"/>
      <path d="M349,322 C407,322 407,352 465,352" fill="none" stroke="#d98a1f" stroke-width="1.6"/>
      <rect x="23" y="181" width="84" height="38" rx="10" fill="#f0f0f0" stroke="#555" stroke-width="1.8"/>
      <text x="65" y="205" text-anchor="middle" class="g-root">Blogs</text>
      <rect x="221" y="60" width="128" height="36" rx="9" fill="#eaf2fd" stroke="#1772d0" stroke-width="1.8"/>
      <text x="285" y="83" text-anchor="middle" class="g-cat" style="fill:#1772d0">Communication</text>
      <rect x="221" y="182" width="128" height="36" rx="9" fill="#e9f7ee" stroke="#2f9e44" stroke-width="1.8"/>
      <text x="285" y="205" text-anchor="middle" class="g-cat" style="fill:#268a3c">Fun with Agents</text>
      <rect x="221" y="304" width="128" height="36" rx="9" fill="#fdf3e3" stroke="#d98a1f" stroke-width="1.8"/>
      <text x="285" y="327" text-anchor="middle" class="g-cat" style="fill:#b5761a">Study Notes</text>
      <a href="/share-a-link-not-a-file.html"><rect x="465" y="32" width="210" height="32" rx="8" fill="#f5f9fe" stroke="#1772d0" stroke-width="1.5"/><text x="570" y="52" text-anchor="middle" class="g-post">Share a Link, Not a File</text></a>
      <a href="/show-dont-tell.html"><rect x="465" y="92" width="210" height="32" rx="8" fill="#f5f9fe" stroke="#1772d0" stroke-width="1.5"/><text x="570" y="112" text-anchor="middle" class="g-post">Show, Don't Tell</text></a>
      <a href="https://yuboshell.github.io/agent-native-lab/"><rect x="465" y="154" width="210" height="32" rx="8" fill="#f2fbf5" stroke="#2f9e44" stroke-width="1.5"/><text x="570" y="174" text-anchor="middle" class="g-post">Lab Management Workflow</text></a>
      <a href="/menu-visualized.html"><rect x="465" y="214" width="210" height="32" rx="8" fill="#f2fbf5" stroke="#2f9e44" stroke-width="1.5"/><text x="570" y="234" text-anchor="middle" class="g-post">A Menu, Visualized</text></a>
      <a href="/how-to-be-good-at-research.html"><rect x="465" y="276" width="210" height="32" rx="8" fill="#fdf7ec" stroke="#d98a1f" stroke-width="1.5"/><text x="570" y="296" text-anchor="middle" class="g-post">How to Be Good at Research</text></a>
      <a href="/graph-tokenization.html"><rect x="465" y="336" width="210" height="32" rx="8" fill="#fdf7ec" stroke="#d98a1f" stroke-width="1.5"/><text x="570" y="356" text-anchor="middle" class="g-post">Graph Tokenization</text></a>
    </svg>
    <div class="graph-list">
      <p class="glist-cat" style="color:#1772d0">Communication</p>
      <ul><li><a href="/share-a-link-not-a-file.html">Share a Link, Not a File</a></li><li><a href="/show-dont-tell.html">Show, Don't Tell</a></li></ul>
      <p class="glist-cat" style="color:#268a3c">Fun with Agents</p>
      <ul><li><a href="https://yuboshell.github.io/agent-native-lab/">The Lab Management Workflow Revolution</a></li><li><a href="/menu-visualized.html">A Menu, Visualized</a></li></ul>
      <p class="glist-cat" style="color:#b5761a">Study Notes</p>
      <ul><li><a href="/how-to-be-good-at-research.html">How to Be Good at Research</a></li><li><a href="/graph-tokenization.html">Graph Tokenization</a></li></ul>
    </div>
  </div>
</details>
