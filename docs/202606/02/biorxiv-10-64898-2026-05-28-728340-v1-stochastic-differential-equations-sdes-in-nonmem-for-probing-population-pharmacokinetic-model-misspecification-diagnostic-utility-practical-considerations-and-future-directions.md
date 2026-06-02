---
title: "Stochastic Differential Equations (SDEs) in NONMEM for Probing Population Pharmacokinetic Model Misspecification: Diagnostic Utility, Practical Considerations, and Future Directions"
title_zh: NONMEM中的随机微分方程用于探讨群体药代动力学模型错误设定：诊断效用、实际考量与未来方向
authors: "Chen, P., Bauer, R. J., Li, Y."
date: 2026-06-01
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.28.728340v1.full.pdf"
tags: ["query:ad"]
score: 7.0
evidence: 用于药代动力学模型误设诊断的随机微分方程方法，可应用于阿尔法放射性药物建模
tldr: 群体药代动力学模型常因模型误设而导致系统偏差被吸收到随机变异中，难以量化。该研究利用随机微分方程引入系统噪声项，通过NONMEM的SDE.f90插件实现模型误设诊断。在模拟和多种误设场景下，估计的系统噪声参数对误设敏感，并能分离系统与残留变异，帮助定位误设来源。该方法扩展了药效学诊断工具箱，但需结合其他诊断指标综合评估。
source: biorxiv
selection_source: fresh_fetch
motivation: 传统popPK模型用ODE描述确定性过程，模型误设难以直接量化；SDE通过引入系统噪声提供更直接的诊断框架。
method: 利用NONMEM的SDE.f90插件实现SDE-based非线性混合效应模型，在模拟和误设场景（时变消除、房室误设、残差误设）中进行验证与评估。
result: 系统噪声参数对模型误设敏感，误设越大参数值越大；SDE模型能分离系统与残留变异，辅助定位误设组件。
conclusion: SDE-based popPK建模是药效学诊断的有力补充，但系统噪声估计需结合结构模型评估、残差诊断和药理学合理性解释。
---

## 摘要
群体药代动力学（popPK）模型通常使用常微分方程（ODE）来描述确定性的浓度-时间曲线，未解释的变异性通常归因于个体间变异性或残差误差。当存在模型错误设定时，系统层面的偏差可能被吸收到这些常规变异性项中，使得模型不足的来源和幅度难以定量评估。随机微分方程（SDE）通过将明确的系统噪声分量引入结构模型，提供了一个替代框架，从而能够更直接地评估模型与数据之间的不匹配。然而，在NONMEM中基于SDE模型的实现历史上具有技术挑战性。Fortran插件子程序SDE.f90的可用性大大降低了这一障碍，并使得在NONMEM中更实际地实现基于SDE的模型成为可能。在本工作中，基于SDE的非线性混合效应模型被评估为一种用于探讨popPK模型错误设定的定量诊断框架。首先使用带有随机过程噪声的模拟一室静脉推注数据集验证了SDE.f90的实现。然后，在故意错误设定的结构或随机假设下进行了额外的模拟-估计场景，包括时变消除、房室错误设定和残差误差错误设定。在这些场景中，估计的系统噪声参数通常对错误设定敏感，较大的值通常与更大的结构或随机不匹配相关。基于SDE的建模还有助于部分地将系统层面变异性与残差变异性分离，并在选定设置下支持将错误设定定位到特定模型组件，从而帮助指导模型改进。总体而言，基于SDE的popPK建模是药理学诊断工具箱的一个有用补充，系统噪声估计最好与结构模型评估、残差诊断、参数行为及药理学合理性一起解释。

## Abstract
Population pharmacokinetic (popPK) models are commonly developed using ordinary differential equations (ODEs) to describe deterministic concentration-time profiles, with unexplained variability typically attributed to interindividual variability or residual error. When model misspecification is present, system-level deviations may be absorbed into these conventional variability terms, making the source and magnitude of model inadequacy difficult to assess quantitatively. Stochastic differential equations (SDEs) provide an alternative framework by introducing an explicit system-noise component into the structural model, allowing model-data mismatch to be evaluated more directly. However, historical implementation of SDE-based models in NONMEM has been technically challenging. The availability of the Fortran plug-in subroutine SDE.f90 substantially lowers this barrier and enables more practical implementation of SDE-based models in NONMEM. In this work, SDE-based nonlinear mixed-effects models were evaluated as a quantitative diagnostic framework for probing popPK model misspecification. The SDE.f90 implementation was first verified using simulated one-compartment intravenous bolus datasets with stochastic process noise. Additional simulation-estimation scenarios were then conducted under intentionally misspecified structural or stochastic assumptions, including time-varying elimination, compartmental misspecification, and residual error misspecification. Across these scenarios, the estimated system-noise parameter was generally sensitive to misspecification, with larger values usually associated with greater structural or stochastic mismatch. SDE-based modeling also helped partially separate system-level variability from residual variability and, in selected settings, supported localization of misspecification to specific model components, thereby helping guide model refinement. Overall, SDE-based popPK modeling is a useful addition to the pharmacometric diagnostic toolbox, with system-noise estimates best interpreted together with structural model evaluation, residual diagnostics, parameter behavior, and pharmacologic plausibility.