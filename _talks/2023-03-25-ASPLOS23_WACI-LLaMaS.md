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

Our brainstorming led us to an intriguing idea: leveraging LLMs to enhance the decision-making of operating systems when confronted with a growing heterogeneity of devices. Imagine you have a system with a new type of memory that can give you amazing performance when reading from the device, but terrible performance when writing to the device. To get the best performance from your programs, you'd need to rewrite every application, manually keeping data that is heavily read from but rarely written to in this new type of memory. This just isn't practical.

Instead, you can add a new component to the operating system which decides which program data to keep in which memory. This is what's done today. The operating system makes all the hardware-dependent decisions for the program so that it doesn't have to be rewritten for every type of device. These decisions could range from selecting the most suitable memory device to place data in to effectively scheduling processes on different types of compute devices. This requires a customized solution for every type of system, e.g. Non-Uniform Memory [[1](https://doi.org/10.1145/3373376.3378468), [2](https://doi.org/10.1145/2451116.2451157), [3](https://doi.org/10.1145/3445814.3446709)], systems with GPUs [[4](https://doi.org/10.1145/2694344.2694381), [5](https://doi.org/10.1145/3123939.3123975)], NVM [[6](https://doi.org/10.1145/3477132.3483550), [7](https://doi.org/10.
1145/3297858.3304024)], or CXL memory [[8](https://doi.org/10.1145/3575693.3578835), [9](https://doi.org/10.1145/3582016.3582063)].

Instead of tailoring these solutions to specific systems, we envisioned that LLMs could act as an intermediary layer. The system administrator would provide the LLM with specific details about all the devices contained in the system. The LLM would then provide guidance and hints to the operating system about how to manage these devices. Any time a new device is added to the system, we only have to inform the LLM about it; no OS modifications are needed.

We performed some feasibility tests using ChatGPT and found it to be quite reliable. We eventually documented everything in the form of a talk which I presented at ASPLOS 2023's Wild and Crazy Ideas Session.