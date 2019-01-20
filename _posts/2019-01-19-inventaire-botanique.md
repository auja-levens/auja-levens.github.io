---
title:  Inventaire botanique
categories: [site]

public-bucket-url: https://storage.googleapis.com/auja-public
photos-dir: inventaire-botanique
photos:
  - { title: 'Genêt', filename: '3.png' }
  - { title: 'Curabitur vestibulum', filename: '1.png'}
  - { title: 'Sed diam.', filename: '2.png' }

  - { title: 'Aenean vehicula purus', filename: '4.png' }
  - { title: 'Liseron', filename: '5.png' }

---

<link href="/assets/css/vendor/flexbin.css" type="text/css" rel="stylesheet" media="all" />

# Inventaire botanique

Page d'origine [ici](http://88.140.148.15/auja/jardins-inventaire1.htm)

---

## Système de "cartes"

Imparfait, l'idéal serait d'avoir des photos de même dimension + rotation.

Ici, j'ai mis celles en mode paysage à la fin.

<main class="cards">
{% for photo in page.photos %}
<div class="card">
  <a href="{{ page.public-bucket-url }}/{{ page.photos-dir }}/{{ photo.filename }}">
    <img src="{{ page.public-bucket-url }}/{{ page.photos-dir }}/{{ photo.filename }}" alt="{{ photo.title }}">
  </a>
  <div class="card-title">{{ photo.title }}</div>
</div>
{% endfor %}
</main>

---

## Flexbin

Pourrait être utile pour afficher des photos en vrac

<div class="flexbin">
	{% for photo in page.photos %}
		<a href="{{ page.public-bucket-url }}/{{ page.photos-dir }}/{{ photo.filename }}">
      <img src="{{ page.public-bucket-url }}/{{ page.photos-dir }}/{{ photo.filename }}" />
		</a>
	{% endfor %}
</div>
