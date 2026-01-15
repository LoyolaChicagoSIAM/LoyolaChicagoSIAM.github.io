---
layout: page
title: Officers 
permalink: /officers/
---

<style type="text/css">
    .container {
        display: grid; 
        grid-template-columns:  1fr 1fr;
        grid-gap: 10px; 
        padding-bottom: 4em;
    }

    .box {
        padding: 5px;
    }

    .imagestyle { 
        max-width: 100%;
        max-height: 100%;
    }

    .contentstyle {
        padding-left: 20px; 
    }

    .image {
        object-fit: scale-down;
        max-width: 100%;
        border: 5px solid #444;
        border-radius: 10px; 
    }

    .name {
        color: #353839;
        font-size: 140%;
    }
</style>

<div class="container"> 
{% for officer in site.officers %}
    {% if officer.status == "active" and officer.position == "President" %}
        <div class="box">
            <img class="image" src="{{ officer.image }}" alt="{{ officer.name }} image"> 
        </div>
        <div class="contentstyle">
            <h2> {{ officer.position }} </h2>
            <p class="name"> {{ officer.name }} <br>
                <a class="u-email" href="mailto:{{ officer.contact }}">
                    {{ officer.contact }} 
                </a>
            </p>
            <p>{{ officer.content | markdownify }}</p>
        </div>
    {% endif %}
{% endfor %}

{% for officer in site.officers %}
    {% if officer.status == "active" and officer.position == "Vice President" %}
        <div class="box">
            <img class="image" src="{{ officer.image }}" alt="{{ officer.name }} image"> 
        </div>
        <div class="contentstyle">
            <h2> {{ officer.position }} </h2>
            <p class="name"> {{ officer.name }} <br>
            <a class="u-email" href="mailto:{{ officer.contact }}">
                {{ officer.contact }} 
            </a>
            </p>
            <p>{{ officer.content | markdownify }}</p>
        </div>
    {% endif %}
{% endfor %}

{% for officer in site.officers %}
{% if officer.status == "active" and officer.position == "Treasurer" %}
    <div class="box">
        <img class="image" src="{{ officer.image }}" alt="{{ officer.name }} image"> 
    </div>
    <div class="contentstyle">
        <h2> {{ officer.position }} </h2>
        <p class="name"> {{ officer.name }} <br>
        <a class="u-email" href="mailto:{{ officer.contact }}">
            {{ officer.contact }} 
        </a>
        </p>
        <p>{{ officer.content | markdownify }}</p>
    </div>
{% endif %}
{% endfor %}
</div>

<div class="container"> 
{% for advisor in site.advisors %}
    <div class="box">
        <img class="image" src="{{ advisor.image }}" alt="{{ advisor.name }} image"> 
    </div>
    <div class="contentstyle">
        <h2> Faculty Advisor </h2>
        <p class="name"> {{ advisor.name }}
            <a class="u-email" href="mailto:{{ advisor.contact }}"> <br>
            {{ advisor.contact }} 
            </a>
        </p>
    </div>
{% endfor %}
</div>
