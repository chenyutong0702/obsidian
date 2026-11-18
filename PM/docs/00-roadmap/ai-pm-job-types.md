# AI PM 岗位类型盘点:大模型 / 应用 / 平台 / 行业

> "AI 产品经理"是一个笼统的说法,实际岗位形态差异很大——在 Anthropic 做模型行为评估,和在一家电商公司做智能客服,虽然都叫 AI PM,但日常工作、能力要求、入行难度完全不同。这篇文章把 AI PM 拆成四类:**大模型厂商 PM、AI 应用 PM、AI 平台(基础设施)PM、行业(垂直)AI PM**,帮你判断自己适合哪一类、该往哪个方向准备。

文中涉及的公司、岗位、产品信息均于 2026 年 7 月通过官方招聘页 / 官方博客核实,具体来源见文末「参考资料」。

## 总览对比表

| 类型 | 核心职责 | 典型公司(2026-07) | 能力侧重 | 入行难度 |
|------|----------|---------------------|----------|----------|
| 大模型厂商 PM | 定义模型训练/评估/安全/API 的产品化优先级 | Anthropic、OpenAI、Google DeepMind;国内:DeepSeek、百度(文心)、阿里(通义)、字节(豆包)、月之暗面(Kimi) | 深度技术认知、评估方法论、与研究团队协作能力 | ★★★★★ 最高 |
| AI 应用 PM | 把模型能力包装成用户可用的产品/功能 | Perplexity、Cursor;国内:抖音、美团、小米、理想汽车、蚂蚁等公司内嵌 AI 功能的团队 | 用户体验设计、Prompt 工程基础、成本与效果的权衡意识 | ★★★ 中等,转型友好度最高 |
| AI 平台(基础设施)PM | 为开发者/企业提供构建 AI 应用的底层能力 | Databricks、Snowflake、AWS(Bedrock);国内:云厂商的大模型服务平台 | 最强的技术深度 + 企业级(B端)产品经验 | ★★★★★ 最高,且要求复合背景 |
| 行业(垂直)AI PM | 把 AI 能力和具体行业知识、合规要求深度结合 | Harvey(法律)、Abridge / Hippocratic AI(医疗)、Sierra(客服);国内:科大讯飞(教育/医疗/司法/汽车)、畅捷通(中小企业 Agent)、海信(智能家电) | 行业知识 > 泛化 AI 认知,合规与领域安全设计能力 | ★★★★ 较高,但行业背景可替代部分 AI 门槛 |

下面逐类展开。

## 一、大模型厂商 PM

**做什么**:这是离模型本身最近的 AI PM,工作内容包括定义预训练/后训练(RLHF、post-training)的产品优先级、设计模型评估体系、把研究团队的能力转化为可发布的产品特性、平衡模型的安全边界与体验、维护开发者 API 生态。

**真实岗位形态**(2026-07 各公司官网仍在招聘的岗位,可以看出这一类内部还会再细分):

- Anthropic:官网列出的 PM 岗位包括 "Product Manager, Compute Platform"(算力平台)、"Product Manager, Safeguards"(安全防护,专门处理稀有但严重的滥用风险)、"Research Product Manager, Model Behaviors"(模型行为研究)、"Web Product Manager"(Claude.ai 网页产品)。这说明即便同属"模型厂商 PM",内部也分化出偏研究、偏安全、偏基础设施、偏消费产品等不同方向。
- OpenAI:官网岗位包括 "Product Manager, Enterprise"、"Product Manager, Integrity"(诚信与滥用防护)、"Product Manager, Countries & Governments"(政企合规场景)等,普遍要求计算机科学/工程/数学等技术背景。
- Google DeepMind:Gemini 相关 PM 岗位包括 "Product Manager, Gemini API Models"(面向开发者的模型发布)、"Senior Product Manager, Gemini Post Training"(把用户需求转化为训练优先级和评估标准)、"Product Manager, Gemini App"(消费者应用产品定义)。
- 国内:DeepSeek 在 2026 年 6 月完成首轮外部融资后启动大规模扩招,产品部门开放"AI 产品经理""AI 产品运营""Agent 智能体产品经理"等岗位,同时在"模型数据策略"方向开放"通用 Agent 数据产品经理""专业领域数据产品经理(小语种、医学、法律等)"等细分岗位——这也说明大模型厂商 PM 正在向"数据策略产品经理"这种更细分的形态延伸。百度(文心)、阿里(通义)、字节跳动(豆包)、月之暗面(Kimi)等公司也均有对应的大模型产品团队。

