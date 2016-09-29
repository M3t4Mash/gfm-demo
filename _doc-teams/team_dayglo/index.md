---
layout: default
title: Team Dayglo Homepage
team: TEAM_NAME
---
{% assign teamName = page.url | split: '/' %}
{{ page.excerpt | replace: '@@@TEAM_NAME@@@', teamName[2] }}
Team name: {{ teamName[2] }}
# Team Dayglo
Well, it glows.
