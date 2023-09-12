---
layout: page
title: Practical
permalink: /practical/
---

You can download the materials of practical classes here . I will try to upload materials prior to their corresponding classes.


<ul id="archive">
{% for prac in site.practical %}
<li class="archiveposturl" style="background: transparent">
<div class="lecture-container">
    {% if prac.thumbnail %}
    <div class="thumbnail">
      <div class="center-cropped" style="margin-top:5px;margin-bottom:5px;background-image: url('{{ prac.thumbnail | prepend: site.baseurl }}');">
        <img src="{{ prac.thumbnail | prepend: site.baseurl }}"/>
      </div>
    </div>
    {% endif %}
    <div class="content">
        <span><a href="#">{{ prac.title }}</a></span><br>

        <strong>tl;dr:</strong> {{ prac.tldr }}
        <br/>
        <strong>
        {% include prac_links.html prac=prac %}
        </strong>
    </div>
</div>
</li>
{% endfor %}
</ul>