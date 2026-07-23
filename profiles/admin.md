---
layout: default
profile: admin
permalink: /admin/
title: Gestoría Fiscal, Contable y de Recursos Humanos
lang: es
published: true
---

<section id="about" aria-labelledby="about-heading" markdown="1">
  <h2 id="about-heading">{{ site.data.ui.profiles.admin.links.about_me[site.active_lang] }}</h2>

**Lo más caro de la gestión no es el papeleo: es darlo por bueno sin revisarlo.**

Llevo años haciendo lo contrario —comprobar, preparar de más y no dar nada por hecho—, primero por curiosidad y luego por convicción. Soy técnico en gestión contable y administrativa, me estoy certificando en recursos humanos, y esto es lo que hay detrás.

La vocación no me vino de un despacho: me vino de ver lo que pasa cuando se hace mal. He visto asesores que escurren el bulto y dejan empresas expuestas a sanciones e inspecciones, y he visto a mucha gente perdida ante trámites que no entiende. Así que empecé a ayudar a quien tenía cerca: explicando derechos, sí, pero también deberes — y lo que cuesta no cumplirlos. Descubrí dos cosas: que la gente entiende cuando se le explica bien, y que pocas cosas llenan tanto como ver que un papel bien hecho le quita un peso de encima a alguien.

Un ejemplo real: una declaración de la renta de alguien de mi entorno venía "ya hecha" con un resultado de unos 2.500 € a pagar. La revisé partida a partida —el borrador se había comido datos que sí correspondían— y se quedó, aproximadamente, en menos de 700 €, y además con pago fraccionado. Sumado a un plan de pagos con los tributos municipales, esa persona pasó de ahogarse a ponerse al día y respirar mes a mes. Ese es mi listón: que la gestión se note en la vida de quien la encarga, no solo en la carpeta.

Mi manera de trabajar tiene fama de precavida: preparo más documentación de la que piden, por si acaso la piden. Prefiero un "por si" de más que un viaje de vuelta a por el papel que falta. Será deformación —la misma que me hace revisarlo todo dos veces—, pero mis trámites no suelen volver rebotados.

En cuanto a lo que sé hacer: gestión contable y fiscal (Certificado de Profesionalidad en Gestión Contable y Gestión Administrativa para Auditoría), recursos humanos (Certificado de Profesionalidad en curso), protección de datos (certificación en RGPD) y trato directo con la Agencia Tributaria, la Seguridad Social y las administraciones locales. He constituido y presidido asociaciones —estatutos, censo de Hacienda, actividad económica— y he vivido la gestión desde dentro en una asesoría profesional. *(El detalle, en Experiencia y Certificaciones.)*

¿Hacia dónde voy? Me gustaría ejercer en una asesoría: ayudar al buen empresario, al emprendedor y al empleado a estar tranquilos con sus números, a que su trabajo les rente y a despejarles el camino para crecer hasta donde quieran. Porque creo en una idea por encima del resto: **una buena gestión es como el abono y la acidez del terreno — no se ve, pero influye en qué puede crecer, cómo lo hace y en cuánto tiempo.**

Si buscas a alguien detallista, que disfruta ayudando y que trata tu proyecto como propio, escríbeme o pásate por el blog. Hago las cuentas como son.
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