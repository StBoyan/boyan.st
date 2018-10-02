---
layout: page
title: Projects
permalink : /projects/
order: 1
---

I try to keep myself busy with projects and I am always looking for something to
build in order to widen my programming skillset. Here you can find some of the
projects I have done. I will be adding more in the future!

<div id="project">
{% assign projects = site.projects | sort: 'order' | reverse%}
{% for project in projects %}
  <a href="{{ project.url }}">
    <figure>
      <img src="{{ site.projects_thumbnail_link }}{{ project.thumbnail }}" width="100px" height="100px"/>
      <figcaption>{{ project.title }}</figcaption>
    </figure>
  </a>
{% endfor %}
</div>
