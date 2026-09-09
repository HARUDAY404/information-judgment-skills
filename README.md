# Information Judgment Skills

一套帮助你**少刷信息、查清说法、形成自己的判断，再把成熟判断变成内容**的 AI 工作流。

今天真正稀缺的已经不是信息，也不是 AI 总结，而是四种能力：

- 从大量内容中找到真正值得看的少数信息；
- 分清事实、观点、推测和营销话术；
- 不把 AI 的答案误当成自己的思考；
- 让零散判断能够被记录、验证，并逐渐长成文章或长期知识。

这个项目把整个过程拆成四个可以单独使用、也可以组合使用的 Skill。它不是一个替你思考的“自动答案机”，而是一套让信息处理过程更容易重复、检查、复盘和改进的工作方法。

## 四个 Skill，就是四个不同的帮手

### 1. Information Radar：帮你少看

围绕你正在解决的问题定向寻找信息，合并重复内容，过滤没有新增量的噪声，最后只留下少量值得继续阅读的线索。

它回答的是：**这条信息值不值得占用我的注意力？**

### 2. Judgment Journal：帮你留下自己的想法

在 AI 给出详细分析之前，先记录你现在怎么看、为什么这样想、信心有多大，以及你最可能错在哪里。

它回答的是：**这是我原来的判断，还是看完 AI 后产生的判断？**

### 3. Claim Auditor：帮你把说法查清楚

把重要说法拆成可以检查的主张，追溯原始来源，同时寻找支持证据、反证、失败案例和其他解释。

它回答的是：**现有证据最多能支持到哪一步？**

### 4. Content Lab：帮你把判断讲出去

把经过核查的判断转成面向具体读者的文章、帖子或视频假设，发布后再根据真实反馈改善表达。

它回答的是：**怎样把一个诚实的判断，变成别人愿意看、看得懂的内容？**

流量可以帮助我们改进表达，但不能证明一个观点是真的。

## 为什么不是直接写一个超长提示词？

当然可以只用一个提示词。四个 Skill 的价值不在于“更神奇”，而在于把几种容易互相干扰的任务分开：

- Radar 负责注意力分配，不急着判断真假；
- Journal 负责保存你的观点，不替你制造观点；
- Auditor 负责检查证据，不决定你的价值选择；
- Content Lab 负责传播实验，不把点赞当成事实证明。

这样做以后，每一步都可以单独替换、测试和复盘。你可以换信息源、换 AI、换评分标准，也可以只使用其中一两个 Skill，而不必推翻整个流程。

## 三分钟开始使用

第一次不用把四个 Skill 全部跑一遍。找一条你最近很想相信、又不完全确定的信息，从下面三步开始。

### 第一步：先保存自己的判断

```text
使用 $judgment-journal，只保存我的审计前快照，暂时不要评价。
我的初始判断是……
我的理由是……
置信度是……
我最可能错在……
```

没有判断也没关系，可以直接记录“我还不知道”。

### 第二步：在独立上下文中检查证据

最好新建一个看不到上述判断的任务，再输入：

```text
使用 $claim-auditor 审计下面这条主张。
请追溯原始来源，同时寻找支持证据、反证和其他解释，
最后告诉我现有证据最多支持到什么程度。

主张或材料：……
```

### 第三步：对照前后变化

回到 Judgment Journal，打开之前保存的快照，记录：

- 哪些判断没有改变；
- 哪些判断改变了，原因是什么；
- 现在还有哪些未知；
- 什么新证据会让你再次改变看法。

这就是最小可用版本。Radar 和 Content Lab 可以等你真正需要时再加入。

## 完整工作流

```text
外部信息
   ↓
Information Radar：值得继续看吗？
   ↓
Judgment Journal（审计前）：我现在怎么看？
   ↓
Claim Auditor：证据究竟支持到哪里？
   ↓
Judgment Journal（审计后）：我为什么保持或修改判断？
   ├── 进入行动或知识库
   └── 可选：Content Lab，变成公开内容实验
```

Content Lab 不是必经步骤。如果你的目标只是减少噪声、提高判断质量，前三个 Skill 就已经足够。

## 一个 Radar 使用示例

```text
使用 $information-radar。
过去 7 天，帮我查看“AI 正在如何改变个人知识管理”。
标准模式，最多 5 条。
优先原始项目、真实实践和失败案例，排除重复转载和纯营销。
```

Radar 可以返回 0 条。没有真正重要的新信息，本身就是一个有效结果。

## 7 天试运行

第一周先不要追求全自动，也不要急着证明它能提高长期判断力。只观察它是否真的让你少看噪声、留下了更清楚的判断过程。

- Radar 每天最多保留 5 条；
- 每天最多深度审计 1 条；
- 不强迫自己对每条信息形成观点；
- 只有准备公开表达时才使用 Content Lab；
- 第 7 天复盘阅读耗时、误收噪声、遗漏的重要信息、追溯到原始来源的比例，以及真正促成判断变化或行动的次数。

## 为什么这样设计

