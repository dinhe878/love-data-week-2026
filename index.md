---
layout: page
title: Hej Hei Data Lovers!
menu_title: Home
menu_icon: house-door
---

{:.secondary}
# {{ site.event_date }}, in association with Nordic Universities and Institutions

<div class="aside">
    <h2><i class="bi bi-calendar3"></i> Event timeline</h2>
    <dl>
        {% if site.registration_status == "soon" or site.registration_status == "open" or site.registration_status == "demo" %}
            <dt>{{ site.registration_opens_date }}</dt>
            <dd>
                Registration open for participants<br>
                {% if site.registration_status == 'open' %}
                    <a href="{{ site.baseurl }}{% link registration.md %}" class="btn">Register now</a>
                {% elsif site.registration_status == 'closed' %}
                    <a class="btn disabled">Registration has closed</a>
                {% elsif site.registration_status == 'soon' %}
                    <a class="btn disabled">Registration opens soon</a>
                {% endif %}
            </dd>
        {% endif %}

        <dt>{{ site.registration_closes_date }}</dt>
        <dd>Registration close</dd>

        <dt>{{ site.event_date }}</dt>
        <dd>Nordic Love Data Week</dd>
    </dl>
</div>

{% if site.event_status != "over" %}

This year, for the first time, a Nordic Love Data Week is organized by several Nordic universities. We aim to promote awareness and best practices about research data management, data sharing, and data literacy across the Nordic region.
We have several presentations to offer and also invite you to set aside some time with you research group for the Nordic "Where's the Data Day" on Thursday 12 February.

## When and where

Visit the Agenda page (LINK) to find an online webinar or workshop of interest.
Further, we invite research groups to create their own hands-on events on **Where's the Data Day** (LINK)

## Välkommen! Tervetuloa! Velkommen!

[faq]: {{ site.baseurl }}{% link faq.md %}

{% else %}

Scientists from the University of Bristol hosted a X-day hackathon on
{{ site.event_date }}, open to researchers, to...

Researchers could sign up to [topics ranging from]({{ site.baseurl }}{% link projects.md %})
... to ..., and more. Teams were be led by senior academics from a range of
disciplines at the University of Bristol, but participating researchers could be
from any UK academic institution.

The event took place virtually, using a combination of **video conferencing**
(Zoom) for meetings and seminars, and **discussion forums** (Slack) for ongoing
comms. Data holding and analysis took place on...

{% endif %}