**能力侧重**:五个能力维度里,「技术认知」和「数据与评估能力」的要求最高,通常需要能直接参与训练数据、评估指标层面的讨论,而不仅仅是需求翻译。

**入行难度**:最高。核心研究相关岗位通常要求较深的技术背景或多年经验(如 OpenAI 岗位普遍要求 10 年以上产品或相关行业经验),校招/应届生更容易进入的是消费产品向或数据策略向的细分岗位。

## 二、AI 应用 PM

**做什么**:在模型能力之上构建终端用户可用的产品——可能是完全 AI 原生的产品(如 AI 搜索、AI 编程助手),也可能是把 AI 能力嵌入到已有产品里(如电商导购、智能客服、车机语音助手)。这是目前岗位数量增长最快、也是传统 PM 转型最容易切入的一类。

**真实岗位形态**:

- Perplexity 设有专门的 Associate Product Manager(APM)项目,面向应届或转型不久的候选人,强调"和工程、设计、数据科学团队协作打造 AI 工具",不要求算法研究背景。
- 国内大厂普遍把 AI 能力作为存量产品的增量功能来招募 PM:字节跳动 2026 校招 AI 相关岗位中包含"电商 AI 产品经理";本仓库收录的多篇 [面经](PM/docs/04-interview/experiences/README.md) 也印证了这一类岗位的真实形态,例如抖音 AI PM、美团 AI 客服 PM 实习、小米 AI PM、理想汽车 AI PM、蚂蚁 AI 客服 PM、B 站多模态 AI PM 等,均属于"在已有业务里做 AI 功能"的应用型岗位。

**能力侧重**:用户体验设计和产品基本功是主战场,技术认知只需要达到「及格线」——理解模型能力边界、会做基础 Prompt 调优、知道效果和成本的权衡即可,不需要参与模型训练层面的决策。

**入行难度**:四类里对传统 PM 最友好的一类。这类岗位数量最多、招聘口径也更贴近传统产品经理的能力模型,是大多数转型者的第一站,具体行动计划可参考 [传统 PM 转型 AI PM 指南](transition-guide.md)。

## 三、AI 平台(基础设施)PM

**做什么**:服务对象不是终端消费者,而是"想用 AI 能力构建产品的开发者和企业"——包括模型托管服务、微调/训练平台、Agent 开发框架、向量数据库、评估工具链等。这类 PM 本质是 B 端/开发者产品经理,只是产品对象换成了 AI 能力。

**真实岗位形态**:Databricks 官网的 "Staff Product Manager, AI Platform" 岗位描述里,职责包括"定义客户如何在 Databricks 上构建、训练、部署和监控 AI/ML 系统""与工程团队共同做深度技术决策""定义 AI 平台功能的定价、打包和商业化策略",要求 5 年以上平台/基础设施类产品经验,理想情况下有 ML/AI、数据或云服务背景。Snowflake、AWS(Bedrock)等云厂商也有对应的大模型托管与 AI 平台产品线,处于同一竞争格局中。

**能力侧重**:四类里对「技术认知」和「商业判断」要求最高的组合——既要懂技术深度(训练/推理/评估的工程细节),又要有成熟的企业级产品定价和打包经验。

**入行难度**:最高,且要求复合背景。这类岗位很少作为"AI 转型第一站",更常见的路径是"先有多年 B 端/基础设施产品经验,再叠加 AI 认知",或者反过来"先在模型厂商/云厂商做过 AI 产品,再转向平台方向"。

## 四、行业(垂直)AI PM

**做什么**:把 AI 能力和某个具体行业的知识、工作流、合规要求深度绑定,做出"通用大模型做不到"的垂直体验。这类岗位的核心壁垒往往不是模型能力本身,而是行业数据、行业安全架构和行业渠道。

**真实岗位形态**:

- 法律行业:Harvey 是这一类最典型的代表,官方数据显示其在 2026 年 3 月完成 11 亿美元估值融资,年化收入(ARR)约 1.9 亿美元,已覆盖多数 AmLaw 100 律所。
- 医疗行业:Abridge(临床对话记录与病历生成)、Hippocratic AI(患者侧护理与陪伴 Agent)是医疗垂直 AI 的代表,两者都强调针对医疗场景的专属安全架构,而不是直接套用通用大模型。
- 客服行业:Sierra 专注企业级客服 Agent,是垂直 Agent 类产品的代表之一。
- 国内:科大讯飞明确把教育、医疗、司法、汽车列为其大模型的四大行业主战场——例如面向教育场景的"步骤级批改、错因定位"能力,面向医疗场景的"AI 慢病管理、AI 病历生成"等;畅捷通面向中小微企业推出了"畅龙虾"AI Agent 平台,定位 7×24 小时自主工作的"AI 员工";海信等家电企业也在招募 AI PM,聚焦智能家电场景下的 AI 能力嵌入。

