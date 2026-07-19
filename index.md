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

<details style="padding:1% 2.5%;">
  <summary class="fold-summary" style="cursor:pointer;"><h2 style="display:inline; margin:0;">Blogs</h2></summary>
  <div style="margin-top:0.7rem;">
    <h3><a href="/share-a-link-not-a-file.html">Share a Link, Not a File</a></h3>
    <h3><a href="/menu-visualized.html">A Menu, Visualized</a></h3>
    <h3><a href="/how-to-be-good-at-research.html">Study Note: How to Be Good at Research</a></h3>
    <h3><a href="/graph-tokenization.html">Study Note: Graph Tokenization</a></h3>
    <h3><a href="https://yuboshell.github.io/agent-native-lab/">The Lab Management Workflow Revolution</a></h3>
  </div>
</details>
