---
layout: container
title: About
---
{% assign me = site.data.pagelist.pages | where: 'title', page.title | first %}  
# {{ me.title }}

{{ me.intro }}