---
layout: page
title:  "Les lieux où tout se joue"
subtitle: "Où voir de l'impro ? Où pratiquer ?"
categories: annuaires
permalink: /lieux/
thumbnail: assets/icons/theater.svg
---

## Les lieux

{% for item in site.data.theaters %}
### {{ item.name }} ({{ item.city }})
{{ item.desc }}

<img src="{{ baseurl }}/assets/images/theaters/{{ item.img }}" alt="{{ item.name }}">

{% if item.website %}
<img src="{{ 'assets/icons/web.svg' | relative_url }}" width="24" alt="Site web">
<a href= '{{ item.website }}'>{{ item.website | replace: "https://", ""  | replace: "http://", "" }}</a>
{% endif %}
{% if item.tickets contains "https://" or item.tickets contains "http://" %}
<img src="{{ 'assets/icons/tickets.svg' | relative_url }}" width="24" alt="Billetterie">
Réservations : <a href= '{{ item.tickets }}'>{{ item.tickets | replace: "https://", ""  | replace: "http://", "" }}</a>
{% elsif item.tickets %}
<img src="{{ 'assets/icons/tickets.svg' | relative_url }}" width="24" alt="Billetterie">
{{ item.tickets }}
{% endif %}
{% if item.address and item.map %}
<img src="{{ 'assets/icons/address-marker.svg' | relative_url }}" width="24" alt="Adresse">
<a href='{{ item.map }}'>{{ item.address }}</a>
{% elsif item.address %}
<img src="{{ 'assets/icons/address-marker.svg' | relative_url }}" width="24" alt="Adresse">
{{ item.address }}
{% elsif item.map %}
<img src="{{ 'assets/icons/address-marker.svg' | relative_url }}" width="24" alt="Localisation">
<a href='{{ item.map }}'>S'y rendre</a> !
{% endif %}
{% if item.phone %}
<img src="{{ 'assets/icons/phone.svg' | relative_url }}" width="24" alt="Téléphone">
{{ item.phone }} (sans abuser ;)
{% endif %}

{% endfor %}

### La carte interactive
<a href='https://goo.gl/maps/ccHyyk1zZEEi2yGH9'><img src="{{ 'assets/images/carte-interactive.png' | relative_url }}" alt="Carte interactive"></a>

### Pas dans la liste ???
N'hésite pas à [nous contacter]('contact'  | relative_url ) pour combler ce vide immense.