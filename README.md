<p><picture>
  <source media="(max-width: 767px)" srcset="https://raw.githubusercontent.com/kennywu411-dev/kennywu411-dev/main/assets/header-narrow.svg">
  <img src="https://raw.githubusercontent.com/kennywu411-dev/kennywu411-dev/main/assets/header.svg" width="825" alt="Kenny Wu，大模型应用与 Agent。10 个开源项目，4 个 PR 合入上游，PyPI 已发布">
</picture></p>

你好，我是 Kenny。我做大模型应用和 Agent，重点放在可验证上：每个设计选择都有对照实验，数字能复现，模型拿不准的地方交给规则、校验或人工。

## 项目

<a href="https://github.com/kennywu411-dev/datapilot"><img src="https://raw.githubusercontent.com/kennywu411-dev/kennywu411-dev/main/assets/datapilot.svg" width="410" alt="DataPilot：63.0% → 68.0%。中文问数（NL2SQL），出错自动修正。取值核对加执行纠错提升 Haiku 准确率；固定流程和 Agent 一样准，Agent 贵 56%；行列级权限越权 0/170。"></a>
<a href="https://github.com/kennywu411-dev/contract-review-agent"><img src="https://raw.githubusercontent.com/kennywu411-dev/kennywu411-dev/main/assets/contract-review-agent.svg" width="410" alt="合同风险审查 Agent：75/75。60 份长合同的难评测集检出 75/75，代价是误报回升；较简单的评测集上，多 Agent 把干净合同的误报意见从 13–14 条降到 4–6 条。每条意见附法条或公司规范原文。"></a>
<a href="https://github.com/kennywu411-dev/uipilot"><img src="https://raw.githubusercontent.com/kennywu411-dev/kennywu411-dev/main/assets/uipilot.svg" width="410" alt="UIPilot：15 处。浏览器 Agent，在没有 API 的网页系统里找缺陷、录单据。在 TodoMVC 11 个官方实现里找到 7 个实现的 15 处规格偏差，逐条人工复核。"></a>
<a href="https://github.com/kennywu411-dev/laborcheck"><img src="https://raw.githubusercontent.com/kennywu411-dev/kennywu411-dev/main/assets/laborcheck.svg" width="410" alt="laborcheck：98.8–100%。中国劳动合同与 Offer 的规则引擎和公开评测集（339 题）。Claude 三档只靠自身知识 82.6–87.6%，接入规则引擎工具后 98.8–100%。"></a>
<a href="https://github.com/kennywu411-dev/evalkit"><img src="https://raw.githubusercontent.com/kennywu411-dev/kennywu411-dev/main/assets/evalkit.svg" width="410" alt="evalkit：776/777。LLM 应用评测平台，零运行时依赖。复算 DataPilot、合同审查、laborcheck 已有的运行记录，唯一不一致的 1 项是已知的文档笔误。"></a>
<a href="https://github.com/kennywu411-dev/honestly"><img src="https://raw.githubusercontent.com/kennywu411-dev/kennywu411-dev/main/assets/honestly.svg" width="410" alt="honestly：94/94。编程助手说“测试通过”时，核对这一轮是否真的跑过，没有就拦下。已发布到 PyPI，在真实的编程助手里跑了 94 个端到端场景。"></a>

可以直接打开看：[UIPilot 操作回放](https://kennywu411-dev.github.io/uipilot/) · [evalkit 评测看板](https://kennywu411-dev.github.io/evalkit/) · [laborcheck 评测看板](https://kennywu411-dev.github.io/laborcheck/)

### 小一些的

- [video-pacing](https://github.com/kennywu411-dev/video-pacing)：检查短视频节奏的 Agent skill 和脚本，看前 5 秒有没有钩子、哪里连续 3 秒以上没有新东西。我自己一条嫌慢的初版被标出 10 段等待，改完后的成片剩 1 段
- [sqlguard-mcp](https://github.com/kennywu411-dev/sqlguard-mcp)：只读的 SQLite MCP 服务器，从 DataPilot 里拆出来的五层防护：语法检查、只读连接、授权回调、超时、行数上限
- [ecommerce-dashboard](https://github.com/kennywu411-dev/ecommerce-dashboard)：跨境电商经营分析看板，先定指标口径再做图。同一个“销售额”，最宽和最窄的口径相差 10.7%（[在线看板](https://kennywu411-dev.github.io/ecommerce-dashboard/)）
- [quant-allocation-research](https://github.com/kennywu411-dev/quant-allocation-research)：跨市场 ETF 配置的个人研究。回测引擎和开源库 bt 交叉核对，5 个因子 ETF 候选按事先写好的门槛全部否决。不是投资建议

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
