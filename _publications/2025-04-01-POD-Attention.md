---
title: 'POD-Attention: Unlocking Full Prefill-Decode Overlap for Faster LLM Inference'
collection: publications
permalink: /publication/ASPLOS25-POD-Attention
excerpt: 'In this paper, we present POD-Attention --- the first GPU kernel that efficiently computes attention for hybrid-batch LLM inference. POD-Attention maximizes the utilization of both compute and memory bandwidth by carefully allocating GPU resources such that prefill and decode operations happen concurrently on the same multiprocessor.POD-Attention speeds up attention computation by up to $59\%$ (mean $28\%$), enabling higher throughput and lower latency LLM inference.'
date: 2025-04-01
venue: 'ACM 30th International Conference on Architectural Support for Programming Languages and Operating Systems (ASPLOS)'
shortform: "ASPLOS '25"
authorlist: "<B>Aditya K Kamath</B>, Ramya Prabhu, Jayashree Mohan, Simon Peter, Ramachandran Ramjee, Ashish Panwar"
paperurl: '/files/ASPLOS25_POD.pdf'
award: 'Distinguished Artifact Award'
videourl: 'https://www.youtube.com/watch?v=LZQIvxjdOQw'
videoembed: '<iframe width="966" height="543" src="https://www.youtube.com/embed/LZQIvxjdOQw" title="[ASPLOS 2025] POD-Attention: Unlocking Full Prefill-Decode Overlap for Faster LLM Inference" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>'
codeurl: 'https://github.com/microsoft/vattention/tree/main/pod_attn'
slideurl: '/files/ASPLOS25_POD.pptx'
bibtex: "
@INPROCEEDINGS {POD:ASPLOS:2025,
author = {Kamath, Aditya K and Prabhu, Ramya and Mohan, Jayashree and Peter, Simon and Ramjee, Ramachandran and Panwar, Ashish},
title = {POD-Attention: Unlocking Full Prefill-Decode Overlap for Faster LLM Inference},
year = {2025},
isbn = {9798400710797},
publisher = {Association for Computing Machinery},
address = {New York, NY, USA},
url = {https://doi.org/10.1145/3676641.3715996},
doi = {10.1145/3676641.3715996},
booktitle = {Proceedings of the 30th ACM International Conference on Architectural Support for Programming Languages and Operating Systems, Volume 2},
pages = {897–912},
numpages = {16},
keywords = {Large language models; GPUs; self-attention},
location = {Rotterdam, Netherlands},
series = {ASPLOS 2025}
}
"
---
Each request in LLM inference goes through two phases: compute-bound <em>prefill</em> and memory-bandwidth-bound <em>decode</em>. To improve GPU utilization, recent systems use hybrid batching that combines the prefill and decode phases of different requests into the same batch. This approach optimizes linear operations but remains inefficient for attention computation because <em>existing attention kernels specialize execution independently for the prefill and decode phases</em>.

In this paper, we present POD-Attention --- the first GPU kernel that efficiently computes attention for hybrid batches. POD-Attention aims to maximize the utilization of both compute and memory bandwidth by carefully allocating the GPU's resources such that prefill and decode operations happen concurrently on the same multiprocessor.
POD-Attention speeds up attention computation by up to $59\%$ (mean $28\%$), enabling higher throughput and lower latency LLM inference compared to the use of independently optimized prefill and decode attention kernels.
