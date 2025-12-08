---
title: "MotionEdit: Benchmarking and Learning Motion-Centric Image Editing"
collection: publications
Authors: 'Yixin Wan, Lei Ke, Wenhao Yu, Kai-Wei Chang, Dong Yu'
date: 12/2025
venue: 'arXiv'
excerpt: 'Introducing MotionEdit, a novel dataset and benchmark for motion-centric image editing. We also propose MotionNFT (Motion-guided Negative-aware FineTuning), a post-training framework with motion alignment rewards to guide models on motion editing task.'
presentationurl: ''
paperurl: 'https://arxiv.org/abs/2403.07420'
topic: null # 'fairness'
selected: 'false' # 'true'
author_profile: false
sidebar: false # Use 'false' or 'null' depending on your theme
layout: post # Use a simple layout that doesn't force a profile by default
permalink: /publication/2026-motionedit
codeurl: 'https://elainew728.github.io'
---

<style>
/* This centers the main content sections */
.page__inner-wrap, .archive {
    text-align: center; 
}
/* Ensure images and videos are centered */
.page__content img, .page__content video {
    display: block;
    margin: 0 auto;
}
/* Center the table content */
.page__content table {
    margin: 1em auto;
}
/* Ensure the body text alignment (justify) is maintained for paragraphs but centered on the page */
.page__content p {
    text-align: justify;
    max-width: 900px; 
    margin-left: auto;
    margin-right: auto;
}
/* Add this rule inside your existing <style> block */
.abstract-pad p {
    /* Adds 3em (about 3 characters width) of internal spacing on left and right */
    padding: 0 3em; 
}
</style>

<!-- # MotionEdit: Benchmarking and Learning Motion-Centric Image Editing -->
<h1 style="text-align: center; margin-top: 1em;">MotionEdit: Benchmarking and Learning Motion-Centric Image Editing</h1>

<h3 style="text-align: center; margin-top: -1em; color: #666;">arXiv, 2024</h3>

<h3 style="text-align: center;">Yixin Wan, Lei Ke, Wenhao Yu, Kai-Wei Chang, Dong Yu</h3>

<p style="text-align: center; font-size: 0.9em; margin-bottom: 2em;">
    <a href='https://arxiv.org/abs/2403.07420.pdf' target="_blank">[Download Paper]</a>
    | <a href='https://github.com/showlab/DragAnything' target="_blank">[Code]</a> 
    | <a href='#demos'>[Scroll to Demos]</a>
</p>

<div class="abstract-pad">
<p align="justify">
We introduce **MotionEdit**, a novel dataset for motion-centric image editing—the task of modifying subject actions and interactions while preserving identity, structure, and physical plausibility. Unlike existing image editing datasets that focus on static appearance changes or contain only sparse, low-quality motion edits, MotionEdit provides high-fidelity image pairs depicting realistic motion transformations extracted and verified from continuous videos. This new task is not only scientifically challenging but also practically significant, powering downstream applications such as frame-controlled video synthesis and animation.

To evaluate model performance on the novel task, we introduce **MotionEdit-Bench**, a benchmark that challenges models on motion-centric edits and measures model performance with generative, discriminative, and preference-based metrics. Benchmark results reveal that motion editing remains highly challenging for existing state-of-the-art diffusion-based editing models. To address this gap, we propose **MotionNFT** (Motion-guided Negative-aware FineTuning), a post-training framework that computes motion alignment rewards based on how well the motion flow between input and model-edited images matches the ground-truth motion, guiding models toward accurate motion transformations. Extensive experiments on FLUX.1 Kontext and Qwen-Image-Edit show that MotionNFT consistently improves editing quality and motion fidelity of both base models on the motion editing task without sacrificing general editing ability, demonstrating its effectiveness.
</p>
</div>

---

<a id="demos"></a>

<h2 style="text-align: center; margin-top: 1em;">🚀 MotionEdit Visual Demos</h2>
<h3 style="text-align: center; margin-top: 1em;">1. Comparison with Base Models</h3>


<!-- ## 🚀 MotionEdit Visual Demos -->
<!-- ### 1. Comparison with XXX -->

<p style="padding: 0 3em; text-align: center;">
Qualitative comparison of our method to Qwen-Image-Edit [10] and the MLLM-only reward training in Lin et al. [5]. The base model frequently fails to demonstrate correct motion awareness for the edit (e.g. failing to displace the watermelon in the second row, and failing to move the subject’s arms in the last row). While the MLLM-only approach improves semantic adherence, it sometimes fail to preserve subject. MotionNFT leverages optical flow to bridge this gap, achieving precise motion alignment
and high fidelity to the editing instructions.
</p>

<div class="demo-grid" style="text-align: center; margin-bottom: 0;">
    <span class="grid-label">Input Image</span>
    <span class="grid-label">Qwen-Image-Edit</span>
    <span class="grid-label">+ UniWorld-V2</span>
    <span class="grid-label">+ MotionNFT (Ours)</span>
    <span class="grid-label">Ground Truth</span>
