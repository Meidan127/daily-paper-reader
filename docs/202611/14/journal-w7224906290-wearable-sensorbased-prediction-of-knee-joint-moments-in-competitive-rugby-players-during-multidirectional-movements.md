---
title: Wearable Sensor‐Based Prediction of Knee Joint Moments in Competitive Rugby Players During Multidirectional Movements
title_zh: 基于可穿戴传感器的竞技橄榄球运动员多方向运动过程中膝关节力矩预测
authors: "Zixiang Gao, Robin Trama, David Mcnish, Michael Esposito, Jake Ruschkowski, Darren John Stefanyshyn, John William Wannop"
date: 2026-10-30
venue: Scandinavian Journal of Medicine and Science in Sports
doi: 10.1111/sms.70391
pdf: "https://onlinelibrary.wiley.com/doi/pdfdirect/10.1111/sms.70391"
tags: ["query:sports-ai"]
score: 8.0
evidence: 可穿戴足底压力传感器结合可解释机器学习预测膝关节力矩
tldr: "橄榄球多方向动作中膝力矩难以在场外连续监测。研究用足底压力传感器与GA-DFR在31名竞技橄榄球运动员中筛选7–18个传感器，并以嵌套交叉验证预测膝合力矩及三个分量。合力矩汇总R²为0.795，屈伸、内收外展、内外旋R²分别为0.806、0.662、0.675，性能优于线性回归和CNN。SHAP显示关键贡献集中于支撑期9%–55%，为无标记可解释膝负荷评估提供依据。"
source: journal
selection_source: fresh_fetch
motivation: 竞技橄榄球多方向动作膝负荷高，但实验室动作捕捉难以现场连续监测，需可穿戴、可解释的膝力矩估计方法。
method: 31名运动员完成四种橄榄球动作，同步采集足底压力、动作捕捉与地面反力；GA-DFR筛选7–18个传感器预测膝合力矩，DFR预测三分量，SHAP解释。
result: 合力矩R²=0.795，RMSE=0.0512 N·m/N；屈伸、内收外展、内外旋R²为0.806、0.662、0.675，DFR优于线性回归和CNN，与DNN/LSTM无显著差异。
conclusion: "减少足底压力输入即可在未见运动员中估计膝合力矩及方向特异波形，SHAP提示支撑期9%–55%为关键贡献段，支持可解释现场膝负荷监测。"
---

## 摘要
本研究旨在开发一个可解释的机器学习框架，利用足底压力传感器估算橄榄球专项动作中的膝关节力矩。共招募31名北美竞技橄榄球运动员，在运动捕捉实验室的填充式人造草坪表面上完成四种常见橄榄球动作。同步采集足底压力、运动捕捉和地面反作用力数据。膝关节力矩通过逆动力学计算。采用遗传算法-深度森林回归（GA-DFR）选择足底压力传感器，并在参与者水平嵌套交叉验证中预测合成力矩。四种替代模型使用相同的传感器布局和参与者划分预测合成力矩。补充的深度森林回归（DFR）模型使用这些布局预测三个力矩分量。SHapley Additive exPlanations（SHAP）用于解释留出集预测。传感器布局包含7–18个传感器。合并的合成力矩R²为0.795，均方根误差为0.0512 N·m/N。DFR优于线性回归和卷积神经网络，与深度神经网络或长短期记忆网络无显著差异。屈伸、内收-外展和内旋-外旋力矩的合并R²分别为0.806、0.662和0.675。合成力矩的时间SHAP贡献在支撑期的9%–55%期间超过其整个支撑期均值，在24%处达到峰值。减少的足底压力输入支持在未见过的橄榄球运动员中估计合成及方向特异性膝关节力矩波形。

## Abstract
ABSTRACT This study aimed to develop an interpretable machine learning framework using plantar‐pressure sensors to estimate knee moments during rugby‐specific movements. A total of 31 North American competitive rugby players were recruited to perform four common rugby movements on an infilled artificial turf surface in a motion capture laboratory. Synchronized data acquisition was performed for plantar pressure, motion capture, and ground reaction forces. Knee moments were calculated via inverse dynamics. Genetic Algorithm‐Deep Forest Regression (GA‐DFR) was used to select plantar‐pressure sensors and predict resultant moments within participant‐level nested cross‐validation. Four alternative models predicted the resultant using the same layouts and participant splits. Complementary deep forest regression (DFR) models predicted the three moment components using these layouts. SHapley Additive exPlanations (SHAP) interpreted held‐out predictions. Layouts contained 7–18 sensors. Pooled resultant R 2 was 0.795, with root mean square error of 0.0512 N·m/N. DFR performed better than linear regression and the convolutional neural network, with no significant differences from the deep neural network or long short‐term memory network. Pooled R 2 was 0.806, 0.662, and 0.675 for flexion‐extension, adduction‐abduction, and internal‐external rotation moments, respectively. Resultant temporal SHAP contributions exceeded their stance‐wide mean during 9%–55% of stance, peaking at 24%. Reduced plantar‐pressure inputs supported estimation of resultant and direction‐specific knee‐moment waveforms in unseen rugby players.

