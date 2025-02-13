---
layout: page
title: New Interfaces for Musical Expression
permalink: /interactive-music/
---
The blog posts of this section relate to the course New Interfaces for Musical Expression (2014-2025) and Mobile and Wearable Computing (2023 onwards). The aim of these courses is to develop knowledge of and practical experience with the design and implementation of systems intended for real-time sonic or musical interaction. This could be in the form of a performance-oriented musical instrument, or in various types of interactive sonic systems that explore collaborative physical, or virtual music-making. 

{%- if site.posts.size > 0 -%}

<!-- <h2 class="post-list-heading">{{ page.list_title | default: "Posts" }}</h2> -->

<ul class="post-list">
    {%- for post in site.categories.interactive-music -%}

    {%- include list-body.html -%}

    {%- endfor -%}

</ul>
  {%- endif -%}
