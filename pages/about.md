---
layout: page
title: About
permalink: /about/
weight: 3
---

# **About Me**

Hi I am **{{ site.author.name }}**,<br>
I'm an Information Sciences major at University of Illinois Urbana-Champaign.<br>
I'm currently pursuing a Bachelor's degree and am planning on pursuing a Master's <br>
once I graduate. I do data science, music, game design, and other computer-related <br>
hobbies.


<div class="row">
{% include about/skills.html title="Programming Skills" source=site.data.programming-skills %}
{% include about/skills.html title="Other Skills" source=site.data.other-skills %}
</div>

<div class="row">
{% include about/timeline.html %}
</div>
