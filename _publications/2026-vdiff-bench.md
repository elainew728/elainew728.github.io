---
title: "VDiff-Bench: A Challenging Benchmark for Fine-Grained Image Difference Identification"
collection: publications
Authors: 'Yixin Wan, Tianle Zheng, Kai-Wei Chang'
date: 09/2026
venue: 'Arxiv'
excerpt: 'We introduce VDiff-Bench, a Benchmark for Fine-Grained Image Difference Identification.'
presentationurl: ''
paperurl: 'https://arxiv.org/abs/2609.06245'
topic: 'fact_faith'
selected: 'true'
permalink: /publication/2026-vdiff-bench
codeurl: 'https://huggingface.co/spaces/elaine1wan/vdiff-bench'
---
---
<a href='https://arxiv.org/abs/2609.06245' target="_blank">[Download Paper]</a>
<!-- | <a href='https://github.com/elainew728/motion-edit/tree/main' target="_blank">[Code]</a> -->

<p align="justify">
Multimodal Large Language Models (MLLMs) perform strongly on general visual understanding tasks such as visual question answering, yet they often struggle with a basic comparative skill: identifying what has changed between two similar images. We introduce <b>VDiff-Bench</b>, a challenging multiple-choice benchmark for fine-grained Image Difference Identification. VDiff-Bench contains 1,756 four-way questions over image pairs and covers 10 change categories: position, motion, regional image color, overall image color, appearance/disappearance, noise/resolution, texture, substitution/size, OCR/text, and illumination. Each question corresponds to two image inputs with 4 choices: the true difference, two hard negative descriptions, and a "no difference" distractor. To make the task challenging, we specifically curate ground-truth-conditioned negatives that require models to distinguish the actual change from nearby semantic alternatives. Experiments with 11 state-of-the-art open- and closed-source MLLMs show that fine-grained visual comparison remains brittle: models exhibit uneven performance across sources and change categories, with persistent failures on subtle low-level changes like noises and textures. For instance, three 7-8B-scale open-source MLLMs score 52.5-70.6% on semantic changes but only 8.7-33.3% on low-level changes like noise and texture, falsely assuming no changes between two image inputs. Surprisingly, despite strong performance of other closed-source commercial models, Grok 4.3 demonstrate remarkable performance drop on identifying noise and texture differences between images, falling significantly behind large open-source models like Kimi K2.5 and K3. Overall, VDiff-Bench provides a targeted diagnostic for evaluating comparative visual understanding in MLLMs, exposing failures that are not captured by standard single-image vision-language tasks.
</p>
