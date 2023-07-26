---
title: "Herding LLaMaS: Using LLMs as an OS Module"
collection: talks
type: "Talk"
permalink: /talks/ASPLOS23_WACI-LLaMaS
authorlist: "<B>Aditya K Kamath*</B> and Sujay Yadalam*<br>(*Authors contributed equally to this work)"
venue: "ASPLOS 2023, Wild and Crazy Ideas Session"
date: 2023-03-25
location: "Vancouver, Canada"
paperurl: '/files/ASPLOS23-WACI_LLaMaS.pdf'
videourl: 'https://www.youtube.com/watch?v=U4_0PmbEYSY'
videoembed: '<iframe width="873" height="491" src="https://www.youtube.com/embed/U4_0PmbEYSY" title="[ASPLOS 2023 WACI] Herding LLaMaS: Using LLMs as an OS Module" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>'
---

Sujay and I found ourselves chatting about the future of research one day. It was around this time that an explosion of interest in Large Language Models (LLMs) had started, sparked by the release of ChatGPT by OpenAI. Our discussion inevitably veered towards this topic, and we became curious about how LLMs could revolutionize the field of operating systems. 

Our brainstorming led us to an intriguing idea: leveraging LLMs to enhance the decision-making of operating systems when confronted with a growing heterogeneity of devices. These decisions could range from selecting the most suitable memory device to place data in, to effectively scheduling processes on different compute devices. In the past this required a customized solution for every type of system, like Non-Uniform Memory [[1](https://doi.org/10.1145/3373376.3378468), [2](https://doi.org/10.1145/2451116.2451157), [3](https://doi.org/10.1145/3445814.3446709)], systems with GPUs [[4](https://doi.org/10.1145/2694344.2694381), [5](https://doi.org/10.1145/3123939.3123975)], or NVM/CXL memory [[6](https://doi.org/10.1145/3575693.3578835), [7](https://doi.org/10.1145/3582016.3582063), [8](https://doi.org/10.1145/3477132.3483550), [9](https://doi.org/10.
1145/3297858.3304024)]

Instead of tailoring these solutions to specific devices we envisioned that LLMs could act as an intermediary layer. The system administrator would provide the LLM with specific details about the new devices contained in the system. The LLM would then provide guidance and hints to the operating system about how to manage these devices. 

We performed some feasibility tests using ChatGPT and found it to be quite reliable. We eventually documented everything in the form of a talk which I presented at ASPLOS 2023's Wild and Crazy Ideas Session.