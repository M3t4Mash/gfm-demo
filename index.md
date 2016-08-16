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

## Troubleshooting			
{% for faq in site.troubleshooting limit:3 %}
  <li>				
	<a href="{{ faq.url }}">{{ faq.title }}</a>				
  </li>
{% endfor %}

{{ 'Hello world' }}

Site collections: {{site.collections}}

Page url: {{page.url}}

## Owner
Team Mandala owns this project. For further information get in touch with [StimpyKatz](https://github.com/StimpyKatz)
