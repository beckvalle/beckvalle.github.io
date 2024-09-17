---
layout: page
permalink: /edu_demo/
title: I-GUIDE Platform Educational Resources Demo
description:
nav: false
---

A few examples of how educational resources for the I-GUIDE platform might look.

{% for map in site.data.maps %}
* [{{map.title}}](#{{map.authors}})
{% endfor %}


{% for map in site.data.maps %}
***
<h2 id="{{map.authors}}">{{ map.title }}</h2>
<p>{{ map.authors }}</p>

<b>Description</b>
<p>{{map.description}}</p>

{% if map.link %}
*Below is a preview of the map, you can access the map at* <a href="{{map.link}}" target="_blank">{{map.link}}</a>
<iframe width="100%" height="500" src="{{map.link}}"></iframe>
{% endif %}

<img width="100%" src="{{map.image}}" />

{% endfor %}