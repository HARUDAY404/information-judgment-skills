# Information Judgment Skills

这是一套帮你“少看一点，想清楚一点”的 AI 工作流。

它不替你做判断，也不鼓励把更多信息囤积进知识库。它要解决的是三个很具体的问题：

- 每天信息太多，到底哪几条值得看？
- 一个说法看起来很有道理，证据究竟到了哪一步？
- 看完别人的观点后，怎样留下并改进自己的判断？

## 四个 Skill 分别做什么

### 1. Information Radar：先决定什么值得看

围绕你当前真正关心的问题寻找信息，合并重复内容，排除没有新增量的噪声，最后只留下少量值得继续看的线索。

它回答的是“值不值得占用你的注意力”，不是“这件事是不是真的”。

### 2. Judgment Journal：在被 AI 影响前，先留下你的想法

当某条信息值得深究时，先记下你此刻的判断、理由、置信度和可能错在哪里。可以不确定，也可以记为“尚未形成判断”。

这一步必须发生在 AI 给出详细分析之前，否则“你的判断”很可能只是被 AI 锚定后的反应。

### 3. Claim Auditor：再查这个说法站不站得住

把一段话拆成可检查的主张，找到尽可能原始的来源，检查方法、样本和利益关系，再主动寻找反证、失败案例和其他解释。

它不是给博主贴上“可信”或“不可信”的永久标签，而是说明：现有证据最多支持到什么程度。

### 4. Content Lab：有需要时，再把判断变成内容实验

当你确实想公开表达时，把经过审计的判断转成面向某类读者的内容假设。发布前说清想验证什么，发布后再根据真实反馈调整。

流量只能说明内容在某些条件下引起了反应，不能证明中心主张是真的。

## 正确的使用顺序

```text
外部信息
   ↓
Information Radar：值得继续看吗？
   ↓
Judgment Journal（审计前）：我现在怎么看？
   ↓
Claim Auditor：证据究竟支持到哪里？
   ↓
Judgment Journal（审计后）：我要不要修改判断？
   ├── 进入行动或知识库
   └── 可选：Content Lab，变成公开内容实验
```

Content Lab 不是必经步骤。如果你只想少看噪声、提高判断质量，前三个 Skill 就足够。

## 一个最小使用示例

先对 Radar 说：

```text
使用 $information-radar。
过去 7 天，帮我查看“AI 正在如何改变个人知识管理”。
标准模式，最多 5 条。优先原始项目、真实实践和失败案例，排除重复转载和纯营销。
```

选中一条后，在看 AI 的深度评价前先说：

```text
使用 $judgment-journal，只保存我的审计前快照，先不要反驳我。
我的初始判断是……，置信度是……，我最可能错在……
```

然后在一个看不到上述判断的新任务或独立上下文中说：

```text
使用 $claim-auditor 审计这条主张。
这是对应的问题和材料，编号是……。请追溯原始来源、寻找反证，并告诉我现有证据最多支持到什么程度。
```

最后回到 Judgment Journal，打开先前封存的快照并追加修订判断，不要覆盖原记录。若只能在同一个上下文内完成，就注明“非盲审”。

## 如何安装

在 Codex 中，把需要的完整 Skill 目录复制到 `~/.codex/skills/`。每个目录内的 `SKILL.md` 和 `references/` 都要保留。

其他工具如果不支持 Agent Skills，可以把对应的 `SKILL.md` 当作工作流指令。定时监测、平台抓取、历史存储和知识库同步需要额外的工具或自动化，不是 Skill 文件本身就能完成的。

## 7 天试运行

第一周不追求“自动化程度”，只看它有没有真正帮你减轻信息负担。

- Radar 每天最多留 5 条，没有有价值的内容就输出 0 条。
- 每天最多深度审计 1 条。
- 不强迫自己对每条信息形成观点。
- Content Lab 只在你真的准备表达时使用，不必日更。
- 第 7 天复盘：每天花费时间、噪声数量、真正改变判断的次数，以及促成行动的次数。

## 几条不能丢的原则

- 问题优先，博主和平台只是信源。
- 同一来源的多次转载，不算多份独立证据。
- 审计具体主张，不给一个人贴永久的可信度标签。
- 保留原始链接、反证、未知和历史修订。
- 点击、点赞和转发是传播反馈，不是真实性证据。
- AI 可以整理材料和充当反方，但不能冒充你的原始判断。
- 评分规则不允许系统静默改写；修改后要用同一批案例重新测试。

## 这套方法有科学依据吗？

严谨的回答是：**部分机制有研究支持，但“四个 Skill 组合起来一定有效”还没有被直接证明。**

因此，这个项目应该被称为“受研究启发、可以检验的工作流原型”，而不是“经过科学验证的信息判断系统”。引用论文的作用，是说明设计选择并非凭空想象；它们不能替这个项目完成尚未做过的对照实验。

现有研究能支持的主要是以下设计原则：

- **主动考虑相反解释，通常比只提醒自己保持客观更有效。** Lord 等人的实验发现，`consider the opposite` 策略能减少偏向性的信息吸收；但 Koslowski 等人的研究也提醒，只顾反驳同样会误判中性证据。因此 Claim Auditor 同时检查支持证据、反证和其他解释，而不是机械地“唱反调”。
- **先写下判断并保留历史，有助于减少事后改写记忆。** 关于锚定、确认偏误和后见之明的研究表明，人会无意间受已有观点和结果影响。因此 Journal 保存审计前快照且不覆盖旧版本。不过，初始判断本身也可能成为新的锚点，所以最好将它封存，让 Auditor 在看不到立场的情况下独立审计。
- **置信度不是证据强度。** 研究发现，高置信度可能让人更主动搜集支持原有选择的信息，并降低对反证的敏感度。因此本项目把“我的置信度”和“证据质量”分开记录。
- **预测、反馈和长期记分可以训练校准。** Good Judgment Project 的研究表明，训练、协作、持续追踪和反馈能改善概率预测表现。但这不等于记日记本身必然提升所有领域的判断。
- **一个工作流能运行，不等于它有效。** Google 关于机器学习生产准备度和数据验证的研究，以及 OpenAI 的评估实践，都强调固定测试集、真实案例、边界案例、持续评估和人工复核。四个 Skill 也应该接受同样的检验。

