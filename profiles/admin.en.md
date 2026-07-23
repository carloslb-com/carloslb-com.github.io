---
layout: default
profile: admin
permalink: /admin/
title: Tax System, Account and Human Resource Administration
lang: en
published: true
---

<section id="about" aria-labelledby="about-heading" markdown="1">
  <h2 id="about-heading">{{ site.data.ui.profiles.admin.links.about_me[site.active_lang] }}</h2>

**The most expensive part of management is not the paperwork: it's taking it for granted without checking it.**

I've spent years doing the opposite — double-checking, preparing more than asked and taking nothing for granted — first out of curiosity, then out of conviction. I'm an accounting and administrative management technician, currently getting certified in human resources, and this is what's behind that.

My calling didn't come from an office: it came from seeing what happens when things are done badly. I've seen advisors dodge their responsibilities and leave companies exposed to penalties and inspections, and I've seen many people lost in paperwork they don't understand. So I started helping those around me: explaining rights, yes, but also duties — and the cost of not meeting them. I discovered two things: people understand when things are explained well, and few things are as fulfilling as seeing a well-prepared document take a weight off someone's shoulders.

A real example: a tax return from someone close to me arrived "already done", with a result of roughly €2,500 to pay. I went through it item by item — the draft had swallowed data that did apply — and it ended up, approximately, at less than €700, and with payment in instalments. Together with a payment plan for local taxes, that person went from drowning to catching up and breathing month to month. That's my bar: management should show in the life of the person who entrusts it to you, not just in the folder.

My way of working has a reputation for being cautious: I prepare more documentation than requested, just in case they ask for it. I'd rather have one "just in case" too many than a trip back for the missing paper. Call it professional deformation — the same one that makes me check everything twice — but my filings rarely bounce back.

As for what I can do: accounting and tax management (Professional Certificate in Accounting and Administrative Management for Auditing), human resources (Professional Certificate in progress), data protection (GDPR certification) and direct dealings with the Tax Agency, Social Security and local administrations. I have incorporated and chaired associations — bylaws, tax authority census, economic activity — and I've experienced management from the inside at a professional advisory firm. *(Details under Experience and Certifications.)*

Where am I heading? I'd like to work at an advisory firm: helping good business owners, entrepreneurs and employees feel at ease with their numbers, making sure their work pays off, and clearing the way for them to grow as far as they want. Because I believe in one idea above all: **good management is like the soil's fertiliser and acidity — you don't see it, but it shapes what can grow, how it grows and how fast.**

If you're looking for someone detail-oriented, who enjoys helping and treats your project as their own, write to me or have a look at the blog. I do the numbers straight.
</section>

<section id="experience" aria-labelledby="experience-heading" markdown="0">
  <h2 id="experience-heading">{{ site.data.ui.profiles.admin.links.experience[site.active_lang] }}</h2>
  {% for experience in site.data.experiences.experiences %}
    <article class="experience">
      <h3>{{ experience.jobtitle[site.active_lang] }}</h3>
      <p class="experience__meta">
        {{ experience.start }}{% if experience.end %} - {{ experience.end }}{% elsif experience.current %} - {{ site.data.ui.common.current[site.active_lang] }}{% endif %}{% if experience.location %} · {{ experience.location[site.active_lang] }}{% endif %}
      </p>
      {% if experience.description %}<p class="experience__description">{{ experience.description[site.active_lang] }}</p>{% endif %}
      {% if experience.companies %}
      <ul class="experience__companies">
        {% for company in experience.companies %}
        <li>{{ company }}</li>
        {% endfor %}
      </ul>
      {% endif %}
      {%- if experience.functions -%}
        <p class="experience__functions">{{ experience.functions[site.active_lang] }}</p>
      {%- endif -%}
    </article>
  {% endfor %}
</section>

<section id="certifications" aria-labelledby="certifications-heading" markdown="0">
  <h2 id="certifications-heading">{{ site.data.ui.profiles.admin.links.certifications[site.active_lang] }}</h2>
{% for cert in site.data.certifications.certifications %}
<article class="certification">
  <h3>{{ cert.name[site.active_lang] }}</h3>

  <p class="certification__meta">
    {{ cert.year }}{% if cert.center %} · {{ cert.center[site.active_lang] }}{% endif %}{% if cert.hours %} · {{ cert.hours }} h{% endif %}
  </p>

  {% if cert.links %}
  <div class="certification__links">
    {% for link in cert.links %}
    <a class="button" href="{{ link.url }}">{{ link.text[site.active_lang] }}</a>
    {% endfor %}
  </div>
  {% endif %}
</article>
{% endfor %}
</section>