# 硬件产品经理学习手册（V2）

> 基于本仓库 `hardware-product-manager-skill` 整理。
> 本版新增“场景战略 → 场景价值判断 → 场景驱动产品设计”，只吸收与产品开发直接相关的方法，不把营销文案方法混入产品决策。

---

# 一、这套 Skill 是做什么的

这套 Skill 的目标不是帮你“写更多文档”，而是让 AI 按照高级硬件产品经理 + NPI 负责人的方式参与消费电子产品开发。

完整链路：

**场景战略 → 场景机会发现 → VOC + 竞争情报 → 市场机会 → 产品验证 → 产品定义 → 场景需求映射 → PRD → 硬件规格 → 成本/BOM → 供应商 RFQ → EVT → DVT → PVT → 认证 → MP → 上市 → 用户反馈闭环**

核心目标：

> 提高发现并推出一个用户需要、有差异化、技术可行、成本可行、能量产、符合认证要求并且能赚钱的硬件产品的概率。

---

# 二、最重要的主线

新版主线是：

**场景 → 用户 → 行为 → JTBD → VOC + 竞争证据 → 问题 → 未满足需求 → 机会 → 产品 → 竞争定位 → 场景需求 → 规格 → 成本 → 工程 → 制造 → 市场 → 用户反馈 + 竞争变化 + 场景变化**

其中最重要的变化是：

1. 场景不再只是 PRD 里的一个字段。
2. 场景本身要被研究、分类、验证。
3. 用户证据和竞争证据必须并行。
4. 场景必须被翻译成可测量的产品要求。
5. 市场传播不能反过来制造不存在的产品需求。

---

# 三、两个项目入口

## 模式 A：还不知道做什么产品

从场景出发：

`/scene-opportunity`

流程：

**场景 → 用户活动 → JTBD → VOC + 竞品 → 场景价值判断 → 未满足需求 → Opportunity Space → 候选产品 → 排名 → `/validate`**

例如：

> 美国 × 家庭卧室 × 床头

不要立刻脑暴“无线充、闹钟、夜灯”。

先研究：

- 谁在这里
- 什么时候进入这个场景
- 做什么动作
- 多久发生一次
- 哪些任务最重要
- 哪些地方反复失败
- 用户如何 workaround
- 现有竞品是否已经解决

## 模式 B：已经有产品想法

例如已经决定研究无线充：

**场景定义 → `/VOC` + `/competitors` → `/validate` → `/define` → 场景需求映射 → `/prd` → `/spec` → 后续开发**

---

# 四、场景不是一个词，而是一组变量

场景定义至少包含：

- 市场 / 国家
- 用户群
- 地点
- 时间 / 时机
- Trigger 触发点
- 行为顺序
- 频次
- 期望结果
- 环境约束
- 当前解决方案
- 摩擦 / 失败

其中建议重点看四个变量：

## 1. 时机 Timing

需求什么时候被激活？

例如：

> 睡觉前 5 分钟，而不是“全天”。

## 2. 场合 Occasion / Place

用户在哪里、周围环境如何？

例如卧室意味着：

- 黑暗
- 安静
- 伴侣可能已睡
- 用户不愿做复杂操作

## 3. 动作 Action

用户实际在做什么？

例如：

> 拿手机 → 放到充电器 → 看屏幕确认 → 熄灯 → 睡觉。

## 4. 频次 Frequency

每天、每周、偶尔还是一年一次？

频率会直接影响产品机会大小和购买价值。

---

# 五、场景也要分级

不是每个场景都应该进入产品定义。

## Core Scene 核心场景

产品最应该解决的场景，也是“为什么这个产品应该存在”的主要答案。

例如卧室无线充的核心场景可能是：

> 睡前把手机放下，不需要反复确认，第二天可靠有电。

## Supporting Scene 支撑场景

能扩展使用价值，但不能破坏核心产品。

例如：

> 白天放在家庭书桌临时补电。

## Lead / Beachhead Scene 引线 / 滩头场景

一群对问题特别敏感、特别容易成为首批用户的人。

它适合帮助找到初始目标用户，但不能自动代表整个大众市场。

## Extreme Scene 极限场景

用来暴露工程极限。

例如：

- 高温环境
- 厚手机壳
- 极端角度
- 高频插拔

极限场景更适合产生可靠性和工程要求，而不是直接决定大众产品功能。

## Reject

场景真实存在，但频率低、价值弱、竞争已经解决或成本不值得，因此不让它影响产品。

