# 硬件产品经理学习手册

> 基于本仓库 `hardware-product-manager-skill` 整理

这份文档把仓库中分散的 `SKILL.md`、`references/`、`templates/`、`checklists/` 和示例，整理成一套可以从头学习、也可以直接拿来做项目的中文方法论。

---

# 目录

1. 这套 Skill 是做什么的
2. 核心思维：不要从功能开始
3. 两种项目入口
4. 场景机会发现：从场景里找产品
5. JTBD：把“想要功能”还原成真实任务
6. VOC：从用户声音中发现真实问题
7. 产品发现：判断问题是否值得做
8. 产品验证：GO / CONDITIONAL GO / NO-GO
9. 产品定义：把机会变成明确产品
10. PRD：把产品定义变成可执行需求
11. 成本与 BOM：从售价倒推能不能赚钱
12. 供应商 RFQ 与供应商选择
13. 硬件研发阶段：Concept → EVT → DVT → PVT → MP
14. DFM、DFT、可靠性与 FMEA
15. 认证与合规
16. 决策框架：事实、假设、未知和验证
17. 三个关键 Gate
18. 命令速查
19. 推荐学习路径
20. 一条完整的新品开发流程

---

# 1. 这套 Skill 是做什么的

这套 Skill 的定位不是“帮你写文档”，而是让 AI 按照一个高级硬件产品经理 + NPI 负责人的方式参与消费电子产品开发。

完整链路是：

**场景机会发现 → VOC → 市场机会 → 产品验证 → 产品定义 → PRD → 硬件规格 → 成本/BOM → 供应商 RFQ → EVT → DVT → PVT → 认证 → MP → 上市 → 用户反馈闭环**

最终目标不是“文件更多”，而是：

> **提高发现并推出一个用户需要、有差异化、技术可行、成本可行、能量产、符合认证要求并且能赚钱的硬件产品的概率。**

这套方法尤其适合：

- 消费电子
- Amazon / 电商产品
- 无线充
- 鼠标、键盘等电脑外设
- 蓝牙 / Wi-Fi 产品
- 音频产品
- 充电产品
- 智能家居
- 电池类产品
- OEM / ODM 产品开发

---

# 2. 核心思维：不要从功能开始

整个仓库最重要的一条原则是：

**Scene → User → Activity → Job → User Voice → Problem → Demand → Opportunity → Product → Specification → Engineering → Manufacturing → Market**

中文可以理解为：

**场景 → 用户 → 行为 → 任务 → 用户声音 → 问题 → 需求 → 机会 → 产品 → 规格 → 工程 → 制造 → 市场**

这意味着：

错误方式：

> 我想做一个 15W 无线充，再加一个 LED，再加提示音，再看看能不能卖。

更好的方式：

> 用户在卧室睡前会做什么？
> 哪个动作经常失败？
> 哪些问题让用户反复确认、调整、抱怨或自己想办法解决？
> 哪些问题值得做成产品？
> 什么产品才是最简单有效的解决方案？

**产品不是起点，用户任务和问题才是起点。**

---

# 3. 两种项目入口

本 Skill 有两种入口模式。

## 模式 A：还不知道做什么产品

适用于：

- 只知道一个场景
- 只知道一类用户
- 想寻找新品机会

入口命令：

`/scene-opportunity`

流程：

**场景 → 用户活动 → JTBD → VOC → 问题空间 → 机会空间 → 候选产品 → 机会排序 → `/validate`**

例如：

> 市场：美国
> 场景：家庭卧室床头柜
> 目标：寻找消费电子产品机会

这时候 AI 不应该马上给你列“无线充、闹钟、夜灯、白噪音机”。

它应该先研究：

- 睡前准备
- 手机和耳机充电
- 看时间
- 闹钟
- 起夜
- 光线
- 噪音
- 收纳
- 线缆
- 手机放置
- 伴侣互相干扰

再从里面寻找真正未满足的任务。

## 模式 B：已经有产品想法

适用于：

- 已经决定研究无线充
- 已经有供应商方案
- 已经看到某个市场机会

流程：

**`/VOC`（必要时）→ `/validate` → `/define` → `/prd` → 后续开发流程**

如果已有充分 VOC 数据，不必重复研究。

---

# 4. 场景机会发现：从场景里找产品

文件：`references/scene-opportunity-discovery.md`

场景机会发现不是随机脑暴产品，而是寻找：

