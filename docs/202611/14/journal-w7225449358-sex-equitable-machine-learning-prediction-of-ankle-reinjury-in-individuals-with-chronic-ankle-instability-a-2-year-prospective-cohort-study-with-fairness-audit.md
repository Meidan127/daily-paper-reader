---
title: "Sex-Equitable Machine Learning Prediction of Ankle Reinjury in Individuals with Chronic Ankle Instability: A 2-Year Prospective Cohort Study with Fairness Audit"
title_zh: 慢性踝关节不稳个体踝关节再损伤的性别公平机器学习预测：一项为期2年的前瞻性队列研究及公平性审计
authors: "Ui‐jae Hwang, Seong Jun Son, Siu-Ngor Fu, Arnold Yu Lok Wong, Dustin A. Bruening, Brent Feland, Martha Seeley, J. Ty Hopkins"
date: 2026-11-07
venue: Sports Medicine - Open
doi: 10.1186/s40798-026-01137-3
pdf: "https://link.springer.com/content/pdf/10.1186/s40798-026-01137-3.pdf"
tags: ["query:sports-ai"]
score: 9.0
evidence: 机器学习模型预测两年踝关节再损伤并进行公平性审计
tldr: "慢性踝关节不稳患者两年再伤率近50%，但缺乏个体化预测且未审查性别公平性。研究基于100人两年前瞻队列，用六种算法和嵌套交叉验证构建再伤预测模型，并以Shapley值解释关键预后因素。弹性网模型AUC达0.807，性别、足弓高度、既往扭伤、背屈活动度和稳定性指数最重要。采用性别特异阈值后均衡赔率差距降低57%，但差异影响比仍未达标，需外部验证。"
source: journal
selection_source: fresh_fetch
motivation: "CAI患者两年再伤率接近50%，但个体化再伤预测模型稀缺，且现有踝伤模型未评估性别公平性。"
method: 100名CAI患者前瞻随访2年，采集14类基线指标，训练六种算法并行嵌套交叉验证、SHAP解释和性别公平性审计。
result: "弹性网模型AUC=0.807，性别、足弓高度、既往扭伤、背屈活动度和稳定性指数最具影响；性别特异阈值使均衡赔率差距降57%。"
conclusion: 公平审计阈值策略可改善CAI再伤预测的性别公平性，但差异影响比仍低于0.80基准，临床部署前需外部验证。
---

## 摘要
背景：慢性踝关节不稳（CAI）患者2年再损伤率接近50%，但在已建立的CAI队列中，量化哪些基线功能损害可预测后续再损伤的个体化预测模型仍然稀缺，且现有踝关节损伤预测模型尚未评估性别相关公平性。本研究旨在开发并内部验证预测CAI个体2年踝关节再损伤的性别公平机器学习（ML）模型，识别最具影响力的基线预后标志物，并审计按性别分层的模型性能。方法：2017年2月至2018年2月从大学生人群中招募100名身体活动的CAI个体（男50名、女50名；平均年龄21.8 ± 2.3岁），并进行为期2年的前瞻性随访；96名（男49名、女47名）至少有一次随访应答者纳入分析（41例再损伤事件，再损伤率43%）。收集了涵盖人口学、人体测量学、损伤史、患者报告、生物力学、姿势控制和功能表现领域的14个基线预测变量。采用嵌套交叉验证训练六种算法：未加惩罚的逻辑回归基线模型和五种ML算法（弹性网络、支持向量机、随机森林、XGBoost、LightGBM）。使用Shapley加性解释和偏依赖图量化每个特征对预测的贡献。预先设定的公平性审计比较了通过折外导出的单一全局Youden阈值和性别特异性Youden阈值，采用均衡赔率差和不成比例影响比。结果：所有算法的曲线下面积（AUC）均高于0.70；弹性网络被选为主要模型（AUC = 0.807，95% CI 0.714–0.893；校准斜率 = 1.015）。性别、足弓高度指数、既往扭伤、背屈活动范围和Biodex总体稳定性指数始终是最具影响力的预后标志物。男性和女性之间的性别内区分度相当，但单一全局阈值产生0.384的均衡赔率差，通过性别特异性阈值化在不重新训练模型的情况下将其降低了57%（降至0.164）。结论：采用公平性审计阈值策略的ML模型预测了CAI个体2年踝关节再损伤，使均衡赔率差降低57%，但不成比例影响比（0.683）仍低于0.80基准。临床部署前需要外部验证。

