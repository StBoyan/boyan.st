---
layout: page
title: Photography
permalink : /photography/
sidebar_link: true
order: 2
---
<!-- Lightbox plugin JS and CSS sources -->
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/lightbox2/2.10.0/js/lightbox.min.js"></script>
<link href="https://cdnjs.cloudflare.com/ajax/libs/lightbox2/2.10.0/css/lightbox.min.css" rel="stylesheet" />

{% assign gallery_image = site.static_files | where: "gallery_image", true %}
<main class="grid">
{% for image in gallery_image %}
<a href="{{ image.path }}" data-lightbox="gallery" data-title="{{ image.basename }}">
	<img src="{{ site.thumbnail_link }}{{ image.name }}" alt="{{ image.basename }}">
</a>
{% endfor %}
</main>

<script>
    lightbox.option({
      'showImageNumberLabel': false,
      'wrapAround': true
    })
</script>