- 未完成的任务
- 反复出现的摩擦
- 高严重度失败
- 用户自己创造的 workaround
- 多步骤但本可简化的行为
- 多个产品拼在一起才能完成的任务
- 兼容性问题
- 光、噪音、热、尺寸、线缆、充电、收纳等场景问题

## 场景边界要先定义

至少明确：

- 国家 / 市场
- 物理位置
- 时间段
- 用户群
- 触发事件
- 前、中、后行为
- 场景里已有的物品和设备
- 环境限制

例如“家庭”太宽。

“美国城市家庭，晚上 10 点到早上 7 点，卧室床头柜”就更适合研究。

## 场景地图要回答 9 个问题

1. 谁在这里？
2. 他想完成什么？
3. 行为顺序是什么？
4. 现在用什么产品解决？
5. 哪里发生摩擦？
6. 哪里会失败？
7. 用户反复检查、调整、携带、记忆、整理、充电或避免什么？
8. 用户有什么 workaround？
9. 哪些任务仍没有被很好解决？

## 特别强的机会信号

比“用户说不喜欢”更值得关注的是：

- 反复重新摆放
- 反复确认
- 自己贴胶带
- 自己增加转接头
- 自己加垫片
- 自己改装
- 为一个简单任务买多个产品
- 为部分解决方案支付高价

用户愿意付出时间、金钱或行为成本，通常说明问题更真实。

---

# 5. JTBD：把“想要功能”还原成真实任务

文件：`references/jobs-to-be-done.md`

JTBD 的标准句式：

> **当……的时候，我想要……，这样我就可以……。**

英文形式：

> When [situation], I want to [motivation/action], so I can [desired outcome].

## 不要把产品写成 Job

错误：

> 我想要一个磁吸无线充。

正确：

> 当我睡前把手机放下时，我希望手机能自动正确开始充电，不需要仔细对位，这样我可以不用反复确认就直接睡觉。

后者才是用户任务。

## 三类 Job

### Functional Job

用户实际上要完成什么。

例如：

- 晚上把手机充满
- 确认第二天闹钟能工作

### Emotional Job

用户希望有什么感觉。

例如：

- 安心
- 不被打扰
- 不焦虑

### Social Job

用户希望别人怎么看自己。

普通消费电子通常优先研究 Functional Job，除非情绪或身份明显影响购买。

## 一个强机会的典型特征

**重要性高 + 当前满意度低 + 发生频繁 + 现有方案弱**

---

# 6. VOC：从用户声音中发现真实问题

文件：`references/voice-of-customer.md`

VOC（Voice of Customer）不是“把评论总结一下”。

正确流程是：

**原始用户声音 → 场景 → 问题编码 → 问题聚类 → 频率 → 严重度 → 当前方案 → workaround → 根因假设 → 产品机会 → 验证**

## VOC 数据可以来自哪里

1. Amazon 等电商评论
2. 产品 Q&A
3. Reddit / 论坛 / 社区
4. 客服工单
5. 退款和退货原因
6. 用户访谈
7. 直接观察用户使用
8. 已有产品使用数据

不要只依赖一种来源。

## 新消费电子的推荐 VOC 流程

1. 选择 10–20 个直接或间接竞品
2. 收集足够广泛的用户声音
3. 保留原始文字和上下文
4. 对每条问题编码
5. 合并同义问题
6. 区分“症状”和“根因”
7. 有完整数据时统计频率
8. 找用户 workaround
9. 排名用户问题
10. 转成机会假设
11. 对高影响假设进一步验证

## 不要把功能需求直接当答案

用户说：

> 我希望 LED 有关闭按钮。

真正的问题可能是：

> 夜间持续亮灯影响睡眠。

可能的解决方案有：

- 自动熄灯
- 自动调暗
- 环境光感应
- 无常亮 LED
- 手动关闭

**用户提出的是方案，不一定是最佳方案。**

## 症状 ≠ 根因

例如：

> “充不上电”

可能来自：

- 对位错误
- 手机壳干扰
- 协议不支持
- 适配器功率不足
- 过热保护
- 硬件故障

因此根因必须标记为 `[HYPOTHESIS]`，直到有证据验证。

## VOC 证据等级

- `[DATA]`：直接观察到的用户声音
- `[PATTERN]`：多个独立用户/来源重复出现
- `[HYPOTHESIS]`：推测出的底层需求或根因
- `[VALIDATED]`：通过进一步数据、访谈或测试确认

