---
layout: default
profile: home
permalink: /contact/
title: Contact
lang: en
---

<div class="contact__introduction">

    <p>I'm glad you want to get in touch.</p>
    <p>Tell me about your query or proposal using the form and I'll reply as soon as I can.</p>
    <p class="contact__warning">The fields marked (required) are needed to send the message. Thank you.</p>
</div>

<form action="https://form.taxi/s/79o0c517" method="POST">
    <div class="contact__field">
        <label for="contact-completename">Full name <span class="contact__required">(required)</span></label>
        <input type="text" name="contact-completename" id="contact-completename" autocomplete="name" required aria-describedby="contact-error-completename" aria-invalid="false">
        <span id="contact-error-completename" class="contact__error" role="alert">Please enter your full name.</span>
    </div>
    <div class="contact__field">
        <label for="contact-companyname">Company name</label>
        <input type="text" name="contact-companyname" id="contact-companyname" autocomplete="organization">
    </div>
    <div class="contact__field">
        <label for="contact-email">Email address <span class="contact__required">(required)</span></label>
        <input type="email" name="contact-email" id="contact-email" autocomplete="email" required aria-describedby="contact-email-hint contact-error-email" aria-invalid="false">
        <span id="contact-email-hint" class="contact__hint">I'll reply to this email address.</span>
        <span id="contact-error-email" class="contact__error" role="alert">Please enter a valid email address.</span>
    </div>
    <div class="contact__field">
        <label for="contact-subject">Subject <span class="contact__required">(required)</span></label>
        <input type="text" name="contact-subject" id="contact-subject" required aria-describedby="contact-error-subject" aria-invalid="false">
        <span id="contact-error-subject" class="contact__error" role="alert">Please specify the subject of your message.</span>
    </div>
    <div class="contact__field">
        <label for="contact-message">Message <span class="contact__required">(required)</span></label>
        <textarea name="contact-message" id="contact-message" required maxlength="1000" aria-describedby="contact-message-hint contact-error-message" aria-invalid="false"></textarea>
        <span id="contact-message-hint" class="contact__hint">There is a limit of 1000 characters. You have <span id="contact-charcounter">1000</span> characters left.</span>
        <span id="contact-error-message" class="contact__error" role="alert">Please enter your message.</span>
    </div>
    <div class="contact__field contact__legal">
        <input type="checkbox" name="contact-legal" id="contact-legal" required aria-describedby="contact-error-legal" aria-invalid="false">
        <label for="contact-legal" class="contact__legal-label">By checking this box, you accept the <a href="{{ site.data.links.legal.notice | relative_url }}">Terms and Conditions</a> of this site, and the <a href="{{ site.data.links.legal.privacy | relative_url }}">processing of your data</a> you are sending me <span class="contact__required">(required)</span>.</label>
        <span id="contact-error-legal" class="contact__error contact__error--legal" role="alert">To send the message, you must accept the terms and conditions and the processing of your data.</span>
    </div>
    <div class="contact__buttons">
        <button type="submit" id="contact-submit">Send</button>
        <button type="reset" id="contact-reset">Reset</button>
    </div>
</form>
{%- include contact-counter.html -%}
{%- include contact-error-messages.html -%}