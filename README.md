<p><picture>
  <source media="(max-width: 767px)" srcset="https://raw.githubusercontent.com/kennywu411-dev/kennywu411-dev/main/assets/header-narrow.svg">
  <img src="https://raw.githubusercontent.com/kennywu411-dev/kennywu411-dev/main/assets/header.svg" width="825" alt="Kenny Wu，大模型应用与 Agent。10 个开源项目，4 个 PR 合入上游，PyPI 已发布">
</picture></p>

你好，我是 Kenny。我做大模型应用和 Agent，重点放在可验证上：每个设计选择都有对照实验，数字能复现，模型拿不准的地方交给规则、校验或人工。

## 项目

<a href="https://github.com/kennywu411-dev/metriclens"><img src="https://raw.githubusercontent.com/kennywu411-dev/kennywu411-dev/main/assets/metriclens.svg" width="410" alt="MetricLens 经营问数：1,151/1,151。经营问数与指标异动归因。归因回答里的 1,151 个数字全部能对上执行过的 SQL；固定流程和 Agent 一样准，成本是它的 1/4–1/7；行列级权限越权 0/170。"></a>
<a href="https://github.com/kennywu411-dev/contract-review-agent"><img src="https://raw.githubusercontent.com/kennywu411-dev/kennywu411-dev/main/assets/contract-review-agent.svg" width="410" alt="采购合同审查 Agent：132–133/133。把每条风险算成钱并排出谈判优先级。模型只抄数字，金额由规则代码计算：60 份留出合同 133 个测算项算对 132–133 个，没有给出过错误金额。"></a>
<a href="https://github.com/kennywu411-dev/webhands"><img src="https://raw.githubusercontent.com/kennywu411-dev/kennywu411-dev/main/assets/webhands.svg" width="410" alt="WebHands 网页操作 Agent：15 处。浏览器 Agent，在没有 API 的网页系统里找缺陷、录单据。在 TodoMVC 11 个官方实现里找到 7 个实现的 15 处规格偏差，逐条人工复核。"></a>
<a href="https://github.com/kennywu411-dev/laborcheck"><img src="https://raw.githubusercontent.com/kennywu411-dev/kennywu411-dev/main/assets/laborcheck.svg" width="410" alt="laborcheck 劳动合同体检：98.8–100%。中国劳动合同与 Offer 的规则引擎和公开评测集（339 题）。Claude 三档只靠自身知识 82.6–87.6%，接入规则引擎工具后 98.8–100%。"></a>
<a href="https://github.com/kennywu411-dev/evalkit"><img src="https://raw.githubusercontent.com/kennywu411-dev/kennywu411-dev/main/assets/evalkit.svg" width="410" alt="evalkit 评测平台：776/777。LLM 应用评测平台，零运行时依赖。复算 MetricLens、合同审查、laborcheck 已有的运行记录，唯一不一致的 1 项是已知的文档笔误。"></a>
<a href="https://github.com/kennywu411-dev/honestly"><img src="https://raw.githubusercontent.com/kennywu411-dev/kennywu411-dev/main/assets/honestly.svg" width="410" alt="honestly：94/94。编程助手说“测试通过”时，核对这一轮是否真的跑过，没有就拦下。已发布到 PyPI，在真实的编程助手里跑了 94 个端到端场景。"></a>

在线演示：[MetricLens 问数与归因回放](https://kennywu411-dev.github.io/metriclens/) · [采购合同审查回放](https://kennywu411-dev.github.io/contract-review-agent/) · [WebHands 操作回放](https://kennywu411-dev.github.io/webhands/) · [evalkit 评测看板](https://kennywu411-dev.github.io/evalkit/) · [laborcheck 评测看板](https://kennywu411-dev.github.io/laborcheck/)

### 其他项目

- [video-pacing 短视频节奏检查](https://github.com/kennywu411-dev/video-pacing)：检查短视频节奏的 Agent skill 和脚本，检测前 5 秒是否有钩子，以及哪些片段连续 3 秒以上没有新信息。同一条视频的初版检出 10 段等待，修改后的成片为 1 段
- [sqlguard-mcp 只读 SQL 防护](https://github.com/kennywu411-dev/sqlguard-mcp)：只读的 SQLite MCP 服务器，五层防护取自 MetricLens：语法检查、只读连接、授权回调、超时、行数上限
- [ecommerce-dashboard 跨境电商看板](https://github.com/kennywu411-dev/ecommerce-dashboard)：跨境电商经营分析看板，先定义指标口径，再设计看板。同一个“销售额”，最宽与最窄口径相差 10.7%（[在线看板](https://kennywu411-dev.github.io/ecommerce-dashboard/)）
- [quant-allocation-research 跨市场配置研究](https://github.com/kennywu411-dev/quant-allocation-research)：跨市场 ETF 配置与 A 股因子研究。回测引擎与开源库 bt 交叉核对；在含退市股的全 A 股（5,481 只）上按预先登记的门槛检验 10 个因子和 3 种合成，13 个试验通过 4 个，LightGBM 合成没有样本外增益。仅为个人研究记录，不构成投资建议

## 文章

- [Claude Opus 在 BIRD 上拿了 86.6%，但可能有一半是背出来的](https://github.com/kennywu411-dev/notes/blob/main/bird-memorized-answers.md)
- [给问数系统加了 Agent，没变准，反而贵了 56%](https://github.com/kennywu411-dev/notes/blob/main/agent-vs-fixed-pipeline.md)

## 开源贡献

已合并：

- [pint #2555](https://github.com/hgrecco/pint/pull/2555)：修正零值的相等比较，0 °C 不再等于 0 °F
- [sqlfluff #8905](https://github.com/sqlfluff/sqlfluff/pull/8905)：SQLite 方言允许 MATCH、VIRTUAL、LAST 作为标识符
- [sqlfluff #8903](https://github.com/sqlfluff/sqlfluff/pull/8903)：SQLite 方言不再把裸函数和字面量解析成列引用
- [sqlglot #8784](https://github.com/tobymao/sqlglot/pull/8784)：SQLite 中 REAL 和 FLOAT 按 8 字节 DOUBLE 解析

进行中：[agentscope #3595](https://github.com/agentscope-ai/agentscope/pull/3595)、[unstructured #4665](https://github.com/Unstructured-IO/unstructured/pull/4665)、[mirascope #2973](https://github.com/Mirascope/mirascope/pull/2973)、[DB-GPT #3306](https://github.com/eosphoros-ai/DB-GPT/pull/3306)、[astroid #3465](https://github.com/pylint-dev/astroid/pull/3465)、[pylint #11788](https://github.com/pylint-dev/pylint/pull/11788)

## 常用技术

**大模型应用：** `RAG` `Agent` `多 Agent` `工具调用` `MCP` `结构化输出` `提示缓存` `Computer Use` `多模态单据识别`

**评测：** `评测集构造` `配对显著性检验` `LLM 裁判校准` `回归门禁` `trace 与成本分析`

**工程：** `Python` `FastAPI` `SSE` `Redis` `SQLite` `sqlglot` `LangGraph` `Playwright` `Next.js` `Docker` `GitHub Actions`
