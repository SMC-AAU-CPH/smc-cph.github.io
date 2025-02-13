---
layout: page
title: Sound Programming
permalink: /sound-programming/
---

The blog posts of this section relate to the course [SMC4001 Sound and Music Programming](https://www.uio.no/studier/emner/hf/imv/SMC4001/) (from 2021), and to the discontinued course [SMC4048 Audio Programming](https://web.archive.org/web/20210414104443/https://www.ntnu.edu/studies/courses/SMC4048) (2019 to 2021). This section also includes posts from the _Digital Audio_ and _Scientific Computing_ modules of the discontinued course [SMC4000 Introduction to Music, Communication and Technology](https://web.archive.org/web/20210419143616/https://www.ntnu.edu/studies/courses/SMC4000) (from 2018 to 2020). The aim of these course is to develop audio signal processing and sound design knowledge as well as skills with general-purpose and audio-specific programming.

{%- if site.posts.size > 0 -%}

  <!-- <h2 class="post-list-heading">{{ page.list_title | default: "Posts" }}</h2> -->
  <ul class="post-list">
    {%- for post in site.categories.sound-programming -%}

    {%- include list-body.html -%}

    {%- endfor -%}

  </ul>
{%- endif -%}

<!-- Hack from https://github.com/jekyll/jekyll/issues/2538 -->

{% capture difference %} {{ site.posts | size | minus:1 }} {% endcapture %}

<!-- {% unless difference contains '-' %} -->
<!-- ***No posts... yet.*** -->
 <!-- Your code will now be dependent on page.tags being empty -->
<!-- {% endunless %} -->
