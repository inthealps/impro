---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

{% for page in site.the_pages limit:5 %}
<article class="post-preview">
<a href="{{ site.baseurl }}/{{ page.url }}">
<h3 class="post-title"><img src="{{ site.baseurl }}/{{ page.thumbnail }}" width="48" alt="{{ page.title }}"> {{ page.title }}</h3>
<h4 class="post-subtitle">{{ page.subtitle }}</h4>
</a>
</article>
<hr>
{% endfor %}