## Abstract
BACKGROUND: Patients with chronic ankle instability (CAI) face a 2-year reinjury rate approaching 50%, but individualized prediction models that quantify which baseline impairments predict subsequent reinjury within an established CAI cohort remain scarce, and existing prediction models for ankle injury have not assessed sex-related fairness. The aim was to develop and internally validate sex-equitable machine learning (ML) models predicting 2-year ankle reinjury in individuals with CAI, identify the most influential baseline prognostic markers, and audit sex-stratified model performance. METHODS: One hundred physically active individuals (50 male, 50 female) with CAI (mean age 21.8 ± 2.3 years) were recruited from a university population between February 2017 and February 2018 and prospectively followed for 2 years; 96 (49 male, 47 female) with at least one follow-up response were retained for analysis (41 reinjury events, 43% reinjury rate). Fourteen baseline predictors spanning demographic, anthropometric, injury-history, patient-reported, biomechanical, postural-control, and functional-performance domains were collected. Six algorithms were trained with nested cross-validation: an unpenalized logistic regression baseline and five ML algorithms (Elastic Net, support vector machine, random forest, XGBoost, LightGBM). Predictive contribution of each feature was quantified using Shapley additive explanations and partial-dependence plots. A pre-specified fairness audit compared single global and sex-specific Youden thresholds derived out-of-fold using the equalized-odds gap and disproportionate-impact ratio. RESULTS: All algorithms achieved area under the curve (AUC) values above 0.70; Elastic Net was selected as the primary model (AUC = 0.807, 95% CI 0.714-0.893; calibration slope = 1.015). Sex, arch height index, previous sprains, dorsiflexion range of motion, and Biodex Overall Stability Index consistently emerged as the most influential prognostic markers. Within-sex discrimination was comparable between males and females, but a single global threshold produced an equalized-odds gap of 0.384 that was reduced by 57% (to 0.164) through sex-specific thresholding without retraining the model. CONCLUSIONS: ML models with a fairness-audited threshold strategy predicted 2-year ankle reinjury in individuals with CAI, reducing the equalized-odds gap by 57%, though the disproportionate-impact ratio (0.683) remained below the 0.80 benchmark. External validation is required before clinical deployment.

---

## 论文详细总结（自动生成）

# 论文结构化总结

## 1. 核心问题与整体含义

- **临床背景**：慢性踝关节不稳（CAI）患者 2 年再损伤率接近 50%，反复损伤带来持续医疗负担与运动参与损失。外侧踝扭伤（LAS）在运动人群中发生率约 7/1000 人年，女性更高（13.6 vs 6.94/1000 暴露）。
- **证据缺口一（预测模型稀缺）**：现有预后工具（如 Ankle-GO 评分，2 年复发 AUC≈0.75）主要在**首次扭伤后回归运动阶段**开发，而非已确诊 CAI 人群；CAI 研究以横断面病例对照为主，无法追踪"哪些基线损害后来进展为复发"，领域被概括为"model rich, data poor"。
- **证据缺口二（公平性缺失）**：临床 ML 综述强调仅高区分度不足，需审计算法公平性；而既往**没有任何 CAI 再损伤 ML 模型报告过性别公平性审计**，尽管 LAS 发生率与内在危险因素均存在性别差异。
- **研究目的**：(1) 开发并内部验证整合多域常规可获取基线指标的 2 年再损伤 ML 模型；(2) 用 SHAP/PDP 识别最具影响力的预后标志物及候选阈值；(3) 审计性别分层性能，量化性别特异阈值策略对公平性指标的影响。
- **预设假设**：ML 模型 AUC≥0.70 且校准良好；少数生物力学与损伤史标志物在多算法中稳定突出；性别内区分度相当，但单一全局阈值会造成敏感度/假阳性率差异，性别特异阈值可在不重训模型下缩小差距。

## 2. 方法论

- **总体框架**：前瞻性队列 + 多算法比较 + 嵌套交叉验证 + 可解释性分析（SHAP/PDP）+ 预设公平性审计，报告遵循 TRIPOD+AI。
- **候选预测变量（14 个，7 个域）**：人口学与生活方式（性别、年龄、习惯性体力活动）、人体测量（BMI、足弓高度指数 AHI）、损伤史与 CAI 症状（既往扭伤数、6 个月内打软腿次数、改良 AII 第 4–8 项"是"数）、患者报告功能（FAAM-ADL、FAAM-Sport）、生物力学（背屈活动度 DFROM）、姿势控制（SEBT 复合达距、Biodex 总体稳定性指数 BBS-OSI）、功能表现（三跳试验/腿长）。
- **算法**：6 种——无惩罚逻辑回归（预设基线，先验排除于主模型选择之外）+ 5 种 ML（Elastic Net、RBF 核 SVM、随机森林、XGBoost、LightGBM）。主分析将全部 14 个变量无外部特征选择地输入，依赖算法内部正则化处理共线性与噪声。
- **嵌套交叉验证流程**：
  - 外层：分层 5 折 × 重复 5 次 = 25 个外层训练-测试划分；
  - 内层：每个外层训练分区内分层 5 折，随机搜索 20 组超参、以内部 AUC 为优化目标；
  - 每名参与者在每轮重复中进入一次外层测试折，产生 5 个留出预测概率并**平均为单一 OOF 预测**。
