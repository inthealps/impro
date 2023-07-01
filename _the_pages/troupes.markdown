---
layout: page
title:  "Annuaires des troupes"
subtitle: "Les troupes et compagnies d'impro sur l'agglo"
categories: annuaires
permalink: /troupes/
thumbnail: assets/icons/people.svg
---

## Les troupes

Liste non exhaustive des troupes d'impro sur l'agglo grenôbloaze.

{% for item in site.data.companies %}

{% if item.isPro == true %}
### {{ item.name }} (pros)
{% else %}
### {{ item.name }} (amateurs)
{% endif %}
{{ item.desc }}

<img src="{{ site.baseurl }}/assets/images/companies/{{ item.img }}" alt="{{ item.name }}">

{% if item.instagram %}
<img src="{{ 'assets/icons/instagram.svg' | relative_url }}" width="24" alt="Instagram">
<a href= '{{ item.instagram }}' target="_blank">{{ item.instagram | replace: "https://", ""  | replace: "http://", "" }}</a>
{% endif %}
{% if item.facebook %}
<img src="{{ 'assets/icons/facebook.svg' | relative_url }}" width="24" alt="Facebook">
<a href= '{{ item.facebook }}' target="_blank">{{ item.facebook | replace: "https://", ""  | replace: "http://", "" }}</a>
{% endif %}
{% if item.twitter %}
<img src="{{ 'assets/icons/twitter.svg' | relative_url }}" width="24" alt="Twitter">
<a href= '{{ item.twitter }}' target="_blank">{{ item.twitter | replace: "https://", ""  | replace: "http://", "" }}</a>
{% endif %}
{% endfor %}

### etc ...
Description à faire ...

### Pas dans la liste ???
N'hésite pas à [nous contacter](/contact) pour combler ce vide immense.