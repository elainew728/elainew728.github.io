---
title: "Not Every Token Needs Forgetting: Selective Unlearning to Limit Change in Utility in Large Language Model Unlearning"
collection: publications
Authors: '<b>Yixin Wan</b>, Anil Ramakrishna, Kai-Wei Chang, Volkan Cevher, Rahul Gupta'
date: 06/2025
venue: 'EMNLP'
excerpt: ''
presentationurl: ''
paperurl: 'https://arxiv.org/abs/2506.00876'
topic: 'safety'
selected: 'true'
permalink: /publication/2025-token
---
---
<a href='https://arxiv.org/abs/2506.00876.pdf' target="_blank">[Download Paper]</a>

<p align="justify">
Large Language Model (LLM) unlearning has recently gained significant attention, driven by the need to remove unwanted information, such as private, sensitive, or copyrighted content, from LLMs. However, conventional unlearning approaches indiscriminately update model parameters to forget all tokens in a target document, including common tokens (e.g., pronouns, prepositions, general nouns) that carry general knowledge. In this paper, we highlight that not every token needs forgetting. We propose Selective Unlearning (SU), which identifies a critical subset of tokens within the forgetting set that is relevant to the unwanted information, and unlearns only those tokens. Experiments on two benchmarks and six baseline unlearning algorithms demonstrate that SU not only achieves effective unlearning on the targeted forget data, but also significantly preserves the model's utility in the retaining set.
</p>