---
layout: default
profile: teaching
permalink: /teaching/
title: Training / Teaching
lang: en
published: true
schema: Person
---

<h1 id="profile-heading">{{ page.title }}</h1>

<section id="about" aria-labelledby="about-heading" markdown="1">
  <h2 id="about-heading">{{ site.data.ui.profiles.teaching.links.about_me[site.active_lang] }}</h2>

**The most expensive part of teaching is not explaining: it's explaining without listening first.**

I discovered I liked teaching almost at the same time I discovered radio. At Aitiden, besides running the technical side, it fell to me to train my colleagues: how to handle a mixing console, what a balanced audio signal is — and why it was designed that way —, how to build your own cables by reading pinout diagrams. And something happened that I didn't expect: I enjoyed watching someone understand more than solving it myself.

Life then took me to teach very different things — in a folk group I helped teach how to play the chácaras and the Tenerife drum — and everywhere I heard the same: that I had patience and knew how to explain. It came up so often that I started observing myself to check whether it was true. Out of that observation came my way of teaching (you'll find it under Methodology).

I haven't stopped since, even without a classroom of my own: throughout my vocational studies and certificates I've tutored classmates who were falling behind with the syllabus and the practical work, and I've contributed materials and tools to help teachers expand theirs — always with their blessing, in their classes. One teacher went as far as telling me my assignments were "dissertations rather than homework", because I'm not satisfied with something merely working: I need to be able to explain why it works.

Where am I heading? I want to become a certified trainer — the official Train-the-Trainer certification is on my roadmap — and devote part of my path to what I do best: helping others understand. I'm especially drawn to technical and vocational training: teaching trades, tools and the why of things to the people who will actually use them.

If you're looking for someone who teaches with patience, adapts to whoever is in front of them and takes nothing for granted, write to me or have a look at the blog. I explain things as they are.
</section>

<section id="methodology" aria-labelledby="methodology-heading" markdown="1">
  <h2 id="methodology-heading">{{ site.data.ui.profiles.teaching.links.methodology[site.active_lang] }}</h2>

**I don't start by explaining: I start by listening.**

When someone brings me a question, the first thing is not to answer it but to understand it: I ask for details, I break it down, and even the way they struggle to explain it tells me a lot — that's usually where the concept lies that was taken for granted and never fully sank in. That's my real starting point: where the learner is, not where the syllabus says they should be.

From there I work backwards. I don't patch the question: I rebuild the missing foundation, and then I give it meaning — why what we've just cleared up matters, and in which future situations they'll run into it again. To understand something is also to know what that understanding is for.

If the idea still won't click, I translate it: analogies from the listener's world, not mine. A good familiar comparison opens more doors than three exact definitions.

I work best with small groups, where I can adapt the pace to each person — and when the classroom doesn't respond as expected, I change the plan, not the blame. I prepare my own teaching and audiovisual materials (graphic design, video, sound: from GIMP and Inkscape to Premiere), because tailor-made materials teach better than off-the-shelf ones.

And one rule I never break: **I teach so they stop needing me.** My goal isn't to solve today's problem, but for them to solve the next one without me — and to know why.
</section>

<section id="courses" aria-labelledby="courses-heading" markdown="0">
  <h2 id="courses-heading">{{ site.data.ui.profiles.teaching.links.courses[site.active_lang] }}</h2>
  {% for course in site.data.courses.courses %}
  <article class="course">
    <h3>{{ course.name[site.active_lang] }}</h3>

    <p class="course__meta">
      {{ course.year }}{% if course.center %} · {{ course.center[site.active_lang] }}{% endif %}{% if course.hours %} · {{ course.hours }} h{% endif %}
    </p>

    {% if course.description %}<p class="course__description">{{ course.description[site.active_lang] }}</p>{% endif %}

    {% if course.links %}
    <div class="course__links">
      {% for link in course.links %}
      <a class="button" href="{{ link.url }}">{{ link.text[site.active_lang] }}</a>
      {% endfor %}
    </div>
    {% endif %}
  </article>
  {% endfor %}
</section>