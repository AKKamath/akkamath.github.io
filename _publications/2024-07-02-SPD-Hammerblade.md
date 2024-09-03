---
title: "Scalable, Programmable and Dense: The HammerBlade Open-Source RISC-V Manycore"
collection: publications
permalink: /publication/ISCA24-SPD-HB
excerpt: "In this paper, we explore HammerBlade, which simultaneously achieves scalability, programmability and density. HammerBlade is a fully open-source RISC-V manycore architecture, which has been silicon-validated with a 2048-core ASIC implementation using a 14/16nm process."
date: 2024-07-02
venue: 'ACM/IEEE 51st Annual International Symposium on Computer Architecture (ISCA)'
shortform: "ISCA '24"
authorlist: "Dai C Jung, Max Ruttenberg, Paul Gao, Scott Davidson, Daniel Petrisko, Kangli Li, <B>Aditya K Kamath</B> et al."
codeurl: 'https://github.com/bespoke-silicon-group/hb_hammerbench'
citation: ""
paperurl: https://www.bsg.ai/papers/HB_ISCA_2024_Camera_Ready_Final.pdf
---
  Existing tiled manycore architectures propose to convert abundant silicon resources into general-purpose parallel processors with unmatched computational density and programmability. However, as we approach 100 K cores in one chip, conventional manycore architectures struggle to navigate three key axes: scalability, programmability, and density. Many manycores sacrifice programmability for density; or scalability for programmability. In this paper, we explore HammerBlade, which simultaneously achieves scalability, programmability and density. HammerBlade is a fully open-source RISC-V manycore architecture, which has been silicon-validated with a 2048-core ASIC implementation using a 14/16nm process. We evaluate the system using a suite of parallel benchmarks that captures a broad spectrum of computation and communication patterns.