## 研究没有替我们证明什么

- 没有证明四个 Skill 比一个写得好的普通提示词更有效。
- 没有证明当前评分阈值具有统计效度；数字只是操作性规则，不是客观真理。
- 没有证明 7 天试运行能提升长期判断力。7 天只能检查它是否易用、是否减轻负担。
- 没有证明 AI 可以独立、公正地审计用户观点。同一个模型既听过你的立场又负责审计，可能产生迎合或确认偏误。
- 没有证明点赞、收藏或转化能反映内容真实性。它们只能评价传播表现。

## 按科学原则使用：先做一个小型对照测试

不要一开始就证明“它有用”，而要设计一个允许它失败的测试。

### 1. 先定义目标和失败条件

目标只保留两个：减少无效信息消耗；提高判断过程的可追溯性与校准度。开始前写下可观察指标，例如每周阅读耗时、误收噪声、漏掉的重要信息、原始来源追溯率、审计后改变判断的次数，以及到期预测的校准情况。

### 2. 建立一组固定案例

先收集 25 个不随测试结果改变的案例：可靠信息、看似权威但夸大的说法、营销内容、真实但不可泛化的个案、证据确实有争议的问题，各 5 个。保存原文、时间和当时可获得的证据，形成一个小型“冻结测试集”。

### 3. 做最小基线对照

将同一批案例分别交给：

- 普通 AI 提问，不加载这四个 Skill；
- 当前四 Skill 工作流。

比较耗时、重复信息、原始来源追溯、反证覆盖、错误接受、重要遗漏和结论边界。条件允许时打乱顺序，并请一个不知道输出来自哪组的人复核，避免只挑自己喜欢的答案。

### 4. 对重要判断采用“封存后盲审”

先用 Journal 保存初始判断，但不给 Auditor 看内容；Auditor 只接收问题、材料和编号。审计结束后再打开快照，记录判断是否改变。如果无法隔离上下文，必须注明“非盲审”，不能把 AI 与你一致当成独立验证。

### 5. 修改规则必须留版本

评分、来源权重、提示词或筛选阈值发生变化时，记录版本和修改理由，再用同一冻结测试集重跑。不要只展示改得更好的案例，也要记录退步和失败案例。

### 6. 分开两种反馈

事实层反馈用于修改证据判断：新原始资料、反证、预测结果。传播层反馈用于修改表达：完读、评论、收藏和转化。Content Lab 可以根据传播反馈改写表达，但不能据此抬高主张的真实性。

## 对外介绍时可以怎么说

可以说：

> 这是一套受确认偏误、反向思考、判断校准和持续评估研究启发的信息工作流。各机制有相关证据，但四 Skill 的整体效果仍需通过固定案例和对照测试持续验证。

不应该说：

> 这是一套已经被科学证明、能够提高判断力的系统。

## 参考研究与工程实践

- Charles G. Lord, Mark R. Lepper, Elizabeth Preston（1984），[Considering the opposite: a corrective strategy for social judgment](https://pubmed.ncbi.nlm.nih.gov/6527215/)。
- Barbara Koslowski 等（2013），[A disconfirming strategy is not necessarily better than a confirming strategy](https://pubmed.ncbi.nlm.nih.gov/24027947/)。
- Peter Kaanders 等（2022），[Humans actively sample evidence to support prior beliefs](https://pubmed.ncbi.nlm.nih.gov/35404234/)。
- Max Rollwage 等（2020），[Confidence drives a neural confirmation bias](https://pubmed.ncbi.nlm.nih.gov/32457308/)。
- Timothy D. Wilson 等（1996），[A new look at anchoring effects](https://pubmed.ncbi.nlm.nih.gov/8945789/)。
- Amy Bradfield Douglass、Gary L. Wells（2005），[Revisiting the role of hindsight bias in evaluations of expert testimony](https://pubmed.ncbi.nlm.nih.gov/15915798/)。
- Barbara Mellers 等（2014），[Psychological strategies for winning a geopolitical forecasting tournament](https://faculty.wharton.upenn.edu/wp-content/uploads/2015/07/2014---psychological-strategies-for-winning-a-tournament.pdf)。
- Eric Breck 等（2017），[The ML Test Score: A Rubric for ML Production Readiness and Technical Debt Reduction](https://research.google/pubs/the-ml-test-score-a-rubric-for-ml-production-readiness-and-technical-debt-reduction/)。
- Eric Breck 等（2019），[Data Validation for Machine Learning](https://research.google/pubs/data-validation-for-machine-learning/)。
- OpenAI（2025），[Evals drive the next chapter of AI](https://openai.com/index/evals-drive-next-chapter-of-ai/)。
- OpenAI（2025），[Expanding on what we missed with sycophancy](https://openai.com/index/expanding-on-sycophancy/)。

这些文献支持的是上面的局部机制和评估原则。项目后续自己的测试数据、失败案例和版本记录，才是判断这套组合是否真的有用的直接证据。
