### 你好，我是 Kenny

我做大模型应用和 Agent，关注的不是"能跑起来"，而是"能证明它靠谱"：每个设计选择都有对照实验，每个数字都能复现，模型拿不准的地方交给规则、校验或人工。

## 项目

| 项目 | 做什么 | 关键结果 |
|---|---|---|
| [**DataPilot**](https://github.com/kennywu411-dev/datapilot) | 中文问数（NL2SQL）：读表结构、写 SQL、只读执行、出错自动修正，返回答案、表格和图表 | 取值核对加执行纠错把 Haiku 准确率从 63.0% 提到 68.0%（p=0.008）；实验证明固定流程和 Agent 准确率相同，Agent 贵 56%；行列级权限越权 0/170；智能路由用 14% 的成本达到 69.6% |
| [**Contract Risk Review Agent**](https://github.com/kennywu411-dev/contract-review-agent) | 合同风险审查：站在我方立场逐条找不利条款，每条意见附法条或公司规范原文，核实不了的转法务 | 难评测集 60 份长合同检出 75/75；多 Agent 把干净合同上的误报意见从 13–14 条降到 4–6 条；无依据意见占比 0.8%；附 PRD、竞品分析和用户试用方案 |
| [**honestly**](https://github.com/kennywu411-dev/honestly) | 给编程助手用的验证工具：它说"测试通过""已部署"时，核对这一轮里是否真的执行过，没有就拦下 | 已发布到 PyPI；纯规则、无依赖、不联网；支持 Claude Code、Codex、Cursor、Gemini CLI |

## 开源贡献

已合并：

- [sqlfluff #8905](https://github.com/sqlfluff/sqlfluff/pull/8905)：SQLite 方言允许 MATCH、VIRTUAL、LAST 作为标识符
- [sqlfluff #8903](https://github.com/sqlfluff/sqlfluff/pull/8903)：SQLite 方言不再把裸函数和字面量解析成列引用
- [sqlglot #8784](https://github.com/tobymao/sqlglot/pull/8784)：SQLite 中 REAL 和 FLOAT 按 8 字节 DOUBLE 解析

进行中：[agentscope #3595](https://github.com/agentscope-ai/agentscope/pull/3595)、[unstructured #4665](https://github.com/Unstructured-IO/unstructured/pull/4665)、[mirascope #2973](https://github.com/Mirascope/mirascope/pull/2973)、[DB-GPT #3306](https://github.com/eosphoros-ai/DB-GPT/pull/3306)

## 常用技术

- 大模型应用：RAG（BM25 + 向量 + 重排）、Agent 与多 Agent、工具调用、MCP、结构化输出、提示缓存
- 评测：评测集构造、配对显著性检验、LLM 裁判校准、回归门禁、trace 与成本分析
- 工程：Python、FastAPI、SSE、Redis、SQLite、sqlglot、LangGraph、Next.js、Docker、GitHub Actions
