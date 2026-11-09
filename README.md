<img src="assets/header.svg" width="100%" alt="Kenny Wu，大模型应用与 Agent。6 个开源项目，3 个 PR 合入上游，PyPI 已发布">

你好，我是 Kenny。我做大模型应用和 Agent，重点放在可验证上：每个设计选择都有对照实验，数字能复现，模型拿不准的地方交给规则、校验或人工。

## 项目

<a href="https://github.com/kennywu411-dev/datapilot"><img src="assets/datapilot.svg" width="100%" alt="DataPilot：63.0% → 68.0%。中文问数（NL2SQL），出错自动修正。取值核对加执行纠错提升了 Haiku 准确率；固定流程和 Agent 准确率相同，Agent 贵 56%；行列级权限越权 0/170。"></a>

<a href="https://github.com/kennywu411-dev/contract-review-agent"><img src="assets/contract-review-agent.svg" width="100%" alt="合同风险审查 Agent：75/75。60 份长合同的难评测集检出 75/75。多 Agent 把干净合同上的误报意见从 13–14 条降到 4–6 条，每条意见附法条或公司规范原文，核实不了的转法务。"></a>

<a href="https://github.com/kennywu411-dev/uipilot"><img src="assets/uipilot.svg" width="100%" alt="UIPilot：15 处。浏览器 Agent，在没有 API 的网页系统里找缺陷、录单据。在 TodoMVC 11 个官方实现里找到 7 个实现的 15 处规格偏差，逐条人工复核。"></a>

<a href="https://github.com/kennywu411-dev/laborcheck"><img src="assets/laborcheck.svg" width="100%" alt="laborcheck：98.8–100%。中国劳动合同与 Offer 的规则引擎和公开评测集（339 题）。Claude 三档只靠自身知识 82.6–87.6%，接入规则引擎工具后 98.8–100%。"></a>

<a href="https://github.com/kennywu411-dev/evalkit"><img src="assets/evalkit.svg" width="100%" alt="evalkit：776/777。LLM 应用评测平台，零运行时依赖。复算 DataPilot、合同审查、laborcheck 已有的运行记录，唯一不一致的 1 项是已知的文档笔误。"></a>

<a href="https://github.com/kennywu411-dev/honestly"><img src="assets/honestly.svg" width="100%" alt="honestly：94/94。编程助手说“测试通过”时，核对这一轮是否真的跑过，没有就拦下。已发布到 PyPI，在真实的 Claude Code、Codex、Gemini CLI 里跑了 94 个端到端场景。"></a>

## 开源贡献

已合并：

- [sqlfluff #8905](https://github.com/sqlfluff/sqlfluff/pull/8905)：SQLite 方言允许 MATCH、VIRTUAL、LAST 作为标识符
- [sqlfluff #8903](https://github.com/sqlfluff/sqlfluff/pull/8903)：SQLite 方言不再把裸函数和字面量解析成列引用
- [sqlglot #8784](https://github.com/tobymao/sqlglot/pull/8784)：SQLite 中 REAL 和 FLOAT 按 8 字节 DOUBLE 解析

进行中：[agentscope #3595](https://github.com/agentscope-ai/agentscope/pull/3595)、[unstructured #4665](https://github.com/Unstructured-IO/unstructured/pull/4665)、[mirascope #2973](https://github.com/Mirascope/mirascope/pull/2973)、[DB-GPT #3306](https://github.com/eosphoros-ai/DB-GPT/pull/3306)

## 常用技术

**大模型应用：** `RAG` `Agent` `多 Agent` `工具调用` `MCP` `结构化输出` `提示缓存` `Computer Use` `多模态单据识别`

**评测：** `评测集构造` `配对显著性检验` `LLM 裁判校准` `回归门禁` `trace 与成本分析`

**工程：** `Python` `FastAPI` `SSE` `Redis` `SQLite` `sqlglot` `LangGraph` `Playwright` `Next.js` `Docker` `GitHub Actions`
