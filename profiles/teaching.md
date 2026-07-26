---
layout: default
profile: teaching
permalink: /teaching/
title: Formación / Docencia
lang: es
published: true
schema: Person
---

<h1 id="profile-heading">{{ page.title }}</h1>

<section id="about" aria-labelledby="about-heading" markdown="1">
  <h2 id="about-heading">{{ site.data.ui.profiles.teaching.links.about_me[site.active_lang] }}</h2>

**Lo más caro de enseñar no es explicar: es explicar sin escuchar antes.**

Descubrí que me gustaba enseñar casi a la vez que descubrí la radio. En Aitiden, además de llevar la técnica, me tocó formar a los compañeros: cómo se maneja una mesa de mezclas, qué es una señal balanceada —y por qué se diseñó así—, cómo fabricar tus propios cables interpretando los esquemas de pinout. Y ahí pasó algo que no esperaba: disfrutaba más viendo a alguien entender que resolviéndolo yo.

Luego la vida me llevó a enseñar cosas muy distintas —en un grupo folklórico ayudaba a enseñar a tocar las chácaras y el tambor de Tenerife— y en todas partes me decían lo mismo: que tenía paciencia y que sabía explicarme. Tanto se repitió que empecé a observarme para comprobar si era verdad. De esa observación salió mi manera de enseñar (la tienes en Metodología).

Desde entonces no he dejado de hacerlo, aunque fuera sin aula propia: en mis ciclos y certificados he tutorizado a los compañeros que iban más atrasados con el temario y las prácticas, y he aportado materiales y herramientas a los profesores para ampliar el suyo —siempre con su beneplácito, en sus clases—. Un profesor llegó a decirme que mis trabajos eran «tesinas más que trabajos», porque no me conformo con que algo funcione: necesito poder explicar por qué funciona.

¿Hacia dónde voy? Quiero certificarme como formador —la Formación de Formadores está en mi hoja de ruta— y dedicar parte de mi camino a lo que mejor sé hacer: que otros entiendan. Me ilusiona especialmente la formación técnica y profesional: enseñar oficios, herramientas y el porqué de las cosas a quien va a usarlos de verdad.

Si buscas a alguien que enseña con paciencia, se adapta a quien tiene delante y no da nada por sabido, escríbeme o pásate por el blog. Explico las cosas como son.
</section>

<section id="methodology" aria-labelledby="methodology-heading" markdown="1">
  <h2 id="methodology-heading">{{ site.data.ui.profiles.teaching.links.methodology[site.active_lang] }}</h2>

**No empiezo explicando: empiezo escuchando.**

Cuando alguien me trae una duda, lo primero no es responderla, sino entenderla: le pido detalles, la desmenuzo, y hasta la forma en que no consigue explicármela me dice mucho — ahí suele estar el concepto que se dio por sabido y nunca terminó de asimilarse. Ese es mi punto de partida real: el del alumno, no el del temario.

Desde ahí trabajo hacia atrás. No parcheo la duda: reconstruyo el cimiento que le falta, y después le doy sentido — por qué importa lo que acabamos de aclarar, en qué situaciones futuras se lo va a volver a encontrar. Entender algo es también saber para qué sirve entenderlo.

Si la idea se resiste, la traduzco: analogías del mundo de quien me escucha, no del mío. Una buena comparación familiar abre más puertas que tres definiciones exactas.

Trabajo mejor con grupos reducidos, donde puedo adaptar el ritmo a cada persona — y cuando el aula no responde como esperaba, cambio el plan, no la culpa. Preparo mis propios materiales didácticos y audiovisuales (diseño gráfico, vídeo, sonido: de GIMP e Inkscape a Premiere), porque el material hecho a medida enseña mejor que el genérico.

Y una regla que no rompo: **enseño para que dejen de necesitarme.** Mi objetivo no es resolver el problema de hoy, sino que la próxima vez lo resuelvan sin mí — y que sepan por qué.
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