</div>
<hr style="width: 700px; margin: 0 auto; border-top: 1px solid #ccc;"/>

<div class="demo-grid">
     <!-- Example 1-->
    <div class="grid-item"> <img src="/images/motionedit/results_suppl/400/pre.jpg" alt="Input 1"> </div>
    <div class="grid-item"> <img src="/images/motionedit/results_suppl/400/qwen_original_100.jpg" alt="Qwen 1"> </div>
    <div class="grid-item"> <img src="/images/motionedit/results_suppl/400/mllm_step210_100.jpg" alt="UniWorld 1"> </div>
    <div class="grid-item"> <img src="/images/motionedit/results_suppl/400/optical_flow4_0.2cos+0.7l1_0.5mllm_v3_step210_100.jpg" alt="Ours 1"> </div>
    <div class="grid-item"> <img src="/images/motionedit/results_suppl/400/gt.jpg" alt="GT 1"> </div>
    <!-- Example 2 -->
    <div class="grid-item"> <img src="/images/motionedit/results_suppl/601/pre.jpg" alt="Input 2"> </div>
    <div class="grid-item"> <img src="/images/motionedit/results_suppl/601/qwen_original_100.jpg" alt="Qwen 2"> </div>
    <div class="grid-item"> <img src="/images/motionedit/results_suppl/601/mllm_step210_100.jpg" alt="UniWorld 2"> </div>
    <div class="grid-item"> <img src="/images/motionedit/results_suppl/601/optical_flow4_0.2cos+0.7l1_0.5mllm_v3_step210_100.jpg" alt="Ours 2"> </div>
    <div class="grid-item"> <img src="/images/motionedit/results_suppl/601/gt.jpg" alt="GT 2"> </div>
    <!-- <div class="grid-item"> <video controls loop autoplay muted><source src="/assets/videos/placeholder_www_1.mp4" type="video/mp4"></video> </div> -->
    <!-- Example 2
    <div class="grid-item"> <img src="/images/motionedit/results_suppl/387/pre.jpg" alt="Input 2"> </div>
    <div class="grid-item"> <img src="/images/motionedit/results_suppl/387/qwen_original_100.jpg" alt="Qwen 2"> </div>
    <div class="grid-item"> <img src="/images/motionedit/results_suppl/387/mllm_step210_100.jpg" alt="UniWorld 2"> </div>
    <div class="grid-item"> <img src="/images/motionedit/results_suppl/387/optical_flow4_0.2cos+0.7l1_0.5mllm_v3_step210_100.jpg" alt="Ours 2"> </div>
    <div class="grid-item"> <img src="/images/motionedit/results_suppl/387/gt.jpg" alt="GT 2"> </div> -->
    <!-- Example 3 -->
    <div class="grid-item"> <img src="/images/motionedit/results_suppl/354/pre.jpg" alt="Input 3"> </div>
    <div class="grid-item"> <img src="/images/motionedit/results_suppl/354/qwen_original_100.jpg" alt="Qwen 3"> </div>
    <div class="grid-item"> <img src="/images/motionedit/results_suppl/354/mllm_step210_100.jpg" alt="UniWorld 3"> </div>
    <div class="grid-item"> <img src="/images/motionedit/results_suppl/354/optical_flow4_0.2cos+0.7l1_0.5mllm_v3_step210_100.jpg" alt="Ours 3"> </div>
    <div class="grid-item"> <img src="/images/motionedit/results_suppl/354/gt.jpg" alt="GT 3"> </div>
</div>

---

<h3 style="text-align: center; margin-top: 1em;">2. Comparison with Open-Sourced Models</h3>

<!-- ### 2. Motion Control -->

<p style="padding: 0 3em; text-align: center;">
[cite_start]The proposed MotionNFT can achieve ... [cite: 29].
</p>

<style>
/* Basic CSS for the responsive grid layout */
.demo-grid {
    display: grid;
    /* Defines 4 columns with equal width */
    grid-template-columns: repeat(5, 1fr); 
    gap: 10px; /* Space between the grid items */
    margin: 20px 0;
}

.demo-grid2 {
    display: grid;
    /* Defines 4 columns with equal width */
    grid-template-columns: repeat(6, 1fr); 
    gap: 10px; /* Space between the grid items */
    margin: 20px 0;
}

.grid-item {
    width: 100%;
    height: auto;
    overflow: hidden; 
    border: 1px solid #eee; /* Light border for separation */
    text-align: center; /* Center labels */
    padding: 5px;
}

.grid-item img, .grid-item video {
    width: 100%;
    height: auto;
    display: block; 
}

.grid-label {
    font-size: 0.9em;
    font-weight: bold;
    margin-top: 5px;
    display: block;
}

/* Make the grid responsive for smaller screens */
@media (max-width: 768px) {
    .demo-grid {
        grid-template-columns: repeat(2, 1fr);
    }
}
@media (max-width: 480px) {
    .demo-grid {
        grid-template-columns: 1fr;
    }
}
@media (max-width: 768px) {
    .demo-grid2 {
        grid-template-columns: repeat(2, 1fr);
    }
}
@media (max-width: 480px) {
    .demo-grid2 {
        grid-template-columns: 1fr;
    }
}
</style>