AI 的推断永远不能自动等同于“用户已验证需求”。

---

# 7. 产品发现：判断问题是否值得做

文件：`references/product-discovery.md`

产品发现阶段研究：

- 目标市场
- 国家
- 用户
- 使用场景
- 现有替代方案
- 痛点
- 市场成熟度
- 价格带
- 竞争强度
- 市场空白

## 场景描述公式

**Person + Place + Time + Task + Problem**

即：

**什么人 + 在哪里 + 什么时间 + 做什么 + 遇到什么问题**

同时区分：

- 核心场景
- 次要场景
- 边缘场景

## 痛点优先级

可以分为：

- P0：关键问题
- P1：重要问题
- P2：锦上添花

判断维度：

- 发生频率
- 严重度
- 现有方案
- 现有方案质量
- 支付意愿
- 产品机会

## 竞争不是只看“同类产品”

至少看四层：

1. 直接竞品
2. 间接竞品
3. 替代行为
4. 新兴替代技术

例如无线充的替代方案不只是另一个无线充，还包括：

- USB-C 线充
- MagSafe / Qi2
- 多口充电器
- 床头带电源的家具

---

# 8. 产品验证：GO / CONDITIONAL GO / NO-GO

文件：`SKILL.md`、`references/product-definition.md`

一个产品不能因为“看起来不错”就进入开发。

必须至少判断七个方面：

1. Desirability：用户真的想要吗？
2. Differentiation：为什么用户会选你？
3. Technical Feasibility：技术做得到吗？
4. Cost Feasibility：成本做得到吗？
5. Margin Feasibility：能赚钱吗？
6. Manufacturing Feasibility：工厂能稳定量产吗？
7. Certification Feasibility：目标市场能合法销售吗？

最后给出三种结果之一：

### GO

证据足够，可以进入下一阶段。

### CONDITIONAL GO

方向有希望，但必须先验证某些关键假设。

### NO-GO

当前产品定义不值得继续。

**Skill 明确规定：不能默认给 GO。**

---

# 9. 产品定义：把机会变成明确产品

文件：`references/product-definition.md`

## 产品定位公式

> 对于 [目标用户]，当他们遇到 [需求/问题] 时，[产品] 是一个 [产品类别]，能够提供 [主要价值]；相比 [替代方案]，它的主要差异是 [核心差异化]。

好的定位应该不需要工程术语也能听懂。

## 产品定义最少要明确

- 产品名称
- 产品类别
- 目标用户
- 目标市场
- 核心场景
- 目标零售价
- 目标 Landed Cost
- 目标 BOM
- 毛利目标
- 销售渠道

## 核心价值不要太多

最好不超过 3 个。

回答：

> **为什么这个产品应该存在？**

## 功能优先级

- MUST：没有就不能成功
- SHOULD：重要竞争能力
- COULD：可有可无
- WON'T：本代明确不做

每一个功能都必须能回答：

**用户问题 → 用户价值 → 商业价值**

否则就要警惕 Feature Creep（功能膨胀）。

---

# 10. PRD：把产品定义变成可执行需求

文件：`templates/PRD-template.md`

仓库中的 PRD 模板包含 26 部分：

1. 产品背景
2. 市场机会
3. 目标用户
4. 使用场景
5. 用户痛点
6. 产品定位
7. 产品目标
8. Non-Goals
9. 功能需求
10. 性能需求
11. UX 需求
12. 工业设计需求
13. 电气需求
14. 固件需求
15. 机械需求
16. 兼容性需求
17. 可靠性需求
18. 安全需求
19. 认证需求
20. 包装需求
21. 成本需求
22. 制造需求
23. 质量需求
24. 上市需求
25. 风险
26. Open Questions

## 写需求最重要的原则

不要写：

> 续航好。

应该写：

> 在定义的典型使用模型下，续航不少于 30 天。

也就是说：

**需求必须尽可能可测量。**

产品经理主要定义 WHAT（需要达到什么）。

工程主要决定 HOW（怎么实现）。

---

# 11. 成本与 BOM：从售价倒推能不能赚钱

文件：`references/cost-and-bom.md`

硬件产品一个非常关键的原则是：

> **不要先把产品做出来，再看卖多少钱。**

应该从目标零售价倒推。

## 成本倒推逻辑

目标零售价

减去：

