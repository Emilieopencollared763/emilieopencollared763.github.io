---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

<span class="anchor" id="about-me"></span>

I am Shengqi Yuan, a master's student in Computer Science at UC San Diego (Class of 2027). Before UCSD I studied Computer Science at Wuhan University (B.Eng., 2021–2025) and spent the fall of 2023 at UC Berkeley on exchange. My interests are robotics software, lab automation and agent systems: control loops on real hardware, the tests and logs that make them repeatable, and the evaluation of learned models. Recent work includes closed-loop waypoint navigation on a Rubik Pi rover, workload modeling for Transformer inference on edge FPGAs at ICSLAB, Wuhan University, and linear probing of a text-to-music diffusion model. I am available for internships from January 2027.

<span class="anchor" id="projects"></span>

# Projects & Research

<div class="paper-box"><div class="paper-box-image"><div><div class="badge">ROS 2, Rubik Pi 3</div><img src="images/projects/nav_trajectory.png" alt="Estimated trajectory of the best navigation run with three waypoints and three AprilTag landmarks" width="100%"><p class="caption">Estimated trajectory of the best run: 16 motion primitives, 59.5 s, three waypoints, three landmarks.</p></div></div>
<div class="paper-box-text" markdown="1">

**Closed-loop waypoint navigation with AprilTag landmarks**

<span class="meta">UC San Diego, Sep 2026 – present. Team of 2; responsible for scheme design and parameter tuning, calibration, sensor experiments, test tooling and real-robot validation. The navigation core was written by my teammate.</span>

A small rover drifts when it executes motion primitives open-loop, so after every primitive it stops, observes AprilTag landmarks, updates an SE(2) extended Kalman filter with chi-square gating, and replans. A fine spin-calibration level cut the smallest executable turn from about 24° to 3.05° (CCW) and 4.55° (CW); across 24 archived runs the best reached all three waypoints with estimated residuals of 3.1, 3.3 and 5.1 cm (filter estimates, no external ground truth).

<span class="links">Code and report: public release pending.</span>

</div></div>

<div class="paper-box no-image">
<div class="paper-box-text" markdown="1">

<span class="badge badge--inline">ICSLAB, Wuhan University</span>

**Workload modeling and scheduling for Transformer inference on edge FPGAs**

<span class="meta">Research assistant, Aug 2024 – Jun 2025, advised by Prof. Dazhao Cheng.</span>

Non-linear Transformer operators are costly on FPGAs and their resource demands are hard to schedule together, so I simplified them with low-order polynomial approximation and integer quantization (after I-BERT) and modeled scheduling as integer nonlinear programming over resource vectors and a task dependency graph, solved by dynamic programming. In simulation the best static configuration, Fix(18,2,2,2), averaged about 18.39% longer inference time than the dynamic-programming schedule. I also lead-wrote, on the PI's behalf, the lab's NSFC Young Scientists Fund (Category C) proposal, funded at RMB 300,000.

</div></div>

<div class="paper-box"><div class="paper-box-image"><div><div class="badge">Mustango, SynTheory</div><img src="images/projects/mustango_probe.png" alt="Bar chart of linear-probe accuracy by music-theory concept on Mustango representations, each against chance" width="100%"><p class="caption">Linear-probe accuracy by concept against chance; the notes row is a handcrafted chroma control, not the model.</p></div></div>
<div class="paper-box-text" markdown="1">

**Probing music-theory concepts in a text-to-music diffusion model**

<span class="meta">UC San Diego, May – Jun 2026. Team of 4; responsible for the Mustango deployment, all Mustango probing experiments, and merging four models' results into one notebook.</span>

Does a latent-diffusion music generator encode music theory in its intermediate representations? Adapting the SynTheory probing method, I trained linear probes on Mustango's VAE latents and UNet activations over a 17-run sweep of layers and diffusion timesteps. Chord-type accuracy reached 0.88 on 1,000 clips (chance 0.25), while pitch-class accuracy from VAE latents stayed near chance (about 0.10 against 0.08) even with frequency-preserving pooling; a handcrafted chroma control on the same split reached 0.72, which places the bottleneck in the latent representation itself, upstream of pooling.

</div></div>

<div class="paper-box"><div class="paper-box-image"><div><div class="badge">PLINK, GCTA</div><img src="images/projects/gwas_qq.png" alt="Q-Q plot of observed against expected p-values for linear regression and the linear mixed model" width="100%"><p class="caption">Q-Q plot of observed against expected p-values for both methods on 118,836 variants.</p></div></div>
<div class="paper-box-text" markdown="1">

**A reproducible GWAS pipeline: linear regression versus linear mixed model**

<span class="meta">UC San Diego, Jan – Mar 2026. Team of 3; main contributor (20 of 33 commits).</span>

Population structure inflates association statistics, so this pipeline takes 1000 Genomes CHB chromosome 22 (118,836 variants and 103 samples after QC), simulates a trait from 20 causal variants (seed 42), and runs PLINK linear regression against a GCTA linear mixed model, reporting λGC with Manhattan and Q-Q plots. An interactive driver checks the environment, runs the five steps in order, and retries or skips a failed step. On this cohort both methods gave λGC within about 1% of 1, so the run is a check of the pipeline rather than a demonstration of the mixed model's advantage.

<span class="links"><a href="https://github.com/zzyzhbs/gwas-lmm-comparison" target="_blank" rel="noopener">Code on GitHub</a></span>

</div></div>

<span class="anchor" id="education"></span>

# Education & Awards

<table class="edu">
<tr><td><strong>UC San Diego</strong><br>M.S. in Computer Science, GPA 4.0/4.0</td><td class="date">Sep 2025 – 2027 (expected)</td></tr>
<tr><td><strong>Wuhan University</strong><br>B.Eng. in Computer Science and Technology, GPA 3.87/4.00</td><td class="date">Sep 2021 – Jun 2025</td></tr>
<tr><td><strong>UC Berkeley</strong><br>Exchange student, Berkeley Global Access, GPA 4.0</td><td class="date">Aug – Dec 2023</td></tr>
</table>

- NOIP 2019, First Prize, Shanxi Division (ranked 10 of 293)
- CCF CSP, top 10%

<span class="anchor" id="contact"></span>

# Contact

Email is the best way to reach me: [s7yuan@ucsd.edu](mailto:s7yuan@ucsd.edu). Code is on [GitHub](https://github.com/zzyzhbs){:target="_blank" rel="noopener"}.

<span class="anchor" id="zh"></span>

# 中文摘要

袁盛琪，加州大学圣迭戈分校计算机科学硕士在读（2027 届），本科毕业于武汉大学计算机学院，2023 年秋在加州大学伯克利分校交换。方向是机器人软件、实验室自动化与智能体系统。做过的事：Rubik Pi 小车基于 AprilTag 路标的闭环航点导航，负责方案设计与参数整定、标定、实车验证；武汉大学智能计算系统实验室的边缘端 Transformer 推理负载建模与调度，仿真中最优静态配置的平均推理时间高出动态规划方案约 18.39%，受托主笔的青年科学基金申请书获批 30 万元；文本到音乐扩散模型 Mustango 的乐理概念线性探测，和弦类型探测准确率 0.88（随机 0.25）；PLINK 与 GCTA 的 GWAS 对比流水线。2027 年 1 月起可实习。联系：s7yuan@ucsd.edu。