---

# 六、如何判断一个场景值不值得做

新版 Skill 使用概念模型：

**Scene Opportunity = Frequency × Job Importance × Problem Severity × Dissatisfaction × Competitive Gap × Solvability × Economics**

不需要硬凑一个精确数字；信息不足时用 High / Medium / Low / Unknown。

重点问：

- 需求会不会稳定出现？
- 用户动作是否重复？
- 失败是否真的烦、贵、危险或影响结果？
- 当前方案是否明显不好？
- 用户有没有自己花时间或钱 workaround？
- 竞品在这个具体场景里是否仍有明显缺口？
- 我们是否能低复杂度解决？
- 市场规模和商业模式是否支持？

---

# 七、JTBD：不要把产品写成任务

标准句式：

> 当……的时候，我想要……，这样我就可以……。

错误：

> 我想要一个磁吸无线充。

正确：

> 当我睡前把手机放下时，我想让它不用仔细对位就能可靠开始充电，这样我不用反复确认就可以直接睡觉。

一个好的 Job 描述解决的是用户目标，不预设具体技术方案。

---

# 八、VOC：从真实声音里找问题

VOC 流程：

**Raw Voice → Context → Problem Code → Problem Cluster → Frequency → Severity → Current Solution → Workaround → Root-Cause Hypothesis → Opportunity → Validation**

主要来源：

- Amazon / 电商评论
- Q&A
- Reddit / 论坛
- 客服
- 退款 / 退货
- 用户访谈
- 观察真实使用
- 已有产品数据

证据等级：

- `[DATA]`：真实用户声音
- `[PATTERN]`：多个独立来源重复
- `[HYPOTHESIS]`：推测出的根因或底层需求
- `[VALIDATED]`：被进一步验证

不能把 AI 的推理直接叫“已验证需求”。

---

# 九、竞争对手必须贯穿全周期

用户证据回答：

> 用户哪里不满意？

竞争证据回答：

> 这个问题现在市场已经解决到什么程度？

因此：

**用户有痛点 ≠ 有产品机会。**

真正的机会更接近：

**User Importance × User Dissatisfaction × Competitive Gap × Solvability × Economics**

竞品要覆盖：

- 直接竞品
- 间接竞品
- 替代行为
- 新兴方案

维护一个 5–10 款左右的 Benchmark Set，并持续更新。

---

# 十、不要只做规格表，要做“场景竞品 Benchmark”

普通竞品表：

> A 15W、B 15W、C 25W。

场景 Benchmark：

> 在同一个卧室睡前场景里，谁更容易对位？谁更安静？谁的灯最不打扰？谁最稳定？谁能单手取放？

可以比较：

- Task Success
- 操作步骤
- 完成时间
- Reliability
- Noise
- Heat
- LED / Visibility
- Placement Tolerance
- Compatibility
- One-hand Interaction
- Occupied Space

真正的竞争差异不是“多一个功能”，而是在用户重要场景中产生更好的结果。

---

# 十一、产品机会怎么判断

先判断问题机会，再判断产品机会。

## Level 1：Problem Opportunity

看：

- Frequency
- Severity
- Importance
- Current Satisfaction
- Workaround
- WTP Signal
- Evidence Strength

## Level 2：Product Opportunity

看：

- User Value
- Differentiation
- Technical Feasibility
- Cost Feasibility
- Margin Potential
- Manufacturing Feasibility
- Compliance Feasibility
- Channel Fit
- Competitive Defensibility

最终 Top 1–3 再进入 `/validate`。

---

# 十二、Product Gate

重大投入前至少判断：

- Desirability
- Scene Fit
- Differentiation
- Competitive Gap
- Technical Feasibility
- Cost Feasibility
- Margin Feasibility
- Manufacturing Feasibility
- Certification Feasibility

结论只能是：

- GO
- CONDITIONAL GO
- NO-GO

不能默认 GO。

---

# 十三、产品定义

产品定义至少明确：

- 产品类别
- 目标用户
- 目标市场
- Core Scene
- Supporting Scene
- Lead Scene
- Target Price
- Target Landed Cost
- Target BOM
- Launch Channel
- 核心价值（不超过 3 个）

功能优先级：

- MUST
- SHOULD
- COULD
- WON'T

每一个功能必须回答：

**用户问题 → 用户价值 → 商业价值**

---

# 十四、新增核心方法：Scene Requirement Mapping

这是新版最重要的产品开发桥梁之一。