- **防泄漏预处理**：中位数插补与标准化均在每个外层训练分区内拟合（"完全嵌套标准化"），不触碰测试折信息；类别不平衡（43%）通过分层 CV 而非过采样处理，以保护校准。
- **性能指标**：AUC（1000 次 bootstrap 95% CI）、校准斜率/截距、Brier 分数；阈值依赖指标（敏感度、特异度、精确度、NPV、F1、MCC、Youden）采用**完全样本外**程序：外层训练分区 OOF 预测估计 Youden 阈值 → 应用于未触碰测试折 → 5 次重复按参与者多数投票合并。
- **主模型选择规则（预设）**：在 AUC 前 3 的 ML 算法中，选 |校准斜率−1| + |校准截距| 最小者，Brier 分数为次级标准；前 3 名进入可解释性与公平性分析。
- **可解释性**：SHAP 值在外层各折测试预测上计算并跨折聚合，平均绝对 SHAP 值排序，并以热图展示跨算法排名一致性；PDP 在保持其他变量为各参与者观测值的前提下遍历单变量范围、跨参与者平均，取预测概率穿越 0.5 的特征值作为候选临床阈值。
- **敏感性分析**：每个外层训练分区做一次稳定性选择（LASSO 逻辑回归，100 次随机子采样，保留选择概率 π≥0.60 的特征，不足 3 个时取前 3），比较有无特征选择的每折性能，推断使用 **Nadeau–Bengio 校正重采样 t 检验**（方差按 (1/K)+(n_test/n_train) 膨胀以校正重复外层折的样本重叠），同时报告未校正 p 值。
- **公平性审计（预设，性别为受保护属性）**：
  - 组内区分度：分别计算男/女 AUC（1000 bootstrap CI）；
  - 两种阈值制度：单一全局 Youden 阈值 vs 性别特异 Youden 阈值，二者均 OOF 导出（训练分区估计、仅用于测试折），聚合后按参与者多数投票计算指标；
  - 指标：均衡赔率差 EO gap（敏感度与假阳性率性别差的绝对值取最大）、人口学均等差 DP gap、不成比例影响比 DI ratio（女/男阳性预测率之比，≥0.80 视为符合"四分之五规则"）；所有指标给参与者级 bootstrap 95% CI。

## 3. 实验设计

- **数据来源与场景**：单中心（Brigham Young University）便利样本，2017 年 2 月–2018 年 2 月招募，入组遵循国际踝关节联盟 CAI 标准（≥1 次显著扭伤且 >12 个月前、近 6 个月 ≥2 次打软腿、改良 AII 1–9 项 ≥5 个"是"、FAAM-ADL<90%、FAAM-Sport<80%、规律负重活动 ≥3 天/周且 ≥90 分钟/周）；排除下肢手术史、骨折史、近 3 个月急性损伤。
- **样本**：100 人（50 男/50 女，平均 21.8±2.3 岁）完成基线；96 人（49 男/47 女）至少一次随访应答纳入分析，41 例同侧再损伤（43%）。
- **结局与随访**：主要结局为 2 年内同侧新发外侧踝扭伤（自报内翻/跖屈事件）；6、12、24 个月 Qualtrics 问卷 + 未应答者电话补访 + 事件即时上报；对侧扭伤单独记录不计入主要结局；6/12/24 月完成率 91%/92%/88%，96 人 24 个月状态均确定（作者说明完整随访敏感性分析与主分析等价）。
- **Benchmark / 对照**：
  - 内部对照：无惩罚逻辑回归作为"标准统计基线"，用于判断 ML 是否带来增量价值；
  - 外部参照：与已发表的 Ankle-GO 评分（2 年复发 AUC=0.75）作间接比较；
  - 算法间横向比较：6 种算法在相同嵌套 CV 框架下对比；
  - 分析策略对照：主分析（无特征选择）vs 敏感性分析（稳定性选择子集）。
