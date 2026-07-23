---
layout: default
profile: home
permalink: /contact/
title: Contacto
lang: es
---

<div class="contact__introduction">

    <p>Me alegra que quieras escribirme.</p>
    <p>Cuéntame tu consulta o propuesta en el formulario y te responderé lo antes posible.</p>
    <p class="contact__warning">Los campos marcados como (obligatorio) son necesarios para poder enviar el mensaje. Gracias.</p>
</div>

<form action="https://form.taxi/s/ig60g745" method="POST">
    <div class="contact__field">
        <label for="contact-completename">Nombre y apellidos <span class="contact__required">(obligatorio)</span></label>
        <input type="text" name="contact-completename" id="contact-completename" autocomplete="name" required aria-describedby="contact-error-completename" aria-invalid="false">
        <span id="contact-error-completename" class="contact__error" role="alert">Introduce tu nombre completo, por favor.</span>
    </div>
    <div class="contact__field">
        <label for="contact-companyname">Razón social</label>
        <input type="text" name="contact-companyname" id="contact-companyname" autocomplete="organization">
    </div>
    <div class="contact__field">
        <label for="contact-email">Correo electrónico <span class="contact__required">(obligatorio)</span></label>
        <input type="email" name="contact-email" id="contact-email" autocomplete="email" required aria-describedby="contact-email-hint contact-error-email" aria-invalid="false">
        <span id="contact-email-hint" class="contact__hint">Te responderé a esta dirección de correo.</span>
        <span id="contact-error-email" class="contact__error" role="alert">Introduce un correo electrónico válido, por favor.</span>
    </div>
    <div class="contact__field">
        <label for="contact-subject">Asunto <span class="contact__required">(obligatorio)</span></label>
        <input type="text" name="contact-subject" id="contact-subject" required aria-describedby="contact-error-subject" aria-invalid="false">
        <span id="contact-error-subject" class="contact__error" role="alert">Especifica el asunto para este mensaje, por favor.</span>
    </div>
    <div class="contact__field">
        <label for="contact-message">Mensaje <span class="contact__required">(obligatorio)</span></label>
        <textarea name="contact-message" id="contact-message" required maxlength="1000" aria-describedby="contact-message-hint contact-error-message" aria-invalid="false"></textarea>
        <span id="contact-message-hint" class="contact__hint">Se aplica un límite de 1000 caracteres. Te quedan <span id="contact-charcounter">1000</span> caracteres.</span>
        <span id="contact-error-message" class="contact__error" role="alert">Introduce el cuerpo del mensaje, por favor.</span>
    </div>
    <div class="contact__field contact__legal">
        <input type="checkbox" name="contact-legal" id="contact-legal" required aria-describedby="contact-error-legal" aria-invalid="false">
        <label for="contact-legal" class="contact__legal-label">Marcando esta casilla, aceptas los <a href="{{ site.data.links.legal.notice | relative_url }}">Términos y Condiciones</a> de este sitio, así como el <a href="{{ site.data.links.legal.privacy | relative_url }}">tratamiento de los datos</a> que envías <span class="contact__required">(obligatorio)</span></label>
        <span id="contact-error-legal" class="contact__error contact__error--legal" role="alert">Para poder enviar el mensaje tienes que aceptar los términos y condiciones y el tratamiento de tus datos, por favor.</span>
    </div>
    <div class="contact__buttons">
        <button type="submit" id="contact-submit">Enviar</button>
        <button type="reset" id="contact-reset">Limpiar</button>
    </div>
</form>
{%- include contact-counter.html -%}
{%- include contact-error-messages.html -%}