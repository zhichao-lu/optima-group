---
title: "Optima Group - AAD Research"
layout: textlay
excerpt: "Optima Group -- Research"
sitemap: false
permalink: /research/aad.html
---

# Automated Algorithm Design (AAD)

## Introduction

**Algorithms** play a critical role in solving real-world problems. However, designing effective algorithms often 
involves a **tedious trial-and-error process** that requires **expert knowledge**.

**Automated algorithm design** has long been a goal for both researchers and practitioners, 
aiming to streamline this process and reduce reliance on manual intervention.

<div style="text-align: center;">
<img src="{{ site.url }}{{ site.baseurl }}/images/respic/aad/AAD_tasks.png" alt="aad_tasks" style="width:80%">
</div>

A **general automated algorithm design task** can be formally defined as follows:

### Given:
- **Problem Instance Distribution $$P^I$$**: A probability distribution representing the target problem instances 
  (e.g., the Traveling Salesman Problem, TSP). In practice, this distribution is typically **unknown**. 
  Therefore, we usually use **$$InstS$$**: A set of problem instances, which are samples drawn from $$P^I$$.

- **Algorithm Space $$A^S$$**: An **algorithm space**, representing the set of all possible algorithms under consideration.

- **Performance Metric $$f(a, i)$$**: A **performance metric** that evaluates the effectiveness of an algorithm $$a \in A^S$$ on a specific problem instance $$i$$.

### Goal:
**Objective**: Find an algorithm $$a \in A^S$$ that **optimizes its expected performance** over the problem instances. This can be expressed as:

$$
F(a) := \mathbb{E}_{i \sim P^I} [f(a, i)].
$$

In practice, since the true distribution $P^I$ is often unavailable, the goal is approximated using the available instances in $InstS$:

$$
F(a) := \sum_{i \in InstS} f(a, i).
$$

---


## Representative Work from Optima Group

### Learning for Optimization

Deep learning and various machine learning methodologies are employed for the automated design of algorithms. 
A particularly prominent area of focus is Neural Combinatorial Optimization (NCO), 
which involves training deep learning models to acquire heuristics for solving combinatorial optimization problems 
in an end-to-end manner. In our recent research, we have advanced multi-task cross-problem learning techniques 
specifically tailored for vehicle routing problems (VRPs) [1], explored prompt learning strategies for 
cross-distribution vehicle routing scenarios [2], and examined the supervised learning paradigm in this context [3]. 
Additionally, we are engaged in the development of Machine Learning-assisted Algorithm Design. 
Notably, we have introduced a machine learning-enhanced multiobjective solver designed to address 
complex real-world industrial routing and packing challenges [4].

### Large Language Model (LLM)-driven AAD

#### Evolution of Heuristics (EoH)：A New Algorithm Design Paradigm

The **Evolution of Heuristics** [5] concept stems from our foundational work, AEL [6], which appeared online in Nov 2023. 
It is the first to integrate **large language models** within an **evolutionary computation** framework, 
serving as designers for automated algorithm design. Contrasted with **a)** traditional hand-crafted design methods 
and **b)** conventional machine learning-assisted algorithm design, it offers several key advantages:

+ **Automation**: It drastically minimizes the need for manual design and eliminates the requirement for model training.
+ **Efficiency**: It enables the parallel and efficient evolution of new algorithms and heuristics.
+ **Performance**: It provides novel insights into target algorithm design tasks and frequently generates new state-of-the-art (SOTA) heuristics.

<div style="text-align: center;">
<img src="{{ site.url }}{{ site.baseurl }}/images/respic/aad/eoh.jpg" alt="eoh" style="width:60%">
</div>

We have successfully applied it on combinatorial optimization problems [5], acquisition function design for Bayesian optimization [7], 
attack strategy design in image adversary attack [8], turbulence model design for computational fluid dynamics [9],  
and automated data augmentation for long-tailed problems [10]. In [11], we highlight the significance of evolutionary 
search in automated algorithm/heuristic/program search.

**MEoH  [12]:** We propose the first LLM-based multi-objective heuristic search framework, **Multi-objective Evolution of Heuristic (MEoH)**, 
which integrates LLMs in a zero-shot manner to generate a non-dominated set of heuristics to meet multiple design criteria. 
We design a new dominance-dissimilarity mechanism for effective population management and selection, 
which incorporates both code dissimilarity in the search space and dominance in the objective space.

