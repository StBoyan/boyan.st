---
layout: page
title: Photography
permalink : /photography/
order: 2
---
<!-- Lightbox plugin JS and CSS sources -->
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/lightbox2/2.10.0/js/lightbox.min.js"></script>
<link href="https://cdnjs.cloudflare.com/ajax/libs/lightbox2/2.10.0/css/lightbox.min.css" rel="stylesheet" />

I have always enjoyed photography and snapping pictures with my phone. Though, I
never realised how limited a phone's camera is until about a year ago, when I finally
decided to take my hobby to the next level. I got a **Sony A6000** mirorrless camera with a
*16-50mm kit lens* that opened an entirely new world of photography for me. Nowadays, I also
have a *Yashica ML 50mm f/1.9* vintage lens and am looking forward to acquiring a 35mm lens too.
Here are some of the photos I have taken with my camera with more to come! <br/><br/>

{% assign gallery_image = site.static_files | where: "gallery_image", true %}
<main class="grid">
{% for image in gallery_image %}
<a href="{{ image.path }}" data-lightbox="gallery" data-title="{{ image.basename }}">
	<img src="{{ site.gallery_thumbnail_link }}{{ image.name }}" alt="{{ image.basename }}">
</a>
{% endfor %}
</main>

<script>
    lightbox.option({
      'showImageNumberLabel': false,
      'wrapAround': true
    })
</script>
