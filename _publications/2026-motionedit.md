---
title: "MotionEdit: Benchmarking and Learning Motion-Centric Image Editing"
collection: publications
Authors: 'Yixin Wan, Lei Ke, Wenhao Yu, Kai-Wei Chang, Dong Yu'
date: 12/2025
venue: 'arXiv'
excerpt: 'We introduce MotionEdit, a novel dataset and benchmark for motion-centric image editing. We also propose MotionNFT (Motion-guided Negative-aware FineTuning), a post-training framework with motion alignment rewards to guide models on motion editing task.'
presentationurl: ''
paperurl: 'https://arxiv.org/abs/2512.10284'
topic: 'fact_faith'
selected: 'true'
permalink: /publication/2025-motionedit
codeurl: 'https://motion-edit.github.io/'
---
---
<a href='https://arxiv.org/abs/2512.10284.pdf' target="_blank">[Download Paper]</a>
| <a href='https://github.com/elainew728/motion-edit/tree/main' target="_blank">[Code]</a>

<p align="justify">
We introduce <b>MotionEdit</b>, a novel dataset for motion-centric image editing-the task of modifying subject actions and interactions while preserving identity, structure, and physical plausibility. Unlike existing image editing datasets that focus on static appearance changes or contain only sparse, low-quality motion edits, MotionEdit provides high-fidelity image pairs depicting realistic motion transformations extracted and verified from continuous videos. This new task is not only scientifically challenging but also practically significant, powering downstream applications such as frame-controlled video synthesis and animation.
To evaluate model performance on the novel task, we introduce MotionEdit-Bench, a benchmark that challenges models on motion-centric edits and measures model performance with generative, discriminative, and preference-based metrics. Benchmark results reveal that motion editing remains highly challenging for existing state-of-the-art diffusion-based editing models. To address this gap, we propose <b>MotionNFT</b> (Motion-guided Negative-aware Fine Tuning), a post-training framework that computes motion alignment rewards based on how well the motion flow between input and model-edited images matches the ground-truth motion, guiding models toward accurate motion transformations. Extensive experiments on FLUX.1 Kontext and Qwen-Image-Edit show that MotionNFT consistently improves editing quality and motion fidelity of both base models on the motion editing task without sacrificing general editing ability, demonstrating its effectiveness.
</p>