- 税
- 平台佣金
- FBA / Fulfillment
- 广告预算
- 退货损耗
- 保修
- 包装
- 关税
- 物流
- 目标利润

得到：

**Maximum Acceptable Landed Cost**

再继续倒推：

- Target Ex-Factory Cost
- Target BOM

如果目标成本明显不成立，要在开发前就停止或调整产品。

## 初步 BOM 常见模块

- PCB
- MCU / SoC
- Power
- RF
- Battery
- Mechanical
- UI
- Accessories
- Packaging

特别重要：

**Estimated BOM ≠ Supplier Quoted BOM**

估算成本和供应商正式报价必须分开。

---

# 12. 供应商 RFQ 与供应商选择

文件：`templates/RFQ-template.md`、`references/cost-and-bom.md`

## RFQ 至少要求供应商回复

- MOQ
- 样品费
- 工程费
- 模具费
- 1K / 5K / 10K / 50K 单价
- 包装成本
- Lead Time
- 是否有现成平台
- 可定制内容
- 已有认证
- 付款条件
- 保修支持

还要问清楚：

- 模具归谁
- 固件归谁
- 测试治具归谁
- IP 是否有限制

## 供应商不能只比价格

仓库建议默认权重：

- 技术能力 20%
- 产品质量 20%
- 成本 15%
- 工程支持 15%
- 产能 10%
- 质量体系 10%
- 沟通 5%
- 交付 5%

同时检查：

- 单一供应商风险
- 关键物料风险
- 模具所有权
- 固件所有权
- 测试治具所有权

---

# 13. 硬件研发阶段：Concept → EVT → DVT → PVT → MP

文件：`references/development-gates.md`

完整架构：

**Concept → Feasibility → Prototype → EVT → DVT → PVT → MP**

核心原则：

> **样机能用，不等于可以量产。**

## EVT：Engineering Validation Test

目标：

> 验证工程架构是否真正工作。

重点验证：

- 电子
- PCB
- Firmware
- 机械架构
- Thermal
- RF
- Power
- Charging
- 核心功能

典型退出条件：

> 没有未解决的 P0 工程问题。

## DVT：Design Validation Test

目标：

> 验证最终设计是否满足 PRD。

包括：

- 功能性能
- 可靠性
- 跌落
- 温度
- 湿度
- 电池
- 充电
- RF
- 兼容性
- 材料
- 机械寿命
- UX
- 包装
- 认证

## PVT：Production Validation Test

目标：

> 验证工厂能不能稳定生产。

重点：

- 生产线
- 治具
- SOP
- 作业指导书
- Cycle Time
- Yield
- Calibration
- Firmware 烧录
- SN
- Traceability
- 包装
- QC

核心指标：

- FPY（First Pass Yield）
- Production Yield

## MP：Mass Production

只有产品、工程、质量、供应链、认证和成本都达到要求，才能进入 MP。

---

# 14. DFM、DFT、可靠性与 FMEA

文件：`references/compliance-and-quality.md`

## DFM：Design for Manufacturing

机械重点：

- 壁厚
- 拔模角
- 倒扣
- 卡扣
- 螺丝数量
- 装配方向
- 外观面

电子重点：

- PCB 拼板
- 测试点
- 元器件间距
- SMT 风险
- 接口位置

一个非常实际的问题：

> 能不能少一个装配步骤？

少一步通常意味着：

- 成本更低
- 时间更短
- 出错概率更低

## DFT：Design for Test

量产测试可能包括：

- 开机
- 电流
- 电压
- RF
- Bluetooth
- Wi-Fi
- Charging
- Battery
- Button
- LED
- Sensor
- Audio
- Firmware Version

## 可靠性

按产品情况考虑：

- 跌落
- 振动
- 温度
- 热循环
- 湿度
- USB 插拔
- 按键寿命
- 开关寿命
- 充电循环
- 电池老化
- 线材弯折
- 表面磨损

## FMEA

至少记录：

- Failure Mode
- Effect
- Severity
- Occurrence
- Detection
- Risk

对于关键问题：

**Root Cause → Containment → Corrective Action → Preventive Action**

不要只修表面症状。

---

# 15. 认证与合规

文件：`references/compliance-and-quality.md`

认证不能最后才考虑。

判断方式：

**Product + Technology + Battery + Market**

## 美国可能涉及

- FCC
- UL / ETL（适用时）
- DOE（适用时）

