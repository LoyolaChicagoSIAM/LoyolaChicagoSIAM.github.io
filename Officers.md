---
layout: page
title: Officers
permalink: /officers/
---

<div class="officers-grid">
{% for officer in site.officers %}
    {% if officer.status == "active" and officer.position == "President" %}
    <div class="officer-card">
        <img class="officer-image" src="{{ officer.image }}" alt="{{ officer.name }}">
        <div class="officer-content">
            <h3>{{ officer.position }}</h3>
            <p class="officer-name">{{ officer.name }}</p>
            <a class="officer-email" href="mailto:{{ officer.contact }}">{{ officer.contact }}</a>
            <div class="officer-bio">{{ officer.content | markdownify }}</div>
        </div>
    </div>
    {% endif %}
{% endfor %}

{% for officer in site.officers %}
    {% if officer.status == "active" and officer.position == "Vice President" %}
    <div class="officer-card">
        <img class="officer-image" src="{{ officer.image }}" alt="{{ officer.name }}">
        <div class="officer-content">
            <h3>{{ officer.position }}</h3>
            <p class="officer-name">{{ officer.name }}</p>
            <a class="officer-email" href="mailto:{{ officer.contact }}">{{ officer.contact }}</a>
            <div class="officer-bio">{{ officer.content | markdownify }}</div>
        </div>
    </div>
    {% endif %}
{% endfor %}

{% for officer in site.officers %}
    {% if officer.status == "active" and officer.position == "Treasurer" %}
    <div class="officer-card">
        <img class="officer-image" src="{{ officer.image }}" alt="{{ officer.name }}">
        <div class="officer-content">
            <h3>{{ officer.position }}</h3>
            <p class="officer-name">{{ officer.name }}</p>
            <a class="officer-email" href="mailto:{{ officer.contact }}">{{ officer.contact }}</a>
            <div class="officer-bio">{{ officer.content | markdownify }}</div>
        </div>
    </div>
    {% endif %}
{% endfor %}
</div>

<h2 class="section-heading">Faculty Advisors</h2>

<div class="officers-grid">
{% for advisor in site.advisors %}
    <div class="officer-card">
        <img class="officer-image" src="{{ advisor.image }}" alt="{{ advisor.name }}">
        <div class="officer-content">
            <h3>Faculty Advisor</h3>
            <p class="officer-name">{{ advisor.name }}</p>
            <a class="officer-email" href="mailto:{{ advisor.contact }}">{{ advisor.contact }}</a>
        </div>
    </div>
{% endfor %}
</div>
