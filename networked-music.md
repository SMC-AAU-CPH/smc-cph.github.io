---
layout: page
title: Networked Music
permalink: /networked-music/
---

The blog posts of this section relate to the courses [SMC4024 Networked Music Performance Tehcnologies 1](https://www.uio.no/studier/emner/hf/imv/SMC4024) and [SMC4025 Networked Music Performance Tehcnologies 2](https://www.uio.no/studier/emner/hf/imv/SMC4025/) (from 2021), and to the discontinued courses [SMC4021 Physical-Virtual Communication and Music 1](https://www.uio.no/studier/emner/hf/imv/SMC4021/), [SMC4022 Physical-Virtual Communication and Music 2](https://www.uio.no/studier/emner/hf/imv/SMC4022/), and [SMC4023 Physical-Virtual Communication and Music 3](https://www.uio.no/studier/emner/hf/imv/SMC4023/) (2018 to 2021).

These courses aim to provide theoretical and practical knowledge on advanced audio-visual systems for online synchronous musical collaboration and hybrid communication settings. The students also learn to operate, maintain and experiment with the physical-virtual Portal, a laboratory for network-based musical communication.

{%- if site.posts.size > 0 -%}

  <!-- <h2 class="post-list-heading">{{ page.list_title | default: "Posts" }}</h2> -->
  <ul class="post-list">
    {%- for post in site.categories.networked-music -%}

    {%- include list-body.html -%}

    {%- endfor -%}

  </ul>
  {%- endif -%}