这套流程参考了确认偏误、反向思考、判断校准、预测反馈和 AI 评估等领域的研究。研究没有为这四个 Skill 直接颁发一张“有效证书”，但为它们提供了几条重要的设计原则。

### 主动寻找相反解释，但不要为了反对而反对

Lord 等人的实验发现，主动“考虑相反情况”比泛泛提醒自己保持客观，更能减少部分判断偏差。Koslowski 等人的研究同时提醒，只执行反驳策略，也可能把中性信息误判为反证。

所以 Claim Auditor 不是机械唱反调，而是要求支持证据、反对证据和其他解释接受同样的检查。

### 保留初始判断，但不要让它干扰审计

关于锚定、确认偏误和后见之明的研究表明，人会受到已有观点影响，也容易在知道结果之后重写自己“原来怎么想”。因此 Judgment Journal 保存审计前快照，并且不覆盖历史。

不过，初始判断本身也可能成为新的锚点。更稳妥的做法是先将它封存，让 Auditor 在看不到你的立场和置信度时独立检查材料；最后再比较前后判断。如果无法隔离上下文，应注明这是“非盲审”，不要把 AI 与你意见一致当成独立验证。

### 把“我有多相信”和“证据有多强”分开

研究发现，高置信度可能使人更主动寻找支持原有选择的信息，并降低对反证的敏感度。因此 Journal 记录的是你的主观置信度，Auditor 评价的是当前证据；两者不能混成一个分数。

### 用反馈改善判断过程，而不是只凭感觉升级系统

Good Judgment Project 的研究显示，训练、协作、持续追踪和反馈可以改善概率预测表现。Google 和 OpenAI 的工程实践也强调：一个 AI 工作流能够运行，不等于它稳定有效；还需要真实案例、边界案例、固定测试集、持续评估和人工复核。

因此，这个项目保留来源、版本和历史记录，也鼓励使用同一批案例比较修改前后的表现。

## 它能做什么，不能做什么

它可以帮助你：

- 稳定地重复一套信息处理流程；
- 看见信息来源、推理过程和判断变化；
- 减少重复阅读和无目的收藏；
- 把经过核查的判断积累成内容素材；
- 用真实案例持续修改自己的工作方法。

它不能保证：

- AI 不会遗漏、误解或迎合使用者；
- 当前评分阈值具有精确的统计意义；
- 四个 Skill 一定优于每一个精心设计的单一提示词；
- 使用 7 天就能提高长期判断能力；
- 点赞、收藏和转化能够证明观点真实。

这里的严谨不是为了否定工具，而是为了避免把工具变成新的权威。

## 想认真验证，可以做一个小型对照测试

普通使用者不必先完成实验才能开始使用。如果你准备公开推广、长期维护或声称它优于其他方法，建议完成下面的最小测试。

### 1. 先定义目标

目标可以只保留两个：减少无效信息消耗；提高判断过程的可追溯性与校准度。

### 2. 建立固定案例

收集 25 个案例：可靠信息、看似权威但夸大的说法、营销内容、真实但不可泛化的个案、证据确实存在争议的问题，各 5 个。保存原文、时间和当时能够获得的证据，形成一组不随结果改变的测试材料。

### 3. 和基线比较

将同一批案例分别交给普通 AI 提问和四 Skill 工作流，比较耗时、重复信息、原始来源追溯、反证覆盖、错误接受、重要遗漏和结论边界。

条件允许时打乱输出顺序，请不知道答案来自哪组的人复核，避免只挑自己喜欢的结果。

### 4. 修改规则时保留版本

来源权重、评分、提示词或筛选阈值发生变化时，记录修改理由，再用同一批案例重跑。既记录进步，也记录退步和失败案例。

### 5. 分开事实反馈和传播反馈

新原始资料、反证和预测结果用于修改事实判断；完读、评论、收藏和转化用于改善内容表达。Content Lab 可以因为传播数据改变标题和结构，但不能据此提高一个主张的真实性等级。

## 如何安装

在 Codex 中，把需要的完整 Skill 目录复制到 `~/.codex/skills/`。每个目录中的 `SKILL.md` 和 `references/` 都需要保留。

如果其他 AI 工具不支持 Agent Skills，也可以把相应的 `SKILL.md` 当作工作流指令使用。定时监测、平台抓取、历史存储和知识库同步还需要额外工具或自动化，不是一个 Skill 文件本身就能完成的。

## 对外介绍时的一句话版本

> Information Judgment Skills 是一套受认知科学和 AI 评估方法启发的信息工作流：用 Radar 减少噪声，用 Auditor 检查证据，用 Journal 保留自己的判断，再用 Content Lab 把成熟判断变成内容。它不替你思考，而是让你的思考更容易被检查、复盘和改进。

## 参考研究与工程实践

- Charles G. Lord、Mark R. Lepper、Elizabeth Preston（1984），[Considering the opposite: a corrective strategy for social judgment](https://pubmed.ncbi.nlm.nih.gov/6527215/)。
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

这些研究支持的是工作流中的局部机制和评估原则。这个项目自己的测试数据、失败案例和版本记录，才是判断这套组合在实际使用中是否有帮助的直接证据。