<div class="demo-grid2" style="text-align: center; margin-bottom: 0;">
    <span class="grid-label">Input Image</span>
    <span class="grid-label">UniWorld-V1</span>
    <span class="grid-label">BAGEL</span>
    <span class="grid-label">FLUX.1 Kontext[Dev]</span>
    <span class="grid-label">MotionNFT (Ours)</span>
    <span class="grid-label">Ground Truth</span>
</div>
<hr style="width: 700px; margin: 0 auto; border-top: 1px solid #ccc;"/>

<div class="demo-grid2">
    <!-- Example 1-->
    <div class="grid-item"> <img src="/images/motionedit/results_open/27/pre.jpg" alt="Input 1"> </div>
    <div class="grid-item"> <img src="/images/motionedit/results_open/27/uniworld_100.png" alt="Uniworld 1"> </div>
    <div class="grid-item"> <img src="/images/motionedit/results_open/27/bagel.png" alt="Bagel 1"> </div>
    <div class="grid-item"> <img src="/images/motionedit/results_open/27/flux_original_100.jpg" alt="Flux 1"> </div>
    <div class="grid-item"> <img src="/images/motionedit/results_open/27/optical_flow4_0.2cos+0.7l1_0.5mllm_v3_step210_100.jpg" alt="Ours 1"> </div>
    <div class="grid-item"> <img src="/images/motionedit/results_open/27/gt.jpg" alt="GT 1"> </div>
    <!-- Example 2-->
    <div class="grid-item"> <img src="/images/motionedit/results_open/28/pre.jpg" alt="Input 2"> </div>
    <div class="grid-item"> <img src="/images/motionedit/results_open/28/uniworld_100.png" alt="Uniworld 2"> </div>
    <div class="grid-item"> <img src="/images/motionedit/results_open/28/bagel.png" alt="Bagel 2"> </div>
    <div class="grid-item"> <img src="/images/motionedit/results_open/28/flux_original_100.jpg" alt="Flux 2"> </div>
    <div class="grid-item"> <img src="/images/motionedit/results_open/28/optical_flow4_0.2cos+0.7l1_0.5mllm_v3_step210_100.jpg" alt="Ours 2"> </div>
    <div class="grid-item"> <img src="/images/motionedit/results_open/28/gt.jpg" alt="GT 2"> </div>
    <!-- Example 3-->
    <div class="grid-item"> <img src="/images/motionedit/results_open/107/pre.jpg" alt="Input 3"> </div>
    <div class="grid-item"> <img src="/images/motionedit/results_open/107/uniworld_100.png" alt="Uniworld 3"> </div>
    <div class="grid-item"> <img src="/images/motionedit/results_open/107/bagel.png" alt="Bagel 3"> </div>
    <div class="grid-item"> <img src="/images/motionedit/results_open/107/flux_original_100.jpg" alt="Flux 3"> </div>
    <div class="grid-item"> <img src="/images/motionedit/results_open/107/optical_flow4_0.2cos+0.7l1_0.5mllm_v3_step210_100.jpg" alt="Ours 3"> </div>
    <div class="grid-item"> <img src="/images/motionedit/results_open/107/gt.jpg" alt="GT 3"> </div>
</div>

---

<h3 style="text-align: center; margin-top: 1em;">3. ⚠️ Bad Cases</h3>

<!-- ### 3. ⚠️ Bad Cases -->
<p style="padding: 0 3em; text-align: center;">
[cite_start]Current models are constrained by  ...., and cannot .... [cite: 39]. [cite_start]This can result in artifacts.... [cite: 40, 41, 42].
</p>

<div class="demo-grid" style="text-align: center; margin-bottom: 0;">
    <span class="grid-label">Input Image</span>
    <span class="grid-label">Qwen-Image-Edit</span>
    <span class="grid-label">+ UniWorld-V2</span>
    <span class="grid-label">+ MotionNFT (Ours)</span>
    <span class="grid-label">Ground Truth</span>
</div>
<hr style="width: 700px; margin: 0 auto; border-top: 1px solid #ccc;"/>

<div class="demo-grid">
     <!-- Example 1-->
    <div class="grid-item"> <img src="/images/motionedit/results_suppl/400/pre.jpg" alt="Input 1"> </div>
    <div class="grid-item"> <img src="/images/motionedit/results_suppl/400/qwen_original_100.jpg" alt="Qwen 1"> </div>
    <div class="grid-item"> <img src="/images/motionedit/results_suppl/400/mllm_step210_100.jpg" alt="UniWorld 1"> </div>
    <div class="grid-item"> <img src="/images/motionedit/results_suppl/400/optical_flow4_0.2cos+0.7l1_0.5mllm_v3_step210_100.jpg" alt="Ours 1"> </div>
    <div class="grid-item"> <img src="/images/motionedit/results_suppl/400/gt.jpg" alt="GT 1"> </div>
</div>

---