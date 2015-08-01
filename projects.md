---
layout: page
---

{% include github_plug.html %}
<div class="posts">
  <h2>Work</h2>
  <hr style="background:#eee; border:0; height:4px" />
  {% assign projects = site.work| sort: 'date' | reverse %}
  {% for project in projects %}
  <div class="post">
    <h3 class="post-title">
        {{ project.title }}
    </h3>
    <h5> <span> {{ project.duration }} </span> <span>{{ project.location }} </span></h5>
    <hr>
    {{ project.content }}
  </div>
  {% endfor %}

  <h2>Projects</h2>
  <hr style="background:#eee; border:0; height:4px" />
  {% assign projects = site.projects| sort: 'date' | reverse %}
  {% for project in projects %}
  <div class="post">
    <h3 class="post-title">
        <a href="{{ project.link }}">{{ project.title }}</a>
    </h3>
    <h5> <span> {{ project.duration }} </span>
    <hr>
    {{ project.content }}
    <a href="{{ project.repo }}"><h6>Source Code</h6></a>
  </div>
  {% endfor %}


</div>