---

## 论文详细总结（自动生成）

> 资料范围说明：以下总结仅依据论文摘要与所给元数据，未获取全文；涉及训练细节、统计检验和算力等信息时，以“摘要未报告”标注，避免过度推断。

## 1. 核心问题与整体含义

- **研究动机**：竞技橄榄球包含大量急停、变向、侧切等多方向动作，膝关节负荷高，与膝损伤风险密切相关。实验室动作捕捉与测力台结合逆动力学可准确计算膝关节力矩，但难以在训练场或比赛中连续、低成本监测。
- **核心问题**：能否仅利用可穿戴足底压力传感器，在减少传感器数量的条件下，准确且可解释地估计橄榄球专项动作中的膝关节合力矩及方向特异性力矩波形？
- **整体含义**：研究试图连接“实验室金标准膝负荷测量”与“现场可穿戴监测”，为橄榄球运动员的膝负荷评估、动作技术优化和损伤预防提供可解释的机器学习框架。

## 2. 方法论

- **核心思想**：以足底压力传感器为输入，以动作捕捉逆动力学计算的膝关节力矩为标签，构建“传感器筛选 + 深度森林回归 + 模型解释”的可解释预测框架。
- **数据与标签生成**：
  - 31名北美竞技橄榄球运动员在运动捕捉实验室的填充式人造草坪上完成四种常见橄榄球动作。
  - 同步采集足底压力、运动捕捉和地面反作用力数据。
  - 膝关节力矩通过逆动力学计算，作为监督学习标签。
- **传感器选择与预测**：
  - 使用**遗传算法-深度森林回归（GA-DFR）**选择足底压力传感器，并预测膝关节合力矩。
  - 传感器布局最终包含**7–18个传感器**，说明方法强调减少输入数量而非使用全部压力单元。
  - 传感器选择与预测在**参与者级嵌套交叉验证**中完成，以降低同一受试者数据同时进入训练和测试造成的泄漏风险。
- **方向特异性建模**：
  - 使用补充的**深度森林回归（DFR）**模型，在相同传感器布局下预测三个膝关节力矩分量：屈伸、内收-外展、内旋-外旋。
- **模型解释**：
  - 使用**SHAP（SHapley Additive exPlanations）**解释留出集预测，并分析时间维度上的贡献。
  - 摘要报告了“时间SHAP贡献”在支撑期内的变化，用于识别膝力矩预测的关键时段。
- **算法流程概括**：同步采集数据 → 逆动力学计算膝力矩 → 在参与者级嵌套交叉验证内用GA搜索传感器子集并训练DFR预测合力矩 → 用相同布局训练DFR预测三分量 → 用线性回归、CNN、DNN、LSTM作为替代模型在同一布局和参与者划分下比较 → 用SHAP解释留出预测。

## 3. 实验设计

- **数据集/场景**：
  - 单一实验队列：**31名北美竞技橄榄球运动员**。
  - 场景为实验室内的填充式人造草坪，完成**四种常见橄榄球多方向动作**。
  - 输入为足底压力；标签为运动捕捉与测力台逆动力学计算的膝关节力矩。
- **Benchmark**：
  - 以动作捕捉结合地面反作用力经逆动力学得到的膝关节力矩作为金标准参考。
  - 评价指标包括汇总**R²**和归一化**均方根误差 RMSE（N·m/N）**。
- **对比方法**：
  - 主模型：GA-DFR预测膝关节合力矩。
  - 替代模型：线性回归、卷积神经网络（CNN）、深度神经网络（DNN）、长短期记忆网络（LSTM）。
  - 摘要明确指出替代模型使用**相同传感器布局和相同参与者划分**预测合力矩，以增强比较公平性。
  - 此外，DFR用于预测三个力矩分量，并报告各分量R²。
- **解释性实验**：
  - 使用SHAP对留出集预测进行解释，并分析支撑期内的时间贡献分布。

