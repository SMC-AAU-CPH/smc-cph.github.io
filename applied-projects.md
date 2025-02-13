---
layout: page
title: Applied Projects
permalink: /applied-projects/
---

The blog posts of this section relate to the course [SMC4033 Applied SMC Project](https://www.uio.no/studier/emner/hf/imv/SMC4033) (2022 onwards) and to the discontinued courses [SMC4031 Applied SMC Project 1](https://www.uio.no/studier/emner/hf/imv/SMC4031) and [SMC4032 Applied SMC Project 2](https://web.archive.org/web/20210419164338/https://www.ntnu.edu/studies/courses/SMC4032) (2019 to 2021). The aim of these courses is to carry out a music technological project in a real-world setting with an external partner or stakeholder. The project should have a societal, research or industrial impact. The problem at hand could be of a non-musical nature requiring students to apply their music-technological knowledge in new and creative ways.

{%- if site.posts.size > 0 -%}

  <!-- <h2 class="post-list-heading">{{ page.list_title | default: "Posts" }}</h2> -->
  <ul class="post-list">
    {%- for post in site.categories.applied-project -%}

    {%- include list-body.html -%}

    {%- endfor -%}

  </ul>
  {%- endif -%}
