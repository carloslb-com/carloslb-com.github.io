---
layout: default
profile: home
permalink: /accessibility.html
title: Compromiso de accesibilidad
lang: es
schema: WebPage
---

# Compromiso de accesibilidad

Este sitio se ha construido buscando que cualquiera pueda usarlo: con teclado, con
lector de pantalla, con la letra ampliada o desde un móvil viejo. Esta página cuenta
qué se ha hecho, cómo se ha comprobado y qué falta.

## Por qué esta página existe

No estoy obligado a publicarla. El Real Decreto 1112/2018 se aplica al sector público,
y la Ley 11/2023 a determinados productos y servicios comerciales; este es el sitio
personal de un particular, sin actividad económica, así que no me alcanza ninguna de
las dos.

La publico porque la accesibilidad me parece parte de hacer bien el trabajo, y porque
un compromiso que no se puede comprobar no es un compromiso.

## Objetivo y estado

El objetivo es **WCAG 2.2, nivel AA**.

A día de hoy el sitio es **parcialmente conforme**: las páginas que se han evaluado
cumplen los criterios comprobados, pero la evaluación todavía no cubre todo el sitio
ni todas las condiciones de uso. El detalle está más abajo, sin adornos.

## Qué se ha comprobado, y cómo

**Herramientas y método**

- Análisis automático y **pruebas guiadas** con axe DevTools (configuración WCAG 2.2 AA,
  incluyendo reglas avanzadas y buenas prácticas): teclado, formularios, estructura,
  imágenes, tablas, diálogos y elementos interactivos.
- Revisión manual con teclado.
- Revisión con lector de pantalla (Orca sobre Firefox, en Linux).

**Alcance de la última evaluación** — [PENDIENTE: fecha]

Se evaluaron [PENDIENTE: nº] páginas de la versión en español: portada, los tres
perfiles, contacto, el blog, las tres páginas legales, la página de confirmación de
envío y la página de error 404. Resultado: sin incidencias detectadas.

## Qué falta por comprobar

- La **versión en inglés** del sitio no se ha evaluado todavía.
- Los listados de blog de cada perfil y las páginas de artículo individuales.
- El sitio ofrece **ocho combinaciones de color** (cuatro perfiles, cada uno en modo
  claro y oscuro). El contraste se ha medido en [PENDIENTE], pero no en todas.
- Zoom al 200 %, aumento del espaciado del texto y visualización en pantallas muy
  estrechas.

[PENDIENTE: limitaciones conocidas que no se vayan a resolver a corto plazo, si las hay]

## Decisiones técnicas que afectan al acceso

- **El sitio funciona sin JavaScript.** El JavaScript es una mejora: si no se ejecuta,
  se pierde comodidad (el contador de caracteres, el aviso de error inmediato, el color
  del artículo según el perfil), nunca el acceso al contenido ni la navegación.
- **El formulario de contacto funciona sin JavaScript**: usa validación nativa del
  navegador, y la verificación anti-abuso se hace en el servidor del proveedor
  (Form.taxi) en una página propia después de enviar, no con un script incrustado aquí.
- **No hay cookies ni rastreadores.** Tipografías, iconos y bibliotecas están alojados
  en este mismo sitio, así que navegar por aquí no implica conexiones a terceros.
- **Se respeta la preferencia de movimiento reducida** del sistema operativo.
- Hay un enlace para **saltar directamente al contenido**, visible al pulsar el
  tabulador.
- Las tipografías son [PENDIENTE: mencionar Atkinson Hyperlegible como cuerpo de texto,
  que está diseñada para baja visión — decidir si contarlo aquí].

## Si encuentras una barrera

{% assign contacturl = site.data.navigation.common | where: "name", "contact" %}

Escríbeme por el [formulario de contacto]({{ contacturl[0].url | relative_url }})
y cuéntame qué ha pasado: qué página, qué intentabas hacer y con qué herramienta.
Lo agradeceré de verdad, y lo corregiré en cuanto pueda.

No tengo un plazo de respuesta comprometido ni un procedimiento formal de reclamación:
esto es un sitio personal, no una administración. Pero leo todo lo que llega.

## Fechas

- Compromiso preparado el [PENDIENTE].
- Última evaluación: [PENDIENTE].