## 4. 资源与算力

- 摘要与元数据**未报告**GPU型号、数量、训练时长、显存占用或总计算量。
- 由于未提供算力信息，无法评估模型训练成本、能耗或大规模部署可行性；仅可推断涉及DFR、CNN、DNN、LSTM等模型训练，但具体计算资源不明。

## 5. 实验数量与充分性

- **实验规模概况**：
  - 一个31人竞技橄榄球运动员队列。
  - 四种橄榄球专项动作。
  - 参与者级嵌套交叉验证。
  - GA-DFR进行传感器选择，布局规模为7–18个传感器。
  - 合力矩预测中比较了DFR与线性回归、CNN、DNN、LSTM等替代模型。
  - 三个膝关节力矩分量分别建模。
  - 包含SHAP时间贡献分析。
- **充分性判断**：
  - **优点**：采用参与者级嵌套交叉验证，并使用相同布局和参与者划分比较多种模型，内部验证设计较为严谨；同时覆盖合力矩和三个方向分量，并加入可解释性分析。
  - **不足**：仅从摘要看，研究似乎基于单一队列、单一实验室场地和四种动作，缺少跨数据集、跨场地、跨鞋具或跨人群的外部验证；摘要未说明超参数调优细节、统计检验细节、重复实验次数，以及传感器数量/布局的消融分析。
  - **公平性**：相同布局与参与者划分有助于公平比较，但替代模型是否经过同等程度的调参、是否使用相同输入预处理，摘要未展开，无法完全判断。

## 6. 主要结论与发现

- 传感器布局仅需**7–18个足底压力传感器**即可估计膝关节力矩。
- 膝关节**合力矩**汇总预测性能为：**R² = 0.795**，**RMSE = 0.0512 N·m/N**。
- 三个方向分量的汇总R²分别为：
  - 屈伸力矩：**0.806**
  - 内收-外展力矩：**0.662**
  - 内旋-外旋力矩：**0.675**
- DFR在合力矩预测中**优于线性回归和CNN**，与DNN或LSTM**无显著差异**。
- SHAP时间分析显示，合力矩预测的时间贡献在支撑期**9%–55%** 区间超过整个支撑期均值，并在**24%** 处达到峰值。
- 总体结论是：减少足底压力输入后，仍可在**未见过的橄榄球运动员**中估计膝关节合力矩及方向特异性力矩波形，并支持可解释的现场膝负荷监测思路。

## 7. 优点

- **可解释性强**：不仅追求预测精度，还使用SHAP解释模型在时间维度上的贡献，增强对膝力矩估计机制的理解。
- **传感器精简**：通过GA筛选7–18个传感器，符合可穿戴现场应用的轻量化需求。
- **验证设计较严谨**：采用参与者级嵌套交叉验证，降低受试者数据泄漏风险。
- **比较设置较公平**：多种替代模型使用相同传感器布局和参与者划分，便于横向比较。
- **任务覆盖较全面**：同时预测合力矩和三个方向分量，并报告方向特异性性能。
- **应用导向明确**：面向橄榄球多方向动作的现场膝负荷监测，具有运动损伤预防和训练监控潜力。

## 8. 不足与局限

- **证据范围受限**：当前仅有摘要，无法核查全文中的数据处理、超参数、统计检验和模型细节。
- **外部有效性有限**：数据来自31名北美竞技橄榄球运动员、实验室填充式人造草坪和四种规定动作，能否推广到比赛、不同场地、不同鞋具、疲劳状态和更多动作尚不明确。
- **样本与人群限制**：样本量相对有限，且为特定竞技水平人群，对其他性别、年龄、运动水平和损伤状态人群的泛化性未知。
- **标签依赖实验室金标准**：膝力矩标签来自动作捕捉与逆动力学的实验室测量，现场应用中无法直接获得同样标签，模型迁移需进一步验证。
- **部分分量精度中等**：内收-外展和内旋-外旋的R²约为0.66–0.68，低于屈伸力矩，方向特异性估计仍有提升空间。
- **解释不等于因果**：SHAP反映模型贡献，不能直接等同于生理因果机制；关键支撑期时段仍需生物力学验证。
- **算力与实时性未报告**：摘要未说明计算资源、推理延迟和实时部署能力，现场连续监测可行性仍需工程验证。
- **实验覆盖仍可扩展**：缺少多数据集外部验证、传感器布局消融、跨动作/跨场地泛化以及与其他可穿戴模态融合的比较。

（完）
