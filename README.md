# Awesome-LLM-Alignment [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

- [Awesome-LLM-Alignment ](#awesome-llm-alignment-)
  - [Papers](#papers)
    - [LLM for Safety \& Safe-Alignment](#llm-for-safety--safe-alignment)
    - [LLM for Evaluation](#llm-for-evaluation)
    - [LLM for Human \& Value-Alignment \& Behavior-Alignment](#llm-for-human--value-alignment--behavior-alignment)
  - [Datasets](#datasets)
    - [English](#english)
    - [Chinese](#chinese)
  - [Codes](#codes)
    - [Support RLHF](#support-rlhf)

## Papers

### LLM for Safety & Safe-Alignment

---
**Characteristics of Harmful Text: Towards Rigorous Benchmarking of Language Models** \
*Maribeth Rauh, John Mellor, Jonathan Uesato, Po-Sen Huang, Johannes Welbl, Laura Weidinger, Sumanth Dathathri, Amelia Glaese, Geoffrey Irving, Iason Gabriel, William Isaac, Lisa Anne Hendricks* \
DeepMind, NeurIPS 2022. [[Paper](https://arxiv.org/abs/2206.08325)] [[Perspective API](https://www.perspectiveapi.com/)] \
28 Oct 2022
<details>
<summary><b>Abstract</b></summary>
Large language models produce human-like text that drive a growing number of applications. However, recent literature and, increasingly, real world observations, have demonstrated that these models can generate language that is toxic, biased, untruthful or otherwise harmful. Though work to evaluate language model harms is under way, translating foresight about which harms may arise into rigorous benchmarks is not straightforward. To facilitate this translation, we outline six ways of characterizing harmful text which merit explicit consideration when designing new benchmarks. We then use these characteristics as a lens to identify trends and gaps in existing benchmarks. Finally, we apply them in a case study of the Perspective API, a toxicity classifier that is widely used in harm benchmarks. Our characteristics provide one piece of the bridge that translates between foresight and effective evaluation.
</details>

---
**Training a Helpful and Harmless Assistant with Reinforcement Learning from Human Feedback** \
*Yuntao Bai, Andy Jones, Kamal Ndousse, Amanda Askell, Anna Chen, Nova DasSarma, Dawn Drain, Stanislav Fort, Deep Ganguli, Tom Henighan, Nicholas Joseph, Saurav Kadavath, Jackson Kernion, Tom Conerly, Sheer El-Showk, Nelson Elhage, Zac Hatfield-Dodds, Danny Hernandez, Tristan Hume, Scott Johnston, Shauna Kravec, Liane Lovitt, Neel Nanda, Catherine Olsson, Dario Amodei, Tom Brown, Jack Clark, Sam McCandlish, Chris Olah, Ben Mann, Jared Kaplan* \
Anthropic, NeurIPS 2022. [[Paper](https://arxiv.org/abs/2204.05862)] [[HuggingFace](https://huggingface.co/datasets/Anthropic/hh-rlhf)] \
28 Oct 2022
<details>
<summary><b>Abstract</b></summary>
We apply preference modeling and reinforcement learning from human feedback (RLHF) to finetune language models to act as helpful and harmless assistants. We find this alignment training improves performance on almost all NLP evaluations, and is fully compatible with training for specialized skills such as python coding and summarization. We explore an iterated online mode of training, where preference models and RL policies are updated on a weekly cadence with fresh human feedback data, efficiently improving our datasets and models. Finally, we investigate the robustness of RLHF training, and identify a roughly linear relation between the RL reward and the square root of the KL divergence between the policy and its initialization. Alongside our main results, we perform peripheral analyses on calibration, competing objectives, and the use of OOD detection, compare our models with human writers, and provide samples from our models using prompts appearing in recent related work.
</details>

---

### LLM for Evaluation

---
**Can Large Language Models Be an Alternative to Human Evaluations?** \
*Cheng-Han Chiang, Hung-yi Lee*\
National Taiwan University, arXiv 2023. [[Paper](https://arxiv.org/abs/2305.01937)] \
3 May 2023
<details>
<summary><b>Abstract</b></summary>
Human evaluation is indispensable and inevitable for assessing the quality of texts generated by machine learning models or written by humans. However, human evaluation is very difficult to reproduce and its quality is notoriously unstable, hindering fair comparisons among different natural language processing (NLP) models and algorithms. Recently, large language models (LLMs) have demonstrated exceptional performance on unseen tasks when only the task instructions are provided. In this paper, we explore if such an ability of the LLMs can be used as an alternative to human evaluation. We present the LLMs with the exact same instructions, samples to be evaluated, and questions used to conduct human evaluation, and then ask the LLMs to generate responses to those questions; we dub this LLM evaluation. We use human evaluation and LLM evaluation to evaluate the texts in two NLP tasks: open-ended story generation and adversarial attacks. We show that the result of LLM evaluation is consistent with the results obtained by expert human evaluation: the texts rated higher by human experts are also rated higher by the LLMs. We also find that the results of LLM evaluation are stable over different formatting of the task instructions and the sampling algorithm used to generate the answer. We are the first to show the potential of using LLMs to assess the quality of texts and discuss the limitations and ethical considerations of LLM evaluation.
</details>

---
**Judging LLM-as-a-judge with MT-Bench and Chatbot Arena** \
*Lianmin Zheng, Wei-Lin Chiang, Ying Sheng, Siyuan Zhuang, Zhanghao Wu, Yonghao Zhuang, Zi Lin, Zhuohan Li, Dacheng Li, Eric. P Xing, Hao Zhang, Joseph E. Gonzalez, Ion Stoica*\
UC Berkeley, arXiv 2023. [[Paper](https://arxiv.org/abs/2306.05685)] \
9 Jun 2023
<details>
<summary><b>Abstract</b></summary>
Evaluating large language model (LLM) based chat assistants is challenging due to their broad capabilities and the inadequacy of existing benchmarks in measuring human preferences. To address this, we explore using strong LLMs as judges to evaluate these models on more open-ended questions. We examine the usage and limitations of LLM-as-a-judge, such as position and verbosity biases and limited reasoning ability, and propose solutions to migrate some of them. We then verify the agreement between LLM judges and human preferences by introducing two benchmarks: MT-bench, a multi-turn question set; and Chatbot Arena, a crowdsourced battle platform. Our results reveal that strong LLM judges like GPT-4 can match both controlled and crowdsourced human preferences well, achieving over 80% agreement, the same level of agreement between humans. Hence, LLM-as-a-judge is a scalable and explainable way to approximate human preferences, which are otherwise very expensive to obtain. Additionally, we show our benchmark and traditional benchmarks complement each other by evaluating several variants of LLaMA/Vicuna. We will publicly release 80 MT-bench questions, 3K expert votes, and 30K conversations with human preferences from Chatbot Arena.
</details>

---

<!-- ## LLM for Application -->

### LLM for Human & Value-Alignment & Behavior-Alignment

---
**Training Socially Aligned Language Models in Simulated Human Society** \
*Ruibo Liu, Ruixin Yang, Chenyan Jia, Ge Zhang, Denny Zhou, Andrew M. Dai, Diyi Yang, Soroush Vosoughi*\
Dartmouth College, arXiv 2023. [[Paper](https://arxiv.org/abs/2305.16960)] [[Github](https://github.com/agi-templar/Stable-Alignment)] [[HuggingFace](https://huggingface.co/papers/2305.16960)] \
26 May 2023
<details>
<summary><b>Abstract</b></summary>
Social alignment in AI systems aims to ensure that these models behave according to established societal values. However, unlike humans, who derive consensus on value judgments through social interaction, current language models (LMs) are trained to rigidly replicate their training corpus in isolation, leading to subpar generalization in unfamiliar scenarios and vulnerability to adversarial attacks. This work presents a novel training paradigm that permits LMs to learn from simulated social interactions. In comparison to existing methodologies, our approach is considerably more scalable and efficient, demonstrating superior performance in alignment benchmarks and human evaluations. This paradigm shift in the training of LMs brings us a step closer to developing AI systems that can robustly and accurately reflect societal norms and values.
</details>

---
**Aligning Language Models to User Opinions** \
*EunJeong Hwang, Bodhisattwa Prasad Majumder, Niket Tandon*\
arXiv 2023. [[Paper](https://arxiv.org/abs/2305.14929)] [[Github](https://github.com/eujhwang/personalized-llms)] \
24 May 2023
<details>
<summary><b>Abstract</b></summary>
An important aspect of developing LLMs that interact with humans is to align models' behavior to their users. It is possible to prompt an LLM into behaving as a certain persona, especially a user group or ideological persona the model captured during its pertaining stage. But, how to best align an LLM with a specific user and not a demographic or ideological group remains an open question. Mining public opinion surveys (by Pew Research), we find that the opinions of a user and their demographics and ideologies are not mutual predictors. We use this insight to align LLMs by modeling both user opinions as well as user demographics and ideology, achieving up to 7 points accuracy gains in predicting public opinions from survey questions across a broad set of topics. In addition to the typical approach of prompting LLMs with demographics and ideology, we discover that utilizing the most relevant past opinions from individual users enables the model to predict user opinions more accurately.
</details>

---

## Datasets
### English
---
**[`Anthropic/hh-rlhf`](https://huggingface.co/datasets/Anthropic/hh-rlhf)**\
*Yuntao Bai, Andy Jones, Kamal Ndousse, Amanda Askell, Anna Chen, Nova DasSarma, Dawn Drain, Stanislav Fort, Deep Ganguli, Tom Henighan, Nicholas Joseph, Saurav Kadavath, Jackson Kernion, Tom Conerly, Sheer El-Showk, Nelson Elhage, Zac Hatfield-Dodds, Danny Hernandez, Tristan Hume, Scott Johnston, Shauna Kravec, Liane Lovitt, Neel Nanda, Catherine Olsson, Dario Amodei, Tom Brown, Jack Clark, Sam McCandlish, Chris Olah, Ben Mann, Jared Kaplan*\
Anthropic, arXiv 2023. [[Paper](https://arxiv.org/abs/2204.05862)] \
12 Apr 2022

<details>
<summary><b>Data Card</b></summary>
This repository provides access to two different kinds of data:

- Human preference data about helpfulness and harmlessness from Training a Helpful and Harmless Assistant with Reinforcement Learning from Human Feedback. These data are meant to train preference (or reward) models for subsequent RLHF training. These data are not meant for supervised training of dialogue agents. Training dialogue agents on these data is likely to lead to harmful models and this should be avoided.
- Human-generated and annotated red teaming dialogues from Red Teaming Language Models to Reduce Harms: Methods, Scaling Behaviors, and Lessons Learned. These data are meant to understand how crowdworkers red team models and what types of red team attacks are successful or not. The data are not meant for fine-tuning or preference modeling (use the data above for preference modeling). These data are entire transcripts of conversations that are derived from the harmlessness preference modeling data described above, where only the chosen response is incorporated into the overall transcript. Furthermore, the transcripts are annotated with human and automated measurements of how harmful the overall dialogues are.

</details>

---

### Chinese

---
**[`zhihu_rlhf_3k`](https://huggingface.co/datasets/liyucheng/zhihu_rlhf_3k)**\
A rlhf dataset contains 3k preference pairs.

---

## Codes

### Support RLHF

---

**[`Safe-RLHF: Constrained Value-Aligned LLM via Safe RLHF`](https://github.com/CarperAI/trlx)**\
*Compare with other frameworks supporting RLHF, safe-rlhf is the first framework to support all stages from SFT to RLHF and Evaluation. In addition, safe-rlhf is the first framework that takes safety preference under consideration during the RLHF stage. It holds a more theoretical guarantee for constrained parameter searching in the policy space.*\
![GitHub last commit](https://img.shields.io/github/last-commit/PKU-Alignment/safe-rlhf?label=last%20update) ![GitHub stars](https://img.shields.io/github/stars/PKU-Alignment/safe-rlhf)


---
**[`trlx: Transformer Reinforcement Learning X`](https://github.com/CarperAI/trlx)**\
*A repo for distributed training of language models with Reinforcement Learning via Human Feedback (RLHF).*\
![GitHub last commit](https://img.shields.io/github/last-commit/CarperAI/trlx?label=last%20update) ![GitHub stars](https://img.shields.io/github/stars/CarperAI/trlx)

---

**[`🐕DeepSpeed-Chat: Easy, Fast and Affordable RLHF Training of ChatGPT-like Models at All Scales🐕`](https://github.com/microsoft/DeepSpeedExamples/tree/master/applications/DeepSpeed-Chat)**\
*A fast, affordable, scalable and open system framework for enabling end-to-end Reinforcement Learning Human Feedback (RLHF) training experience to generate high-quality ChatGPT-style models at all scales.*\
![GitHub last commit](https://img.shields.io/github/last-commit/microsoft/DeepSpeedExamples?label=last%20update) ![GitHub stars](https://img.shields.io/github/stars/microsoft/DeepSpeedExamples)

---

**[`PaLM-rlhf-pytorch`](https://github.com/lucidrains/PaLM-rlhf-pytorch)**\
*Implementation of RLHF (Reinforcement Learning with Human Feedback) on top of the PaLM architecture. Basically ChatGPT but with PaLM.*\
![GitHub last commit](https://img.shields.io/github/last-commit/lucidrains/PaLM-rlhf-pytorch?label=last%20update) ![GitHub stars](https://img.shields.io/github/stars/lucidrains/PaLM-rlhf-pytorch)

---