**CoEvo [13]:** We propose a framework that utilizes LLMs in an evolutionary search methodology, 
augmented by a dynamic knowledge library that integrates and refines insights in an open-ended manner. 
This approach aims to tackle the dual challenges of efficiently navigating complex symbolic representation spaces 
and leveraging both existing and newly generated knowledge to foster open-ended innovation. 
By enabling LLMs to interact with and expand upon a knowledge library, we facilitate the continuous 
generation of novel solutions in diverse forms such as language, code, and mathematical expressions.

### LLM4AD Platform

🚀LLM4AD is an open-source Python-based Platform leveraging **Large Language Models (LLMs)** for 
**Automated Algorithm Design (AD)**. 🔥It has won the second price in 
[IEEE CIS FLAME Technical Challenge 2024](https://cis.ieee.org/activities/educational-activites/competitions/flame-technical-challenge-2024). 
🔥It has been listed as one of the suggested [integrations by DeepSeek](https://github.com/deepseek-ai/awesome-deepseek-integration).

+ Visit our [GitHub Repo](https://github.com/Optima-CityU/llm4ad)
+ Please refer to the [paper](https://arxiv.org/pdf/2412.17287) for detailed information, 
including the overview, methodology, and benchmark results.
+ LLM4AD is accompanied with [Documents](https://llm4ad-doc.readthedocs.io/en/latest/) and 
[Examples](https://github.com/Optima-CityU/LLM4AD/tree/main/example) materials to support users and 
developers to easily test, build and deploy their own LLM4AD applications and conduct research.
+ LLM4AD was originally developed for [optimization tasks](https://llm4ad-doc.readthedocs.io/en/latest/task/optimization/index.html). 
The framework is versatile enough to be used in other areas, including 
[machine learning](https://llm4ad-doc.readthedocs.io/en/latest/task/machine_learning/index.html), 
[science discovery](https://llm4ad-doc.readthedocs.io/en/latest/task/science_discovery/index.html), 
game theory and engineering design.

<div style="text-align: center;">
<img src="{{ site.url }}{{ site.baseurl }}/images/respic/aad/llm4ad_platform.png" alt="llm4ad" style="width:80%">
</div>


### Surveys / Tutorials / Special Sessions

#### **Tutorial**

+ **EMO 2025 Tutorial:**  *[Multi-objective Algorithm Design using Large Language Models](https://emo2025.org/program.html)*
+ **CEC 2025 Tutorial:** *[Large Language Model for automated Algorithm Design](https://www.cec2025.org/index/page.html?id=1390)*

#### **Survey**

+  [A Systematic Survey on Large Language Models for Algorithm Design.](https://arxiv.org/abs/2410.14716) 2024 [14]

<div style="text-align: center;">
<img src="{{ site.url }}{{ site.baseurl }}/images/respic/aad/llm4ad_survey.png" alt="llm4ad_survey" style="width:80%">
</div>


### **References**

[1] Fei Liu, Xi Lin, Zhenkun Wang, Qingfu Zhang, Tong Xialiang, and Mingxuan Yuan. "[Multi-task learning for routing problem with cross-problem zero-shot generalization.](https://dl.acm.org/doi/abs/10.1145/3637528.3672040?casa_token=kd49JPOnMlwAAAAA:yDU8H-O-9eUF6u2RkuoCRinQcFbk269CBMs8PHObHoBuBessl7nZFwuXxlHtlrQJseD0oYifvm4)" *SigKDD* 2024.

[2] Fei Liu, Xi Lin, Weiduo Liao, Zhenkun Wang, Qingfu Zhang, Xialiang Tong, and Mingxuan Yuan. "[Prompt learning for generalized vehicle routing.](https://www.ijcai.org/proceedings/2024/0771.pdf)" *IJCAI* 2024.

[3] Shunyu Yao, Xi Lin, Jiashu Wang, Qingfu Zhang, and Zhenkun Wang. "[Rethinking Supervised Learning based Neural Combinatorial Optimization for Routing Problem.](https://dl.acm.org/doi/abs/10.1145/3694690)" *ACM Transactions on Evolutionary Learning*, 2024.

[4] Fei Liu, Qingfu Zhang, Qingling Zhu, Xialiang Tong, and Mingxuan Yuan. "[Machine learning assisted multiobjective evolutionary algorithm for routing and packing.](https://ieeexplore.ieee.org/abstract/document/10423590?casa_token=-A83S6MG5_UAAAAA:prI55BzOXfQjKs1MTXW5S4mjMXwSwKgYeqL49ev7UupXUk2vN87ou7rRTKzTqHAWyD8oUv8)" *IEEE Transactions on Evolutionary Computation*, 2024.

[5] Fei Liu, Tong Xialiang, Mingxuan Yuan, Xi Lin, Fu Luo, Zhenkun Wang, Zhichao Lu, and Qingfu Zhang. "[Evolution of Heuristics: Towards Efficient automated Algorithm Design Using Large Language Model.](https://arxiv.org/abs/2401.02051)" *ICML* 2024. (**Oral**)

[6] Fei Liu, Xialiang Tong, Mingxuan Yuan, and Qingfu Zhang. "[Algorithm evolution using large language model.](https://arxiv.org/abs/2311.15249)" *arXiv:2311.15249*, 2023.

[7] Yiming Yao, Fei Liu, Ji Cheng, and Qingfu Zhang. "[Evolve Cost-aware Acquisition Functions using Large Language Models.](https://link.springer.com/chapter/10.1007/978-3-031-70068-2_23)" *PPSN* 2024. (**Best Paper Nomination**)

[8] Ping Guo, Fei Liu, Xi Lin, Qingchuan Zhao, and Qingfu Zhang. "[L-autoda: Large language models for automatedally evolving decision-based adversarial attacks.](https://dl.acm.org/doi/abs/10.1145/3638530.3664121?casa_token=kEziyf5vxqUAAAAA:_bkiogphXzK_T3Qi5IpfidE8mb0VCBCepGZtoFAw3bnYQcEV9rfMzXj_rqQAIFDky_hbyAa_Ufo)" *GECCO (Companion)* 2024.

[9] Yu Zhang, Kefeng Zheng, Fei Liu, Qingfu Zhang, and Zhenkun Wang. "[AutoTurb: Using large language models for automated algebraic turbulence model discovery.](https://arxiv.org/abs/2410.10657)" *Physics of Fluids*, 2025.

[10] Pengkun Wang, Zhe Zhao, HaiBin Wen, Fanfu Wang, Binwu Wang, Qingfu Zhang, and Yang Wang. "[LLM-AutoDA: Large Language Model-Driven automated Data Augmentation for Long-tailed Problems.](https://openreview.net/forum?id=VpuOuZOVhP&referrer=%5Bthe%20profile%20of%20Binwu%20Wang%5D(%2Fprofile%3Fid%3D~Binwu_Wang1))" *NeurIPS* 2025.

[11] Rui Zhang, Fei Liu, Xi Lin, Zhenkun Wang, Zhichao Lu, and Qingfu Zhang. "[Understanding the importance of evolutionary search in automated heuristic design with large language models.](https://link.springer.com/chapter/10.1007/978-3-031-70068-2_12)" *PPSN* 2024.

[12] Shunyu Yao, Fei Liu, Xi Lin, Zhichao Lu, Zhenkun Wang, and Qingfu Zhang. "[Multi-objective evolution of heuristic using large language model.](https://arxiv.org/abs/2409.16867)" *AAAI* 2025. (**Oral**)

[13]  Ping Guo, Qingfu Zhang, and Xi Lin. "[CoEvo: Continual Evolution of Symbolic Solutions Using Large Language Models.](https://arxiv.org/abs/2412.18890)" *arXiv:2412.18890*, 2024.

[14] Fei Liu, Yiming Yao, Ping Guo, Zhiyuan Yang, Xi Lin, Xialiang Tong, Mingxuan Yuan, Zhichao Lu, Zhenkun Wang, and Qingfu Zhang. "[A Systematic Survey on Large Language Models for Algorithm Design.](https://arxiv.org/abs/2410.14716)" *arXiv:2410.14716*, 2024
