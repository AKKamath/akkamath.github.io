---
permalink: /
title: "Homepage"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Heya! I'm a Ph.D. student at the University of Washington's Paul G Allen School of Computer Science and Engineering advised by [Professor Simon Peter](https://homes.cs.washington.edu/~simpeter/). 
My current work revolves around analyzing data movement and mitigating its performance impact in contemporary applications [[ISCA '24](/publication/ISCA24-MCSquare)]. 
I hope to explore this problem across the stack from the single-node architectural level to multi-machine distributed systems.

There are three main axes by which I'm doing this:     
1) Avoiding (unnecessary) data movement,     
2) Reducing (necessary) data movement, and     
3) Hiding the overheads of data movement by overlapping it with other operations.


Prior to this, I spent two years as a research assistant at the Indian Institute of Science, working with [Professor Arkaprava Basu](https://www.csa.iisc.ac.in/~arkapravab/). Here, I worked on improving race detection in GPUs [[ISCA '20](https://dl.acm.org/doi/10.1109/ISCA45697.2020.00088), [SOSP '21](https://dl.acm.org/doi/10.1145/3477132.3483545)], and improving GPU performance through the use of NVM technology [[ASPLOS '22](https://dl.acm.org/doi/abs/10.1145/3503222.3507758), ['23](https://dl.acm.org/doi/10.1145/3575693.3575749)].

I try to weightlift every weekday, and I'm always on the lookout for workout buddies. If you're at UW and love pumping iron as much as I do, please hit me up!

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>

<p class="divider__line"></p>
Still here? Curious to see what first contact with aliens might look like? <br>
Check out this talk I gave at the ASPLOS 2023 "Wild and Crazy Ideas" session:
<iframe width="950" height="534" src="https://www.youtube.com/embed/U4_0PmbEYSY" title="[ASPLOS 2023 WACI] Herding LLaMaS: Using LLMs as an OS Module" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>