- **评价维度**：区分度、校准、阈值依赖指标、SHAP 排名一致性、PDP 阈值、性别公平性指标（含 bootstrap CI）。

## 4. 资源与算力

- 论文**未报告任何算力信息**：未提及 GPU 型号/数量、CPU 配置、训练时长或能耗。
- 仅说明分析环境为 **R 版本 4.5.3**，所有建模与统计在 CPU 上完成（由方法学性质推断，文中未明示）。
- 计算负载可从设计间接估计：6 种算法 × 25 个外层划分 × 内层 5 折 × 20 组超参随机搜索，另加 100 次子采样的稳定性选择、1000 次 bootstrap 重采样与 SHAP/PDP 计算；但具体耗时无记载。

## 5. 实验数量与充分性

- **实验规模概览**：
  - 主分析：6 种算法 × 嵌套 CV（25 外层划分 × 内层 5 折 × 20 超参配置/算法）；
  - 敏感性分析：同一框架下叠加稳定性选择，重复 6 种算法；
  - 可解释性：3 个顶级算法的 SHAP（含跨算法排名热图）+ 5 个顶级特征的 PDP（含敏感性分析版本）；
  - 公平性审计：3 个算法 × 2 种阈值制度 × 多指标 × 1000 次 bootstrap CI，另在敏感性分析模型上重复；
  - 统计推断：主分析 vs 敏感性分析的每折配对比较（校正与未校正 t 检验并列报告）。
- **充分性评估**：
  - **优点**：实验层次完整（性能—校准—解释—公平性—稳健性），预设分析计划、预设模型选择规则、预设公平性审计，减少事后选择性报告；同时报告校正与未校正 p 值，透明度较高。
  - **不足**：**无外部验证集、无独立时间/中心验证**；有效样本仅 96 例、41 事件，EPV≈2.9（远低于传统 ≥10 规则，作者以惩罚回归/树模型 + 内部 CV 的模拟证据辩护）；女性再损伤仅 13 例，单一误分类即改变组内敏感度 7.7 个百分点，公平性指标 bootstrap CI 很宽（如 DI 0.435–1.000）。
  - **客观/公平性**：嵌套 CV、OOF 阈值、多数投票、Nadeau–Bengio 校正等措施较好地控制了乐观偏倚与信息泄漏；但**无惩罚逻辑回归基线 AUC（0.812）点估计略高于被选为主模型的 Elastic Net（0.807）**，主模型选择依赖校准而非区分度，作者据此论证"ML 的增量价值在于校准而非原始区分"，这一解释合理但削弱了"ML 优于传统统计"的强度；敏感性分析中 AUC 普遍下降但校正后均不显著（p≥0.087），作者亦承认主分析的表观优势仅为"提示性"。

## 6. 主要结论与发现

- **预测性能**：5 种 ML 算法 AUC 均 >0.70（0.747–0.807）；Elastic Net 为主模型，AUC=0.807（95% CI 0.714–0.893），校准斜率 1.015、截距 0.007（近理想）；基线逻辑回归 AUC=0.812 但严重失校准（斜率 0.482）。
- **关键预后标志物（跨算法、跨分析策略一致）**：**性别、AHI、既往扭伤数、DFROM、BBS-OSI** 占据三个顶级算法前六名，并在稳定性选择中被选中的比例分别为 92%、88%、84%、76%、68%。
- **PDP 候选阈值**（预测概率穿越 0.5 处，探索性）：AHI 0.37–0.38、既往扭伤 4.7–5.0 次、DFROM 36–40°、BBS-OSI 1.0–1.1；临床可表述为 AHI ≥0.37、DFROM ≤37°、既往扭伤 ≥5 次、BBS-OSI ≥1.0。
- **功能测试价值有限**：三跳试验在稳定性选择中被选比例 0%，SHAP 排名 12/14，提示单跳类功能测试在已确诊 CAI 人群中对再损伤的预后价值可能有限。
- **公平性**：性别内区分度男女相当（女 0.770–0.800，男 0.735–0.767，CI 重叠）；但单一全局阈值下女性敏感度 0.615 vs 男性 0.929，**EO gap=0.384、DI ratio=0.428**（远低于 0.80）；改用性别特异阈值后 **EO gap 降至 0.164（降 57%）**、DI ratio 升至 **0.683**，且无需重训模型；XGBoost（EO 0.242→0.135，DI 0.583→0.791）与 LightGBM（EO 0.234→0.203，DI 0.431→1.001）呈类似模式。
- **差异来源定位**：
