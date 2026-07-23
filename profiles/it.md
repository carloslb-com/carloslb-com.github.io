---
layout: default
profile: it
permalink: /it/
title: Informática y Telecomunicaciones
lang: es
published: true
---

<section id="about" aria-labelledby="about-heading" markdown="1">
  <h2 id="about-heading">{{ site.data.ui.profiles.it.links.about_me[site.active_lang] }}</h2>

**Cuando un sistema crítico se cae, lo más caro no es no saber arreglarlo: es arreglarlo con prisa y sin criterio.**

Llevo más de quince años haciendo lo contrario: diagnosticar con cabeza y resolver sin romper nada por el camino. Soy técnico en Informática y Telecomunicaciones, y esto es lo que hay detrás.

Empecé con siete años delante de un Commodore 64: tecleaba yo mismo los comandos para echar a andar mis juegos —me lo explicaron una sola vez—. Desde ahí arrancó mi viaje por la informática. Lo que vino después fue pura curiosidad: FidoNet y el descubrimiento de que un ordenador conectaba con el mundo; tardes con mi padre montando equipos y comunicándolos por puerto serie y paralelo; mis primeros programas.

Más tarde llegó la radio, y con ella mi pasión por las telecomunicaciones: ver cómo se monta, se programa y se mantiene un sistema de transmisión completo me enganchó hasta el punto de matricularme en un ciclo formativo de grado superior. Y la radio no reemplazó a la informática: la expandió. Nunca he dejado de ver en un ordenador un lienzo en blanco donde construir lo que haga falta.

Mi forma de trabajar se entiende mejor con un ejemplo real: un servidor crítico cae estando yo de vacaciones, con presión para resolver ya. Diagnostiqué el problema (un RAID mal montado y un puerto deteriorado), confirmé que los datos estaban a salvo y me negué a tocar el hardware sin una copia de seguridad verificada. Me llamaron exagerado; al final tenía razón. Ese es mi sello: cabeza fría y criterio cuando las cosas se tuercen. Y soluciones robustas con software libre y pocos recursos —que lo barato, bien hecho, también funciona—.

En cuanto a mis habilidades, administro sistemas y redes (VPN, RADIUS, Ubiquiti), levanto y mantengo bases de datos (SQL Server, MySQL) y programo lo que falta con Python, SQL, PHP, JavaScript o C# —y, si un proyecto lo pide, amplío el repertorio—. A todo esto se suman más de quince años de experiencia, certificación en RGPD e inglés C1.

Mi primer proyecto, hace ya tiempo, fue un sistema de gestión que ayudó a un centro a obtener la certificación ISO 9001; el último es esta misma web. (Hay más en mis proyectos.)

Asumo responsabilidades y digo la verdad aunque incomode. Enseño a quien sabe menos para que no dependa de mí, en lugar de hacerme imprescindible. Y procuro entender el trabajo de los demás para ayudar sin estorbar. Porque creo en una idea por encima del resto: la tecnología está para ayudar a las personas, no para sustituirlas.

Me ilusionan los proyectos con impacto —los que hacen el trabajo de la gente más fácil sin solapar su esfuerzo—.
Si te encaja esta forma de trabajar, escríbeme o pásate por el blog y los proyectos. Cuento las cosas como son.
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