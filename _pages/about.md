---
permalink: /
title: "My homepage"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Heya! I'm a Ph.D. student at the University of Washington's Paul G Allen School of Computer Science and Engineering advised by [Professor Simon Peter](https://homes.cs.washington.edu/~simpeter/). I enjoy building high-performance software tailored to efficiently utilise underlying architectures/systems.

Prior to this, I spent two years as a research assistant at the Indian Institute of Science, working with [Professor Arkaprava Basu](https://www.csa.iisc.ac.in/~arkapravab/). Here, I worked on improving race detection in GPUs [[ISCA '20](https://dl.acm.org/doi/10.1109/ISCA45697.2020.00088), [SOSP '21](https://dl.acm.org/doi/10.1145/3477132.3483545)], and improving GPU performance through the use of NVM technology [[ASPLOS '22](https://dl.acm.org/doi/abs/10.1145/3503222.3507758), ['23](https://dl.acm.org/doi/10.1145/3575693.3575749)].

I try to weightlift every weekday, and I'm always on the lookout for workout buddies. If you're at UW and love pumping iron as much as I do, please hit me up!

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
(*Authors contributed equally to this work)