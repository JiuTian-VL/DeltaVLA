<div align="center">
<h2 class="papername"> ΔVLA: Prior-Guided Vision-Language-Action Models via
World Knowledge Variation </h2>
<div>
    <a href="https://scholar.google.com.hk/citations?user=0GtAUPoAAAAJ&hl=zh-CN&oi=sra" target="_blank">Yijie Zhu</a><sup>1,2</sup>,
    <a href="https://orcid.org/0009-0001-9102-7051" target="_blank">Jie He</a><sup>1</sup>,
    <a href="https://rshaojimmy.github.io/OrionLab/" target="_blank">Rui Shao*</a><sup>1</sup>,
    <a href="https://scholar.google.com/citations?user=LiIKEyMAAAAJ&hl=zh-CN" target="_blank">Kaishen Yuan</a><sup>3</sup>,
    <a href="https://zitongyu.github.io/" target="_blank">Xiaochen Yuan</a><sup>4</sup>, 
    <a href="https://zitongyu.github.io/" target="_blank">Tao Tan</a><sup>4</sup>, 
    <a href="https://zitongyu.github.io/" target="_blank">Zitong Yu*</a><sup>2</sup>, 
</div>
<sup>1</sup>School of Computer Science and Technology, Harbin Institute of Technology, Shenzhen<br>
<sup>2</sup>Great Bay University
<sup>3</sup>The Hong Kong University of
Science and Technology, Guangzhou<br>
<sup>4</sup> Macao Polytechnic University
   
*Corresponding author<br>


<h3 align="center">
    <strong>
    🛠️ We're still cooking — Stay tuned!🛠️<br>
    ⭐ Give us a star if you like it! ⭐ <br> 
    ✨If you find this work useful for your research, please kindly cite our paper.✨ 
    </strong>
</h3>
</div>


## :fire: Introduction

**ΔVLA** is a **prior-guided vision‑language‑action model** that reasons about **world knowledge variation** instead of directly predicting future states. Its core idea shifts the learning paradigm **from forecasting absolute outcomes to modeling the process of change**, thereby enhancing causal consistency and efficiency in robotic manipulation. Unlike previous methods that directly predict future images or world states, ΔVLA first constructs an explicit **current‑world knowledge prior** through the **Prior‑Guided World Knowledge Extractor (PWKE)**, which extracts actionable regions, semantic cues, and geometric depth from the visual input. Building on this prior, the model encodes how knowledge evolves under actions via the **Latent World Variation Quantization (LWVQ)**, representing changes in a discrete latent space rather than reconstructing full future modalities. Furthermore, to reduce cross‑modal interference during variation modeling, ΔVLA introduces the **Conditional Variation Attention (CV‑Atten)** mechanism, which isolates attention flows across different knowledge types to promote disentangled causal reasoning.

We also provide a comprehensive comparison of different paradigms for world‑knowledge modeling and robotic control (see below).

<div align="center">
<img src='assets/intro.png' width='75%'>
</div>

The overall framework of ΔVLA is illustrated below: given a visual observation and a task instruction, ΔVLA first extracts an explicit **world knowledge prior** via **PWKE**, then encodes world changes into discrete latent variables through **LWVQ**. These prior representations along with the variation tokens are fed into a **large language model**, which performs reasoning internally using a **Conditional Variation Attention (CV‑Atten)** mechanism to ensure disentanglement among semantic, geometric, and regional variations, ultimately generating precise and causally consistent action sequences.consistent action sequences.
<div align="center">
<img src='assets/method.png' width='100%'>
</div>





## Videos


https://github.com/user-attachments/assets/f0459407-00f0-4d27-8387-1812adaff688


https://github.com/user-attachments/assets/25967916-1bf0-4ebe-b47d-4318095df25e


https://github.com/user-attachments/assets/c038f407-ebb0-4ba0-b1ab-825556f90604

https://github.com/user-attachments/assets/035239ec-0889-4385-8659-74e8e75393fd










## Acknowledgement
* Lots of code are inherited from [OpenVLA-oft](https://github.com/moojink/openvla-oft). Thanks for this great work.
