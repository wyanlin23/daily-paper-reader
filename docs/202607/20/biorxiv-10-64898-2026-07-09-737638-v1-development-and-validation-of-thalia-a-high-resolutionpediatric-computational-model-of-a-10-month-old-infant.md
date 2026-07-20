---
title: "Development and Validation of Thalia: A High-ResolutionPediatric Computational Model of a 10-Month-Old Infant"
title_zh: Thalia的开发与验证：一个10个月大婴儿的高分辨率儿科计算模型
authors: "Albrecht, A., Ntolkeras, G., Zollei, L., Sideris, G., Marturano, F., Lev, M. H., Grant, E., Bonmassar, G."
date: 2026-07-16
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.09.737638v1.full.pdf"
tags: ["query:ad"]
score: 7.0
evidence: 高分辨率儿科计算模型用于剂量测定
tldr: 当前缺少高分辨率、非变形的1岁左右儿童全身计算模型，研究基于MRI数据构建了10个月女婴Thalia模型，分割442个组织并验证。该模型为儿科医疗设备开发、剂量学和生物电磁仿真提供准确解剖基础，已作为开源资源公开。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-09-737638-v1/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1546, \"height\": 953, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-09-737638-v1/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 955, \"height\": 1405, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-09-737638-v1/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1048, \"height\": 1206, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-09-737638-v1/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1573, \"height\": 1244, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-09-737638-v1/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1522, \"height\": 927, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-09-737638-v1/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1528, \"height\": 890, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-09-737638-v1/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1559, \"height\": 940, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-09-737638-v1/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1542, \"height\": 700, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-09-737638-v1/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1546, \"height\": 741, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-09-737638-v1/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1542, \"height\": 478, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-09-737638-v1/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1545, \"height\": 364, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-09-737638-v1/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1613, \"height\": 2251, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-09-737638-v1/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1564, \"height\": 1164, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-09-737638-v1/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1544, \"height\": 603, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-09-737638-v1/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1552, \"height\": 558, \"label\": \"Table\"}]"
motivation: 现有儿科模型多由成人变形而来或分辨率不足，无法准确代表1岁左右婴幼儿解剖结构。
method: 从MRI数据半自动分割442个组织，脑组织使用婴儿FreeSurfer框架，经专家审查和文献值定量验证。
result: 获得高分辨率全身数值模型Thalia，详细呈现脑、肌肉骨骼、血管和器官，验证结果与文献一致。
conclusion: Thalia为儿科医学研究提供可靠开源平台，支持设备设计、安全评估和生物电磁仿真。
---

## 摘要
数值人体模型对于推进医疗器械设计、安全性评估以及研究解剖发育如何影响生理过程至关重要。尽管儿科模型日益增多，但在代表一岁左右儿童的高分辨率、非变形的全身模型方面仍存在关键空白。现有的儿科模型通常源自对较大年龄解剖结构的变形，或者缺乏足够的组织分割来准确捕捉早期发育解剖结构。

本研究介绍了Thalia，一个健康的10个月大女婴的非变形、高分辨率数值模型。该模型通过从磁共振成像数据中分割442个组织构建而成。使用婴儿专用的FreeSurfer框架自动分割脑组织，随后在3DSlicer中进行半自动和手动细化。该模型通过专家评审以及与文献中报道的年龄匹配解剖值的定量比较进行了验证。生成的全身模型提供了跨越大脑、肌肉骨骼系统、血管和内脏的详细解剖表示，为计算研究实现了组织特异性属性的真实分配。它为儿科医疗器械开发、剂量测定、安全性评估和生物电磁模拟提供了一个多功能平台。该儿科数值解剖模型作为开源资源公开提供。

亮点
O_LI基于MRI数据开发的10个月大儿童的高分辨率模型
C_LI
O_LI分割了442个组织以准确捕捉早期解剖发育
C_LI
O_LI模型经过专家评审和年龄匹配解剖数据验证
C_LI
O_LI儿科经颅磁刺激使用案例的示例说明
C_LI

## Abstract
Numerical human models are essential to advance medical device design, safety assessment, and study how anatomical development influences physiological processes. Despite increasing availability of pediatric models, a critical gap remains in high-resolution, non-morphed whole-body models representing children around one year of age. Existing pediatric models are often derived from morphing older anatomies or lack sufficient tissue segmentation to accurately capture early developmental anatomy.

This study introduces Thalia, a non-morphed, high-resolution numerical model of a healthy 10-month-old female. The model was constructed by segmenting 442 tissues from Magnetic Resonance Imaging data. Brain tissues were automatically segmented using an infant-specific FreeSurfer framework, followed by semi-automated and manual refinement in 3DSlicer. The model was validated by expert review and quantitative comparison with age-matched anatomical values reported in the literature. The resulting whole-body model provides detailed anatomical representation across the brain, musculoskeletal system, vasculature, and internal organs, enabling realistic assignment of tissue-specific properties for computational studies. It provides a versatile platform for pediatric medical device development, dosimetry, safety assessment, and bioelectromagnetic simulations. This pediatric numerical anatomical model is openly available as an open-source resource.

HighlightsO_LIHigh-resolution model of a 10-month-old child developed from MRI data
C_LIO_LI442 tissues segmented to capture early anatomical development accurately
C_LIO_LIModel validated against expert review and age-matched anatomical data
C_LIO_LIIllustrative Example of a pediatric transcranial magnetic stimulation use case
C_LI