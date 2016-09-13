---
layout: default
title: Start page of the gfm demo
---

# Project name
This project provides a service that does something useful. It provides the following features:

* item 1
* item 2
* item 3
* item 4

# Variable Testing
owner_name: '{{site.github.owner_name}}'
repository_name: '{{site.github.repository_name}}'
repository_nwo: '{{site.github.repository_nwo}}'


## Related Topics
* [Deployment](deployment.html)

{% include listCollection collection="doc-troubleshooting" %}

{% include listCollection collection="doc-interfaces" %}

## Image test
{% include addImage file="milo.jpg" caption="Milo goes to college" width="100" %}

## Collection Tester
{% assign distinctTeamUris = '' | split: ',' %}
{% assign teamPages = site.doc-teams | sort: 'relative_path' %}

{% for page in teamPages %}
 {% assign currUrl = page.relative_path | split: "/" %}
 {% assign currTeam = currUrl[1] %}
 {% unless currTeam == previous %}
  {% assign currTeamLabel = currTeam | split: "_" %}
  {% capture headingLabel %}{% for word in currTeamLabel %}{{ word | capitalize }} {% endfor %}{% endcapture %}
  {% assign newUri = currUrl[0] | append: '/' | append: currUrl[1] %}
  {% assign distinctTeamUris = distinctTeamUris | push: currTeam %}
  <h2 id="{{ currTeam }}">{{ headingLabel }}</h2>  
 {% endunless %}
 {% if currTeam == previous or currTeam == '' %}
   {% if currTeam.size > 3 %}
   <li>
   <a href="{{ site.baseurl }}{{ page.url }}">{{ page.title }}</a>		
   </li>
   {% endif %}
 {% endif %}
 {% assign previous = currTeam %}
{% endfor %}


## Owner
Team Mandala owns this project. For further information get in touch with [StimpyKatz](https://github.com/StimpyKatz)