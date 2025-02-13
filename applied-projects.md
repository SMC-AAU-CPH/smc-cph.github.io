---
layout: page
title: Semester Projects
permalink: /applied-projects/
---
The blog posts of this section relate to the 15 ECTS semester projects in SMC7-9. The aim of these projects is to carry out a sound and music technological project in a real-world problem-based setting. The projects should have a societal, research or industrial impact. 

In Spring 2025, the project themes relate to the brief given by Roskilde Festival (RF): in two main groups: INCLUSION or FIRST DAYS:

# INCLUSION: ACCESSIBILITY, EQUALITY, DIVERSITY

Roskilde Festival has a strong focus on social sustainability and on being an inclusive and diverse festival where people can meet across differences. How can RF become an inviting, including, and open community, welcoming people whatever their functional capability?

* How can we improve the accessibility of toilets and bathing facilities (design, location, etc.)?
* How can the first encounter and arrival at the festival become a pleasant and safe experience?
* How can we reach out to people with disabilities who may be reluctant to participate in festivals?
* How can we design content and appearance of meeting points at the festival addressing diversity, equality, and accessibility?
* Games and activities for HandiCamp that encourage people to meet and facilitate dialogue and interaction between participants in a respectful, funny, and thoughtful manner.
* The accessible tent platform. At our camping facilities, we want to meet the different needs of participants with disabilities.

# FIRST DAYS: JOINING PEOPLE TOGETHER, MAKING A DIFFERENCE

We are interested in activities which can contribute to fun and new friendships among the participants at the campsite, and which further address our agendas on environmental, social, economic, and cultural sustainability development. We see arts and culture as driving forces in circular development.

- Design and testing of experimental experiences, in which co-creation as well as arts and culture in a broad sense encourage to reflect on circularity and sustainability. Arts and culture can be, for example architecture, technology, and social intervention. Sustainability is seen in a broad sense, i.e. social, environmental, economic, and cultural aspects. Solutions can be specific technical designs, process-oriented courses, games, workshops, etc.
- Relaxation and activities in a funny and respectful manner. We often find that after a few days at the campsite, the participants are interested in activities to gather around which only require the gear already present in the camp. Further, we are interested in activities which do not necessarily require alcohol as a central element

{%- if site.posts.size > 0 -%}

<!-- <h2 class="post-list-heading">{{ page.list_title | default: "Posts" }}</h2> -->

<ul class="post-list">
    {%- for post in site.categories.applied-project -%}

    {%- include list-body.html -%}

    {%- endfor -%}

</ul>
  {%- endif -%}
