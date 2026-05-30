---
title: An AI-agent-orchestrated grey-box Transformer framework for sparse pharmacokinetic curve reconstruction and pharmacometric model initialization
title_zh: 一种AI代理编排的灰盒Transformer框架，用于稀疏药代动力学曲线重建和药理学模型初始化
authors: "Chen, J., Wang, J., Du, S., Chen, Y., Li, K., Song, J., Liu, D."
date: 2026-05-27
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.23.727373v1.full.pdf"
tags: ["query:ad"]
score: 7.0
evidence: 药代动力学建模框架适用于一般药物，可用于阿尔法放射性药物分布建模
tldr: "临床药代动力学建模因稀疏采样和单药模型泛化性差而受限。本文提出PKFM，一种灰色框Transformer框架，在32种药物上预训练，从稀疏浓度观测、给药事件、分子描述符和生理协变量重建浓度-时间曲线，同时保持可解释性。使用三个稀疏输入点，对Midazolam口服和Verapamil口服分别达到R²=0.992和0.990。重建曲线用于NONMEM改进了协方差稳定性和个体预测精度；对比学习嵌入支持Top-10 PBPK候选检索，75.6%观测在2倍范围内；PM Agent在标准化建模基准上优于通用编程工具。该框架作为稀疏PK证据的信息补全层和建模工作流的结构化支架，但临床或监管使用需前瞻性验证。"
source: biorxiv
selection_source: fresh_fetch
motivation: 临床PK建模受稀疏采样、单药模型泛化性差和人工流程繁琐的制约，需要跨药物预训练模型高效推断完整药物暴露。
method: 提出PKFM灰色框Transformer，预训练于32种药物，输入稀疏浓度、给药事件、分子描述符和生理协变量，输出可解释的完整浓度-时间曲线。
result: "三个稀疏点重建曲线R²>0.99；对比学习检索PBPK候选75.6%在2倍内；PM Agent在建模基准中稳定性和胜率优于通用工具。"
conclusion: PKFM作为信息补全层，为稀疏PK证据和建模工作流提供结构化框架，但需前瞻性验证和专家评估才能用于临床或监管。
---

## 摘要
临床药代动力学（PK）建模受限于稀疏采样、单药物模型的有限泛化能力以及劳动密集型工作流程，使得从有限的浓度观测中推断完整的药物暴露变得困难。我们提出了药代动力学基础模型（PKFM），这是一个跨32种药物预训练的灰盒Transformer框架，能够从稀疏浓度观测、给药事件、分子描述符和生理协变量中重建浓度-时间曲线，同时保持输出可解释性。在代表性口服PK曲线中，三个稀疏输入点恢复了主要的吸收-消除轨迹，对于咪达唑仑口服和维拉帕米口服分别实现了决定系数（R²）=0.992和R²=0.990。在NONMEM（非线性混合效应建模）中使用重建曲线改善了协方差稳定性和个体预测准确性。对比学习嵌入支持前10个基于生理的药代动力学（PBPK）候选检索，其中75.6%的观测值落在2倍范围内。一个基于药理学信息的AI代理（PM代理）在标准化建模基准测试中，在稳定性和成对胜率方面优于通用编程工具，每次运行在下游使用前都需要人类药理学家确认。这些结果支持跨药物预训练的PK模型作为稀疏PK证据的信息补全层和建模工作流程的结构化支架；临床或监管应用需要前瞻性验证、更广泛的外部基准测试和独立专家评估。

## Abstract
Clinical pharmacokinetic (PK) modelling is constrained by sparse sampling, limited general-isability of single-drug models, and labour-intensive workflows, making it difficult to infer complete drug exposure from limited concentration observations. We present the Pharmacokinetic Foundation Model (PKFM), a grey-box Transformer framework pre-trained across 32 drugs that reconstructs concentration-time profiles from sparse concentration observations, dosing events, molecular descriptors, and physiological covariates while preserving output interpretability. In representative oral PK curves, three sparse input points recovered the principal absorption-elimination trajectory, achieving coefficient of determination (R2) = 0.992 for Midazolam oral and R2 = 0.990 for Verapamil oral. Using reconstructed curves in NONMEM (nonlinear mixed-effects modelling) improved covariance stability and individual prediction accuracy. Contrastive-learning embeddings supported Top-10 physiologically based pharmacokinetic (PBPK) candidate retrieval, with 75.6% of observations within the 2-fold range. A pharmacometrics-informed AI Agent (PM Agent) outperformed general-purpose programming tools in stability and pairwise win rate on a standardised modelling benchmark, with each run requiring human pharmaco-metrician confirmation before downstream use. These results support cross-drug pre-trained PK models as an information-completion layer for sparse PK evidence and a structured scaffold for the modelling workflow; clinical or regulatory use requires prospective validation, broader external benchmarking, and independent expert assessment.