---
title: "*InsideOut: Measuring and Mitigating Insider–Outsider Bias in Interview Script Generation"
collection: publications
Authors: '<b>Yixin Wan</b>, Xingrun Chen, Kai-Wei Chang'
date: 07/2026
venue: 'ACL'
excerpt: ''
presentationurl: ''
paperurl: 'https://aclanthology.org/2026.acl-long.1094/'
topic: 'fairness'
selected: 'true'
permalink: /publication/2026-insideout
---
---
<a href='https://aclanthology.org/2026.acl-long.1094/' target="_blank">[Download Paper]</a>

<p align="justify">
Advancements in Large language models (LLMs) have enabled a variety of downstream applications like story and interview script generation. However, recent research raised concerns about culture-related fairness issues in LLM-generated content. In this work, we identify and systematically investigate LLMs’ insider-outsider bias, a phenomenon where models position themselves as "insiders" of mainstream cultures during generation while externalizing less dominant cultures. We propose the InsideOut benchmark with 4,000 generation prompts and three evaluation metrics to quantify this bias through a culturally situated interview script generation task, in which an LLM is positioned as a reporter interviewing local people across 10 diverse cultures. Empirical evaluation on 5 state-of-the-art LLMs reveals that while models adopt insider tones in over 88% US-contexted scripts on average, they disproportionately default to "outsider" stances for non-Western cultures. To mitigate these biases, we propose 2 inference-time methods: a baseline prompt-based Fairness Intervention Pillars (FIP) method, and a structured Mitigation via Fairness Agents (MFA) framework consisting of a Single-Agent (MFA-SA), a Hierarchical-Agent (MFA-HA), and an autonomous Agentic Planning (MFA-Plan) pipeline. Empirical results demonstrate that agent-based MFA methods achieve outstanding and robust performance in mitigating the insider-outsider bias: For instance, on the Cultural Alignment Gap (CAG) metric, MFA-SA reduces bias in Llama model by 89.70 % and MFA-HA mitigates bias in Qwen by 82.54%. These findings showcase the effectiveness of agent-based methods as a promising direction for mitigating biases in generative LLMs.
</p>