不能从：

> 场景 = 卧室

直接跳到：

> 所以做一个夜间模式。

正确转换链是：

**Scene → Job → Friction / Failure → Desired Outcome → Product Principle → Requirement → Test Method**

例如：

**Scene**：黑暗卧室睡前充电

↓

**Job**：放下手机后直接睡觉

↓

**Friction**：持续亮灯影响睡眠

↓

**Desired Outcome**：确认充电后环境恢复黑暗

↓

**Product Principle**：仅在必要时提供状态反馈

↓

**Requirement**：开始充电后状态灯在定义时间内自动熄灭

↓

**Test Method**：DVT 夜间指示灯行为测试

这样，场景才真正进入工程开发。

---

# 十五、场景如何变成硬件规格

示例：

- 安静卧室 → Acoustic Noise Requirement
- 黑暗卧室 → LED Brightness / Timeout Requirement
- Travel → Size / Weight / Cable Storage
- One-hand Use → Base Stability / Removal Force
- Outdoor → IP / Temperature / Drop
- 睡前操作 → Steps / Confirmation Time / Alignment Tolerance

不要在 PRD 里留下“适合卧室”“操作方便”“高级感好”这种无法验收的表述。

必须转换成可验证的行为或指标。

---

# 十六、发生规格冲突时，优先保护什么

顺序：

1. Core Scene
2. Category Entry Requirement
3. Must-Win
4. Must-Match
5. Supporting Scene
6. Nice-to-have

不要为了让所有场景都能用，最后做出一个每个场景都不够好的产品。

---

# 十七、PRD

PRD 应覆盖：

- 背景
- 市场机会
- 用户
- 场景
- 痛点
- 定位
- Goals / Non-Goals
- Functional Requirements
- Performance
- UX
- ID
- Electrical
- Firmware
- Mechanical
- Compatibility
- Reliability
- Safety
- Certification
- Packaging
- Cost
- Manufacturing
- Quality
- Launch
- Risk
- Open Questions

新增建议：

> 重要项目附一张 `Scene Requirement Matrix`。

---

# 十八、竞争属性分类

每个关键规格不要只问“竞品有没有”，而要分类：

## Category Entry Requirement

没有就会被市场淘汰。

## Must Match

至少达到主流水平。

## Must Win

这是本产品明确要赢的地方。

## Acceptable Lag

可以弱一点，不影响购买理由。

## Irrelevant

用户不在意，不要浪费成本。

这能有效抑制 Feature Creep。

---

# 十九、成本与 BOM

从售价倒推，而不是先把东西做出来。

Retail Price

减去：

- 税
- 平台费
- Fulfillment
- 广告
- 退货
- 保修
- 包装
- Duty
- Logistics
- Target Profit

得到：

**Maximum Acceptable Landed Cost**

再倒推：

- Target Ex-Factory Cost
- Target BOM

必须区分：

**Estimated BOM ≠ Supplier Quoted BOM**

---

# 二十、供应商与 RFQ

RFQ 至少问：

- MOQ
- Sample Cost
- Engineering Fee
- Tooling
- 1K / 5K / 10K / 50K Price
- Packaging
- Lead Time
- Existing Platform
- Customization
- Certification Status
- Payment Terms

并确认：

- Tooling Ownership
- Firmware Ownership
- Fixture Ownership
- IP Restriction

供应商评价不能只看价格。

---

# 二十一、EVT / DVT / PVT 如何加入场景

## EVT

问：

> 工程架构能不能支持 Core Scene 的关键要求？

例如卧室充电：

- 散热方案是否会产生噪音？
- LED 能否按需求控制？
- 对位结构是否稳定？

## DVT

问：

> 最终设计在代表性 Core Scene 中是否真正达到要求？

不仅测实验室参数，还应做场景化测试。

并且 Must-Win 必须与 Benchmark Product 在相近条件下比较。

## PVT

问：

> 工厂能否稳定生产出持续满足这些场景关键要求的产品？

例如：

- 每批磁力一致性
- LED 亮度一致性
- 风扇 / 噪音一致性
- 充电性能一致性

---

# 二十二、Design Freeze 之前

至少确认：

- Core Scene 已验证
- 场景关键需求已写入 PRD
- Must-Win 有测试证据
- Major DVT Issue 已解决
- 成本可接受
- Tooling Risk 可接受
- Certification Path 已确认
- Supplier Ready
- Critical Components 已锁定

如果 Core Scene 还没有验证，不应该因为进度压力就 Freeze。