## 欧盟可能涉及

- CE
- RED
- EMC
- LVD
- RoHS
- REACH
- WEEE

## 日本可能涉及

- TELEC / GITEKI
- PSE（适用时）

## 电池相关

- UN38.3
- IEC 62133（适用时）

## 无线充

- Qi / Qi2（适用时）

最终认证要求必须由有资质的实验室或合规专业人士确认。

---

# 16. 决策框架：事实、假设、未知和验证

文件：`references/decision-framework.md`

面对重要产品决策，用下面六步：

## 1. Evidence

我们确定知道什么？

## 2. Assumption

我们正在假设什么？

## 3. Unknown

还有什么不知道？

## 4. Risk

如果假设错了，会损失什么？

## 5. Validation

怎样用最低成本验证？

## 6. Decision

现在应该做什么？

## Assumption Register

把假设分成：

- Confirmed
- Partially Validated
- Unvalidated

优先验证：

**高不确定性 × 高影响**

## Cost of Change 原则

开发阶段越往后，改错成本越高。

所以每进入下一阶段前都问：

> **有什么问题如果现在发现很便宜，但以后发现会非常贵？**

推荐验证顺序：

**Research → Existing Data → User Interview → Competitive Analysis → Supplier Confirmation → Prototype → Engineering Test → Tooling → Production**

---

# 17. 三个关键 Gate

仓库里有三个非常重要的 Checklist。

## Gate 1：Concept Gate

进入正式开发前至少确认：

- 目标用户已定义
- 核心场景已定义
- 核心 JTBD 已定义
- P0 痛点已识别
- 已理解现有替代方案
- 已找到竞争空白
- 已确定目标价格
- 已粗略验证成本可行性
- 已识别主要技术风险
- 已大致确认认证路径
- 已给出 Product Gate 决策

## Gate 2：Design Freeze

冻结设计前确认：

- 核心需求已验证
- 主要 DVT 问题已解决
- 成本可接受
- 模具风险可接受
- 认证路径已确认
- 供应商准备好
- 关键元器件已锁定
- Open Changes 已评审

## Gate 3：MP Readiness

量产前确认：

- PRD Passed
- DVT Passed
- Critical Defects Closed
- PVT Passed
- Yield 达标
- QC Plan 已批准
- 关键物料可供应
- 必要认证已取得
- 成本达标
- 包装已验证
- Traceability 已验证

最后输出：

- `MP READY`
- `MP NOT READY`

---

# 18. 命令速查

## 机会发现阶段

### `/scene-opportunity`

从一个场景寻找产品机会。

### `/VOC`

系统研究用户声音和真实问题。

### `/discover`

研究市场、用户、痛点、竞品和机会空间。

### `/competitors`

做竞品分析。

### `/reviews`

做聚焦式评论研究。

### `/validate`

判断一个具体产品是否值得继续。

## 产品定义与开发

### `/define`

生成产品定义。

### `/prd`

生成 PRD。

### `/spec`

生成硬件规格。

### `/cost`

做售价倒推与成本模型。

### `/bom`

创建初步 BOM。

### `/rfq`

准备供应商询价资料。

### `/supplier`

比较和评估供应商。

### `/evt`

建立 EVT 计划。

### `/dvt`

建立 DVT 测试矩阵。

### `/pvt`

建立 PVT 试产计划。

### `/dfm`

做可制造性 Review。

### `/fmea`

做失效模式风险分析。

### `/cert`

分析认证路径。

### `/risk`

建立风险清单。

### `/mp`

判断是否达到量产条件。

### `/launch`

准备上市。

### `/feedback`

把上市后的评论、退货、售后反馈重新转成产品输入。

### `/next`

当你不知道下一步做什么时，让 Skill 根据当前项目阶段给出优先动作。

---

# 19. 推荐学习路径

如果你把这套 Skill 当作一门“硬件产品开发课程”，建议按下面顺序学习。

## 第一阶段：先学会发现问题

重点阅读：

1. `scene-opportunity-discovery.md`
2. `jobs-to-be-done.md`
3. `voice-of-customer.md`
4. `product-discovery.md`

目标：

> 不再从“我想做什么产品”出发，而是从“用户在哪个场景里有什么任务没有被很好完成”出发。

## 第二阶段：学会做产品决策

重点阅读：

1. `opportunity-scoring.md`
2. `product-definition.md`
3. `decision-framework.md`
4. `concept-gate.md`

