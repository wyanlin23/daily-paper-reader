---
title: Multiscale modeling of the subcutaneous administration of peptides
title_zh: 肽类皮下给药的多尺度建模
authors: "Kuhar, S., Li, C., Ardekani, A. M."
date: 2026-06-04
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.01.724102v1.full.pdf"
tags: ["query:ad"]
score: 6.0
evidence: 多尺度皮下给药建模结合房室药代动力学模型
tldr: 皮下注射多肽的吸收机制尚不清晰，现有模型未考虑浓度依赖性低聚化和可逆结合。本文首次耦合组织级孔隙弹性模型与系统药代动力学模型，模拟注射及后续吸收过程。以semaglutide验证，模型准确预测药代参数，揭示白蛋白结合单体包裹注射区域、低聚化与结合的动态平衡等新机制。为设计理想药代动力学的多肽制剂提供理论工具。
source: biorxiv
selection_source: fresh_fetch
motivation: 多肽皮下注射的吸收机制未被充分理解，现有模型未捕捉浓度依赖性低聚化和与白蛋白及细胞外基质的可逆结合。
method: 耦合组织级孔隙弹性模型与系统药代动力学模型，考虑竞争性结合与低聚化，模拟注射及后续数天的吸收过程。
result: 以semaglutide单剂量给药验证，准确复现实验药代参数，揭示白蛋白结合单体包裹注射区域及低聚化与结合的平衡作用。
conclusion: 首次实现多肽皮下给药的跨尺度模拟，阐明结合对持续释放的贡献，为优化多肽制剂设计提供计算框架。
---

## 摘要
随着肽类皮下给药的日益普遍，了解它们的释放和吸收对于设计具有理想药代动力学特性的制剂至关重要。尽管单克隆抗体（mAbs）的吸收已通过计算建模得到广泛探索，但肽类的吸收仍知之甚少，因为肽类吸收的关键特征，包括浓度依赖性寡聚化以及与血清白蛋白和细胞外基质的可逆结合，尚未被捕捉。在这项工作中，我们提出了一种首创的方法来模拟肽类的皮下给药，该方法将高保真度的组织级孔隙弹性模型与系统隔室药代动力学模型耦合。在考虑肽类竞争性结合和寡聚化倾向的同时，该模型不仅捕捉了注射过程，还追踪了随后数天的吸收。我们使用单剂量给药的司美格鲁肽展示了该模型，并针对实验观察到的药代动力学参数进行了验证。结果显示了注射肽的不同形式在全身的分布，并描述了结合在维持其释放中的作用。该模型还揭示了新的机制，例如白蛋白结合单体包裹羽流，以及肽吸收早期阶段寡聚化与结合的平衡。

## Abstract
With the increasing prevalence of subcutaneous administration of peptides, understanding their release and absorption is key to designing formulations with desired pharmacokinetics. Though the absorption of monoclonal anti-bodies (mAbs) has been widely explored through computational modeling, that of peptides remains poorly understood, as key features of peptide absorption, including concentration-dependent oligomerization and reversible binding with serum albumin and extracellular matrix, have not been captured. In this work, we present a first-of-its-kind approach to simulating subcutaneous administration of peptides that couples a high-fidelity tissue-level poroelastic model with a systemic compartment pharmacokinetic model. While accounting for competing binding and oligomerization tendencies of peptides, the model not only captures the process of injection but also tracks the absorption over subsequent days. We demonstrate the model using a single-dose administration of semaglutide and validate it against experimentally observed pharmacokinetic parameters. The results show the distribution of the different forms of the injected peptide throughout the body and describe the role of binding in sustaining its release. The model also reveals novel mechanisms, such as albumin-bound monomers enveloping the plume and the balance of oligomerization and binding in early stages of peptide absorption.