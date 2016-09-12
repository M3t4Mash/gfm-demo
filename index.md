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
{% for i in site.doc-teams %}
{% assign currUrl = i.relative_path | split: "/" %}
  <li>				
	<a href="{{ site.baseurl }}{{ i.url }}">{{ i.title }} {{ currUrl[ {{ currUrl | size }} - 1] }}</a>				
  </li>
{% endfor %}

## Owner
Team Mandala owns this project. For further information get in touch with [StimpyKatz](https://github.com/StimpyKatz)