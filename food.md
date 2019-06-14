---
title: Food
date: 2019-05-31 13:41:00 +02:00
position: 2
Field name:
layout: home
menu: true
---

# Eat your heart out

{% for burger_hash in site.data.burgers %}
{% assign burgers = burger_hash[1] %}

<h2>{{burgers.name}}</h2>
<p>{{burgers.description}}</p>
{% for burger in burgers.items %}
<h3>{{burger.name}} <span>({{burger.info}})</span> <strong>{{burger.price}}kr</strong></h3>
<p>{{burger.description}}</p>
{% endfor %}

{% endfor %}