---

# 二十三、认证与质量

认证按：

**Product + Technology + Battery + Market**

考虑：

- FCC
- UL / ETL（适用时）
- CE / RED / EMC / LVD
- RoHS / REACH / WEEE
- TELEC / GITEKI
- PSE
- UN38.3
- IEC 62133
- Qi / Qi2

最终要求应由实验室或合规专业人士确认。

质量方面继续使用：

- DFM
- DFT
- Reliability
- FMEA

---

# 二十四、决策框架

重大决策都问：

## Evidence

知道什么？

## Assumption

假设什么？

## Unknown

不知道什么？

## Risk

错了损失什么？

## Validation

如何便宜地验证？

## Decision

现在应该做什么？

优先验证：

**High Uncertainty × High Impact**

并始终遵守：

> 越晚发现错误，硬件修改成本越高。

---

# 二十五、推荐命令顺序

## 不知道做什么产品

`/scene-opportunity`

↓

`/VOC + /competitors`

↓

`/discover`

↓

机会排序

↓

`/validate`

## 已经有产品

场景定义

↓

`/VOC + /competitors`

↓

`/validate`

↓

`/define`

↓

Scene Requirement Matrix

↓

`/prd + /spec`

↓

`/cost + /bom`

↓

`/rfq + /supplier`

↓

EVT → DVT → PVT → MP

↓

`/feedback`

---

# 二十六、一个无线充例子

场景：

> 美国家庭卧室，用户睡前把手机放到床头充电。

不要直接定义：

> 15W、LED、提示音。

先拆：

**Timing**：睡前

**Place**：黑暗安静的卧室

**Action**：放手机 → 确认 → 睡觉

**Frequency**：每天

**Job**：第二天可靠有电

**Friction**：对位、灯光、噪音、发热、掉充

然后用 VOC 确认哪些是真问题，再看竞品有没有解决。

如果最后发现：

- 磁吸对位已经是市场标配
- 夜间灯光仍有用户 workaround
- 高功率产品出现噪音/热问题

那么产品机会就不应该是：

> “再做一个 15W 无线充。”

而可能是：

> **针对卧室 Core Scene 优化的 Reliable + Dark + Silent Charging。**

然后再把这个价值拆成可测试规格。

---

# 二十七、最后记住 9 句话

1. **不要从功能开始，从场景和 Job 开始。**
2. **场景不是一个地点，而是时机、场合、动作、频次和约束的组合。**
3. **不是每个场景都值得进入产品定义。**
4. **用户有痛点，不等于市场有机会。**
5. **VOC 与竞争证据必须一起看。**
6. **场景必须最终翻译成可测试的 Requirement。**
7. **核心场景优先于功能堆叠。**
8. **有样机不等于能量产；能量产不等于能赚钱。**
9. **越晚发现错误，硬件项目付出的成本越高。**

---

# 新版重点文件

## 场景方法

- `references/scene-strategy.md`
- `references/scene-value-evaluation.md`
- `references/scene-opportunity-discovery.md`
- `references/scene-product-design.md`
- `references/jobs-to-be-done.md`

## 用户与竞争证据

- `references/voice-of-customer.md`
- `references/competitive-intelligence.md`
- `references/competitive-benchmarking.md`
- `references/opportunity-scoring.md`

## 产品开发

- `references/product-discovery.md`
- `references/product-definition.md`
- `references/cost-and-bom.md`
- `references/development-gates.md`
- `references/compliance-and-quality.md`
- `references/decision-framework.md`

## 新增场景模板

- `templates/scene-definition.csv`
- `templates/scene-value-scorecard.csv`
- `templates/scene-competitor-benchmark.csv`
- `templates/scene-requirement-map.csv`

## 其他关键模板

- `templates/VOC-raw-data.csv`
- `templates/VOC-coding.csv`
- `templates/problem-ranking.csv`
- `templates/opportunity-ranking.csv`
- `templates/competitive-benchmark.csv`
- `templates/PRD-template.md`
- `templates/BOM-template.csv`
- `templates/RFQ-template.md`
- `templates/EVT-template.md`
- `templates/DVT-template.md`
- `templates/PVT-template.md`
- `templates/FMEA-template.csv`

---

**建议学习顺序：先学 Scene Strategy → JTBD → VOC → Competitive Intelligence → Opportunity → Product Definition → Scene Requirement Mapping，再学习成本、供应商和 EVT/DVT/PVT。**
