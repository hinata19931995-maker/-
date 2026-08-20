# 竞争情报与竞品 Benchmark 学习章节

> 本文是 `hardware-product-manager-study-guide-zh.md` 的补充章节，解释为什么竞争对手研究必须贯穿整个硬件产品生命周期。

## 1. 为什么竞争研究不是一次性工作

用户研究告诉我们：

> 用户在哪里遇到问题。

竞争研究告诉我们：

> 这些问题目前已经被市场解决到什么程度。

因此：

**用户有痛点 ≠ 市场一定存在机会。**

一个更完整的产品机会判断是：

**产品机会 = 用户重要性 × 用户不满意度 × 竞争空白 × 可解决性 × 商业经济性**

这个公式用于思考，不用于制造虚假的精确分数。

---

## 2. 两条证据线

### 用户证据线

**场景 → JTBD → VOC → 问题 → workaround → 未满足需求**

### 竞争证据线

**竞品 → 替代方案 → 定位 → 价格 → 规格 → 评论 → 技术 → Benchmark 实测 → 市场变化**

两个证据线必须在重要产品决策前汇合。

---

## 3. 竞品不只是直接竞品

至少研究：

1. 直接竞品
2. 间接竞品
3. 替代产品
4. 替代行为
5. 新兴技术
6. 可能进入该任务空间的邻近品类

例如研究卧室无线充时，替代方案不仅是另一台无线充，还可能包括 USB-C 线充、多口充电器、带充电功能的床头家具、MagSafe/Qi2 配件等。

---

## 4. 建立 Benchmark Product Set

每个项目建议维护约 5–10 款有代表性的基准产品。

可以包含：

- Market Leader：市场领导者
- Price Leader：价格领导者
- Feature Leader：功能领导者
- Design Leader：设计领导者
- Best Rated：用户满意度较高产品
- Emerging Challenger：新兴挑战者
- Direct Substitute：直接替代方案

选择 Benchmark 的原则不是“品牌有名”，而是：

> **它能不能回答我们正在面对的产品决策问题。**

---

## 5. 不同阶段，研究竞争对手的目的不同

### 场景机会发现

研究：

- 用户现在用什么产品
- 哪些任务已经被很好解决
- 哪些任务需要多个产品拼起来完成
- 哪些 workaround 说明存在空白

### VOC

研究：

- 竞品反复被抱怨什么
- 竞品反复被赞扬什么
- 哪些问题已经有竞品解决得很好

### `/validate`

判断：

- 市场是否过度拥挤
- 差异化是否真的有意义
- 竞争对手是否很容易复制
- 价格和利润是否成立

### `/define`

把产品属性分成：

- Category Entry Requirement：进入市场的基础门槛
- Must Match：必须达到主流水平
- Must Win：必须明显领先
- Acceptable Lag：可以弱一些
- Irrelevant：不值得投入

### PRD / Spec

把竞品能力变成可测量的 Benchmark，例如：

- 充电时间
- 温升
- 噪音
- 续航
- 延迟
- RF 距离
- 重量
- 尺寸
- 对位成功率
- 兼容性
- 单手操作

### Cost / BOM

用市场价格和竞品架构挑战自己的：

- 售价
- Landed Cost
- BOM
- 配件
- 包装

但没有可靠证据时，不能把竞品 BOM 或工厂成本说成事实。

### Supplier / RFQ

问供应商：

- 是否有类似成熟平台
- 哪些功能是标准方案
- 哪些必须定制
- Benchmark 功能增加多少成本
- 模具和认证影响是什么

### EVT / DVT

真正拿 Benchmark 产品做受控测试。

DVT 要回答：

- Category Entry 是否达到
- Must Match 是否达到
- Must Win 是否真的赢
- Acceptable Lag 是否仍然可接受

如果 Must Win 无法证明：

> 要么改产品，要么改定位。

### Launch

上市前重新检查：

- 当前价格
- 促销
- 新型号
- 新卖点
- 评论变化
- 规格变化

### Post-launch

持续观察：

- 新竞品
- 新协议
- 降价
- 差异化被复制
- 新用户抱怨

然后进入下一代产品。

---

## 6. 五种竞争要求分类

### Category Entry Requirement

用户已经默认期待的基础能力。

缺失会直接造成购买拒绝。

### Must Match

需要达到市场主流水平，但不必领先。

### Must Win

与产品定位直接相关，必须明显胜出。

### Acceptable Lag

可以弱一点，因为不是核心价值。

### Irrelevant

用户不在意，也不支持核心定位，不应该继续花成本。

这套分类可以防止产品经理陷入：

> “竞品有，所以我们也要有。”

---

## 7. Benchmark 测试纪律

做实物竞品 Benchmark 时，尽量做到：

- 相同测试设备
- 相同电源条件
- 相同环境温度
- 相同起始状态
- 相同测试时长
- 必要时重复测试
- 记录 Firmware / Software Version
- 记录测试方法和仪器

不能把不同测试方法得到的数据直接横向比较，却不给任何说明。

---

## 8. 竞争空白的类型

可以把 Competitive Gap 分成：

- Performance Gap
- Reliability Gap
- UX Gap
- Scenario Gap
- Price / Value Gap
- Design Gap
- Compatibility Gap
- Ecosystem Gap
- Service / Warranty Gap
- Manufacturing / Quality Gap

但真正值得做的 Gap 必须同时满足：

> **用户在意 + 现有方案没有解决好 + 我们有能力解决 + 商业模型成立。**

---

## 9. 一个无线充例子

假设 VOC 发现：

> 用户觉得 LED 太亮。

第一反应不能直接是：

> 加一个 LED 关闭按钮。

先看竞品：

- A：LED 常亮
- B：几秒后自动熄灭
- C：无常亮 LED

如果大量同价位竞品已经自动熄灯，那么“自动熄灯”只是 Category Entry Requirement，而不是差异化。

继续研究也许发现：

- 15W 产品安静但慢
- 25W 产品快但风扇明显
- 高端产品解决散热，但价格很高

这时候真正的机会可能是：

> **中低价位、适合卧室的安静低温 Qi2 产品。**

这就是 VOC 与 Competitive Intelligence 结合后的价值。

---

## 10. 在本 Skill 中如何使用

### `/competitors`

现在不再只是一次性竞品表。

它应该根据项目阶段输出：

1. 研究范围
2. 竞品宇宙
3. Benchmark Product Set
4. 定位地图
5. 价格 / 价值地图
6. 功能和规格对比
7. 用户好评 / 差评对比
8. Category Entry Requirements
9. Must Match / Must Win / Acceptable Lag
10. Competitive Gaps
11. 替代威胁
12. 证据质量和未知项
13. 对产品定义的影响
14. 下一步竞争验证

常用模板：

- `templates/competitor-landscape.csv`
- `templates/competitive-benchmark.csv`
- `templates/competitive-change-log.csv`

核心参考：

- `references/competitive-intelligence.md`
- `references/competitive-benchmarking.md`

---

# 最重要的四句话

1. **用户有痛点，不代表市场有机会。**
2. **竞品有功能，不代表我们也必须有。**
3. **真正的差异化必须同时得到用户证据和竞争证据支持。**
4. **竞争研究应该从机会发现一直持续到下一代产品，而不是做完一张竞品表就结束。**
