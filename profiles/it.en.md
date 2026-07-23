---
layout: default
profile: it
permalink: /it/
title: Information Technology Systems
lang: en
published: true
---

<section id="about" aria-labelledby="about-heading" markdown="1">
  <h2 id="about-heading">{{ site.data.ui.profiles.it.links.about_me[site.active_lang] }}</h2>

**When a critical system goes down, the most expensive thing is not failing to know how to fix it: it's fixing it in a hurry and without judgement.**

I've spent more than fifteen years doing the opposite: diagnosing with a cool head and solving problems without breaking anything along the way. I'm an IT and Telecommunications technician, and this is what's behind that.

I started at seven years old in front of a Commodore 64: I typed in the commands to get my games running myself — I was shown only once. That's where my journey through computing began. What followed was pure curiosity: FidoNet and the discovery that a computer could connect you to the world; afternoons with my father assembling machines and linking them through serial and parallel ports; my first programs.

Later came radio, and with it my passion for telecommunications: seeing how a complete transmission system is built, programmed and maintained hooked me to the point of enrolling in a higher vocational degree. And radio didn't replace computing: it expanded it. I've never stopped seeing a computer as a blank canvas where you can build whatever is needed.

The way I work is best understood through a real example: a critical server goes down while I'm on holiday, with pressure to fix it right away. I diagnosed the problem (a poorly assembled RAID and a deteriorated port), confirmed the data was safe, and refused to touch the hardware without a verified backup. I was called an alarmist; in the end I was right. That's my hallmark: a cool head and sound judgement when things go wrong. And robust solutions with free software and scarce resources — because inexpensive, done right, works too.

As for my skills, I administer systems and networks (VPN, RADIUS, Ubiquiti), I build and maintain databases (SQL Server, MySQL) and I program whatever's missing with Python, SQL, PHP, JavaScript or C# — and, if a project calls for it, I expand the repertoire. On top of all this: more than fifteen years of experience, GDPR certification and C1 English.

My first project, quite some time ago, was a management system that helped a site obtain its ISO 9001 certification; the latest is this very website. (There's more in my projects.)

I take on responsibility and tell the truth even when it's uncomfortable. I teach those who know less so they don't depend on me, instead of making myself indispensable. And I make a point of understanding other people's work so I can help without getting in the way. Because I believe in one idea above all: technology is here to help people, not to replace them.

I'm drawn to projects with impact — the ones that make people's work easier without overriding their effort.

If this way of working resonates with you, write to me or have a look at the blog and the projects. I tell things as they are.
</section>


<section id="projects" aria-labelledby="projects-heading" markdown="0">
  <h2 id="projects-heading">{{ site.data.ui.profiles.it.links.projects[site.active_lang] }}</h2>
  {% for project in site.data.projects.projects %}
    <article class="project">
      <h3>{{ project.title[site.active_lang] }}</h3>
      <p class="project__meta">
        {{ project.year }}{% if project.client %} · {{ project.client[site.active_lang] }}{% endif %}
      </p>
      <p class="project__description">{{ project.description[site.active_lang] }}</p>

      {%- if project.technologies -%}
        <h4>{{ site.data.ui.profiles.it.sections.techs_used[site.active_lang] }}</h4>
        <ul class="project__tech">
          {%- for tech in project.technologies -%}
            <li>{{ tech[site.active_lang] }}</li>
          {%- endfor -%}
        </ul>
      {%- endif -%}

      {%- if project.links -%}
        <h4>{{ site.data.ui.profiles.it.sections.links[site.active_lang] }}</h4>
        <div class="project__links">
          {%- for link in project.links -%}
            <a class="button" href="{{ link.url }}">{{ link.text[site.active_lang] }}</a>
          {%- endfor -%}
        </div>
      {%- endif -%}
    </article>
  {% endfor %}
</section>

<section id="skills" aria-labelledby="skills-heading" markdown="0">
  <h2 id="skills-heading">{{ site.data.ui.profiles.it.links.skills[site.active_lang] }}</h2>
{% for category in site.data.skills.categories %}
  <div class="skills-category">
    <h3>{{ category.name[site.active_lang] }}</h3>
    <ul class="skills-list">
    {% assign sorted_items = category.items | sort %}
      {% for item in sorted_items %}
        <li>{{ item }}</li>
      {% endfor %}
    </ul>
  </div>
{% endfor %}
</section>