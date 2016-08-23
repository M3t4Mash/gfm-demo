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

## Related Topics
* [Deployment](deployment.html)

{% if site.doc-troubleshooting %}
<h2 id="doc-troubleshooting">Troubleshooting</h2>
<ul>			
{% for faq in site.doc-troubleshooting %}
  <li>				
	<a href="{{ site.baseurl }}{{ faq.url }}">{{ faq.title }}</a>				
  </li>
{% endfor %}
</ul>
{% endif %}

## Function Test
{% include listCollection.md currCollection="doc_troubleshooting" %}

## Image test
![Millo goes to colleague]({{ site.baseurl }}/doc-images/milo.jpg | width=100)
{% include includeImage file="milo.jpg" caption="Millo goes to colleague" width="100" %}

## Owner
Team Mandala owns this project. For further information get in touch with [StimpyKatz](https://github.com/StimpyKatz)

Rendered at '{{date}}'
