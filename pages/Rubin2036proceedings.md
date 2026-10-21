---
title: Rubin2036 Workshop Proceedings
lede: Science cases and technical upgrades explored at the August 2026 workshop
hero_image: /assets/img/rubin2036_banner.jpg
hero_image_alt: Rubin 2036 banner with Vera C. Rubin Observatory, NSF, Department of Energy, and KIPAC logos.
---

This page collects materials from the Rubin 2036 workshop: the workshop summary report,
the post-workshop group white papers, other contributions, slides from a selection of
the talks, and the workshop agenda. The full set of contributed documents is archived in
the [Rubin 2036 Zenodo community](https://zenodo.org/communities/rubin2036workshop).

## Workshop Summary Report

The workshop summary report, *The "Rubin 2036: Opportunities for Discovery" Workshop: A
Community Roadmap for the Future of the Vera C. Rubin Observatory After the LSST*
(A. A. Plazas Malagón et al.), is available on arXiv and in the Zenodo community.

<div class="item-list">
  <article class="list-item">
    <div>
      <h3><a href="https://arxiv.org/abs/2610.28482">The &ldquo;Rubin 2036: Opportunities for Discovery&rdquo; Workshop: A Community Roadmap for the Future of the Vera C. Rubin Observatory After the LSST</a></h3>
      <p>Authors: A. A. Plazas Malagón et al.</p>
      <p>arXiv: <a href="https://arxiv.org/abs/2610.28482">arXiv:2610.28482</a> &middot; Zenodo: <a href="https://zenodo.org/records/23535364">10.48550/arXiv.2610.28482</a></p>
    </div>
  </article>
</div>

## Group White Papers

Each working group developed a white paper after the workshop. The papers are archived
in the [Rubin 2036 Zenodo community](https://zenodo.org/communities/rubin2036workshop).

<div class="item-list">
  {% for paper in site.data.Rubin2036papers %}
    <article class="list-item">
      <div>
        {% if paper.group %}<p class="item-meta">{{ paper.group }}</p>{% endif %}
        <h3><a href="{% include link-target.html url=paper.url %}">{{ paper.title }}</a></h3>
        {% if paper.authors %}<p>Authors: {{ paper.authors }}</p>{% endif %}
        {% if paper.doi %}<p>DOI: <a href="https://doi.org/{{ paper.doi }}">{{ paper.doi }}</a></p>{% endif %}
      </div>
    </article>
  {% endfor %}
</div>

## Other Contributions

Additional contributions archived in the Rubin 2036 Zenodo community.

<div class="item-list">
  {% for item in site.data.Rubin2036other %}
    <article class="list-item">
      <div>
        {% if item.kind %}<p class="item-meta">{{ item.kind }}</p>{% endif %}
        <h3><a href="{% include link-target.html url=item.url %}">{{ item.title }}</a></h3>
        {% if item.authors %}<p>Authors: {{ item.authors }}</p>{% endif %}
        {% if item.doi %}<p>DOI: <a href="https://doi.org/{{ item.doi }}">{{ item.doi }}</a></p>{% endif %}
      </div>
    </article>
  {% endfor %}
</div>

## Talks

{% assign talks_by_date = site.data.Rubin2036talks | sort: "date" | reverse %}

<div class="item-list">
  {% for doc in talks_by_date %}
    <article class="list-item">
      <div>
        <p class="item-meta">{{ doc.date | date: "%B %-d, %Y" }}</p>
        {% if doc.url and doc.url != "#" %}
          <h3><a href="{% include link-target.html url=doc.url %}">{{ doc.title }}</a></h3>
        {% else %}
          <h3>{{ doc.title }}</h3>
        {% endif %}
        {% if doc.authors %}<p>Authors: {{ doc.authors }}</p>{% endif %}
        {% if doc.description %}<p>{{ doc.description }}</p>{% endif %}
      </div>
    </article>
  {% endfor %}
</div>

## Agenda

Opportunities for Discovery — The Future of the Rubin Observatory After the LSST.
KIPAC / SLAC, 3–5 August 2026 (Mon–Wed).

{% for day in site.data.Rubin2036agenda %}
<h3 class="agenda-day">{{ day.day }}{% if day.subtitle %} <span class="agenda-sub">{{ day.subtitle }}</span>{% endif %}</h3>
<div class="agenda-wrap">
<table class="agenda-table">
  <thead>
    <tr><th>Time</th><th>Session</th><th>Speaker</th></tr>
  </thead>
  <tbody>
    {% for s in day.sessions %}<tr><td>{{ s.time }}</td><td>{{ s.topic }}</td><td>{{ s.speaker }}</td></tr>
    {% endfor %}
  </tbody>
</table>
</div>
{% endfor %}

## Contributing

To add your document:
1. Upload your document to Zenodo and save the DOI.
2. In a branch or fork of this repository, edit `_data/Rubin2036papers.yml` to add a card for your document, including the Zenodo DOI.
3. Make a Pull Request to this repository.

The admins will review your document for consistency with the template and coherence and merge in your changes.

<figure>
  <img src="{% include link-target.html url='/assets/img/rubin2036_group_photo.jpg' %}" alt="Rubin 2036 workshop participants gathered for a group photo, with several remote participant headshots along the bottom.">
  <figcaption>Rubin 2036 workshop group photo.</figcaption>
</figure>