目标：

> 学会说 GO，也学会说 NO-GO。

## 第三阶段：学会把产品做成商业项目

重点阅读：

1. `PRD-template.md`
2. `cost-and-bom.md`
3. `RFQ-template.md`
4. Supplier Scorecard

目标：

> 把产品价值、规格、成本和供应商能力连起来。

## 第四阶段：学会真正把硬件量产出来

重点阅读：

1. `development-gates.md`
2. EVT / DVT / PVT 模板
3. `compliance-and-quality.md`
4. FMEA
5. Design Freeze Checklist
6. MP Readiness Checklist

目标：

> 理解“有样机”和“能量产”之间巨大的差别。

---

# 20. 一条完整的新品开发流程

如果今天从 0 开始寻找一个消费电子产品，可以这样跑：

## Step 1：选择场景

例如：

> 美国 × 家庭卧室 × 床头柜

运行：

`/scene-opportunity`

输出：

- 用户
- 行为
- JTBD
- 摩擦
- workaround
- 产品机会池

## Step 2：研究 VOC

运行：

`/VOC`

输出：

- Raw VOC
- Problem Coding
- Problem Clusters
- Top Problems
- Evidence Strength

## Step 3：机会排序

判断：

- 用户价值
- 差异化
- 技术可行性
- 成本可行性
- 经济性
- 证据强度

取 Top 1–3。

## Step 4：产品验证

运行：

`/validate`

得到：

- GO
- CONDITIONAL GO
- NO-GO

## Step 5：产品定义

运行：

`/define`

确定：

- 用户
- 场景
- 价值
- 价格
- 核心规格
- MUST / SHOULD / COULD / WON'T

## Step 6：写 PRD 和规格

运行：

- `/prd`
- `/spec`

## Step 7：成本与供应商

运行：

- `/cost`
- `/bom`
- `/rfq`
- `/supplier`

## Step 8：开发验证

按顺序：

**Prototype → EVT → DVT → Design Freeze → PVT**

## Step 9：量产判断

运行：

`/mp`

只有所有 Blocker 关闭，才进入 MP。

## Step 10：上市反馈闭环

运行：

- `/launch`
- `/feedback`

把：

**评论 → 退货 → 售后 → 故障 → 用户 workaround**

重新进入 VOC。

这样就形成：

**市场 → 产品 → 开发 → 量产 → 上市 → 用户反馈 → 下一代产品**

---

# 最后记住 6 句话

1. **不要从功能开始，从场景和 Job 开始。**
2. **用户说的功能，不一定是用户真正的问题。**
3. **有痛点，不等于有产品机会。**
4. **有样机，不等于能量产。**
5. **能做出来，不等于能赚钱。**
6. **越晚发现错误，硬件项目付出的成本越高。**

如果把这六句话真正用到每一个新品项目里，这套 Skill 才真正发挥价值。

---

# 仓库文件与本手册对应关系

## 核心入口

- `SKILL.md`
- `README.md`

## 方法论

- `references/scene-opportunity-discovery.md`
- `references/jobs-to-be-done.md`
- `references/voice-of-customer.md`
- `references/opportunity-scoring.md`
- `references/product-discovery.md`
- `references/product-definition.md`
- `references/decision-framework.md`
- `references/cost-and-bom.md`
- `references/development-gates.md`
- `references/compliance-and-quality.md`

## 常用模板

- `templates/PRD-template.md`
- `templates/product-definition-template.md`
- `templates/RFQ-template.md`
- `templates/EVT-template.md`
- `templates/DVT-template.md`
- `templates/PVT-template.md`
- `templates/BOM-template.csv`
- `templates/FMEA-template.csv`
- `templates/risk-register-template.csv`
- `templates/supplier-scorecard-template.csv`
- `templates/change-log-template.csv`
- `templates/VOC-raw-data.csv`
- `templates/VOC-coding.csv`
- `templates/problem-ranking.csv`
- `templates/opportunity-backlog.csv`
- `templates/scene-map.csv`
- `templates/problem-space.csv`
- `templates/opportunity-ranking.csv`

## Gate Checklist

- `checklists/concept-gate.md`
- `checklists/design-freeze.md`
- `checklists/mp-readiness.md`

---

**建议使用方式：先通读本手册建立整体框架，再回到对应 reference 和 template 练习具体项目。**
