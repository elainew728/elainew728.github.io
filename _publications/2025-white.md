---
title: "White Men Lead, Black Women Help? Benchmarking and Mitigating Language Agency Social Biases in LLMs"
collection: publications
Authors: '<b>Yixin Wan</b>, Kai-Wei Chang'
date: 06/2025
venue: 'ACL'
excerpt: ''
presentationurl: ''
paperurl: 'https://arxiv.org/abs/2404.10508'
topic: 'fairness'
selected: 'true'
permalink: /publication/2025-white
---
---
<a href='https://arxiv.org/abs/2404.10508.pdf' target="_blank">[Download Paper]</a>

<p align="justify">
Social biases can manifest in language agency. However, very limited research has investigated such biases in Large Language Model (LLM)-generated content. In addition, previous works often rely on string-matching techniques to identify agentic and communal words within texts, falling short of accurately classifying language agency. We introduce the Language Agency Bias Evaluation (LABE) benchmark, which comprehensively evaluates biases in LLMs by analyzing agency levels attributed to different demographic groups in model generations. LABE tests for gender, racial, and intersectional language agency biases in LLMs on 3 text generation tasks: biographies, professor reviews, and reference letters. Using LABE, we unveil language agency social biases in 3 recent LLMs: ChatGPT, Llama3, and Mistral. We observe that: (1) LLM generations tend to demonstrate greater gender bias than human-written texts; (2) Models demonstrate remarkably higher levels of intersectional bias than the other bias aspects. (3) Prompt-based mitigation is unstable and frequently leads to bias exacerbation. Based on our observations, we propose Mitigation via Selective Rewrite (MSR), a novel bias mitigation strategy that leverages an agency classifier to identify and selectively revise parts of generated texts that demonstrate communal traits. Empirical results prove MSR to be more effective and reliable than prompt-based mitigation method, showing a promising research direction.
</p>