**能力侧重**:行业知识的重要性通常高于泛化的 AI 前沿认知——懂法律工作流、懂医疗合规、懂教育场景的人,往往比"只懂大模型但不懂行业"的人更有竞争力。合规与领域安全设计能力(如医疗数据隐私、教育场景未成年人保护)也是核心要求。

**入行难度**:较高,但路径更多元。如果你有对应行业的从业背景(比如做过法律、医疗、教育行业的产品或业务),AI 认知反而可以作为"加分项"补齐,而不必先具备大模型厂商级别的技术深度。

## 怎么选适合自己的方向

1. 先用 [AI 产品经理能力模型](ai-pm-capability-model.md) 给自己五个维度打分——技术认知和评估能力弱、但产品基本功扎实,大概率更适合 AI 应用 PM;如果你本身有深厚的行业背景(法律、医疗、教育、制造等),行业垂直 AI PM 是更顺的路径。
2. 没有相关经验的转型者,建议从 AI 应用 PM 切入,门槛最低、和传统 PM 经验的重合度最高,参考 [传统 PM 转型 AI PM 指南](transition-guide.md) 的 3 个月计划。
3. 大模型厂商 PM 和 AI 平台 PM 通常需要更长的积累周期(技术深度、B 端经验),更适合作为"第二步"目标,而不是转型第一站。
4. 不要只看公司名气,要看具体岗位描述里写的职责——同一家公司内部,"消费产品 PM"和"模型行为研究 PM"可能是完全不同的能力要求。

## 相关阅读

- [AI 产品经理能力模型](ai-pm-capability-model.md)
- [传统 PM 转型 AI PM 指南](transition-guide.md)
- [AI 产品经理入门路径](getting-started.md)
- [模型与产品效果评估](PM/docs/02-pm-skills/model-evaluation/README.md)
- [成本测算与技术协作](PM/docs/02-pm-skills/cost-and-tech/README.md)
- 面经案例:[字节跳动 KOL Agent PM](bytedance-kol-agent-pm-202607.md)、[美团 AI PM 实习](meituan-ai-pm-intern-202607.md)、[科大讯飞 产品经理](iflytek-pm-202511.md)、[畅捷通 AI 产品经理](changjietong-ai-pm-202607.md)、[海信集团 AI 产品](hisense-ai-pm-202607.md)

## 参考资料

- [Jobs \ Anthropic](https://www.anthropic.com/careers/jobs) — Anthropic 官方招聘页,列出 Compute Platform、Safeguards、Research Product Manager 等岗位,2026-07 访问
- [Product Manager, Enterprise | OpenAI](https://openai.com/careers/product-manager-enterprise/) — OpenAI 官方招聘详情页,2026-07 访问
- [Careers at Google DeepMind](https://deepmind.google/careers/) — Google DeepMind 官方招聘页,2026-07 访问
- [Product Manager, Gemini API Models, DeepMind — Google Careers](https://www.google.com/about/careers/applications/jobs/results/130228712753767110-product-manager-gemini-api-models-deepmind) — Google 官方招聘详情页,2026-07 访问
- [Staff Product Manager, AI Platform - Databricks](https://www.databricks.com/company/careers/product/staff-product-manager-ai-platform-8427940002) — Databricks 官方招聘详情页,2026-07 访问
- [Perplexity Associate Product Manager Program](https://www.perplexity.ai/hub/associate-product-manager) — Perplexity 官方 APM 项目介绍页,2026-07 访问
- [Harvey Raises at $11 Billion Valuation to Scale Agents Across Law Firms and Enterprises](https://www.harvey.ai/blog/harvey-raises-at-dollar11-billion-valuation-to-scale-agents-across-law-firms-and-enterprises) — Harvey 官方博客,2026-07 访问
- [DeepSeek计划所有部门的规模扩大1倍 融资后大举招聘](https://companies.caixin.com/2026-06-26/102458093.html) — 财新网报道,2026-07 访问
