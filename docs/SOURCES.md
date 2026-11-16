# 来源仓库登记 · Source Repositories

本文件记录本仓库的**来源与上下文**，以及「哪些内容取自哪里、哪些明确没有取」。

> 结论先行：本仓库是独立展示项目。唯一取自来源仓库的内容是 `index.html`——`outshore` 仓库中 `outshore.html` 的逐字副本（SHA-256 一致）；其余仓库仅作为同方向项目集登记在案，未复制代码、数据或文档正文。

## 登记表

| 仓库 | 默认分支 | 角色 | 技术栈 | 与本仓库的关系 | 可见性 |
| --- | --- | --- | --- | --- | --- |
| `wanqushangpai-odoo` | `main` | 香港公司 Odoo 18 记账中台：SME-FRS 科目表、多币种流水采集、离岸豁免辅助核算、CPA 底稿导出 | Odoo 18 · Python · PostgreSQL 16 · Docker | 账务与审计底稿来源；页面中的服务边界与自检口径对应其产出 | private |
| `wanqushangpai-odoo-infra` | `master` | 上述中台的一键部署、备份与运维 | Docker Compose · Nginx · Certbot | 部署层；与本仓库无运行时依赖 | private |
| `group-sop` | `master` | 竞标 / 经纪 / PDF 解析引擎：需求解析、群内竞标、定标签约 | React 19 · TypeScript · Vite · Cloudflare Workers · D1 · R2 | 同一业务方向的工程样例（前端 + 边缘后端） | private |
| `crypto-reconciliation-cleaner` | `main` | 单文件离线加密交易对账清洗器：本地 CSV/JSON 清洗、判重、成本基础缺口扫描 | 单文件 HTML/JS（零依赖、零构建） | 同一设计取向：纯本地处理、数据不出浏览器 | private |
| `outshore` | `main` | OUTSHORE 离岸证据链技术劳务落地页（Upwork 端） | 单文件 HTML/JS | **本仓库页面的直接来源**：`index.html` 即其 `outshore.html` 的逐字副本 | private |

## 脱敏边界

| 类别 | 是否进入本仓库 | 说明 |
| --- | --- | --- |
| `outshore` 的页面源文件（`outshore.html`） | ✅ | 逐字复制为 `index.html`，未改动文字、价格、样式、脚本与合规声明 |
| 其余四个仓库的源代码 | ❌ | 仅登记仓库名与一句话用途 |
| 上述仓库的 README / 文档正文 | ❌ | 不在本仓库中转载 |
| 客户名称、真实个案、真实申报数据 | ❌ | 页面只有通用服务描述，不含任何客户或个案数据 |
| 密钥、令牌、`.env`、私钥、站外联系方式 | ❌ | 提交前经高置信 secret 扫描，零命中 |
| 仓库名与大致用途 | ✅ | 仅用于说明项目脉络；均为私有仓库，不含可访问内容 |

## 为什么没有把代码直接搬进来

1. **形态不同。** 五个仓库分别是 Odoo 18 应用、Docker 部署、React + Workers 应用和两个单文件页面；拼进同一个仓库只会得到一个无法整体运行的大杂烩。
2. **私有内容不适合公开。** 其中包含客户记账配置、内部流程与竞标规则；公开传播既无必要也有风险。
3. **可审阅性。** 一个能在浏览器直接打开、零依赖的完整页面，比一堆无法运行的片段更能说明工程判断力。

## 同步规则

- `index.html` 必须与 `outshore` 仓库的 `outshore.html` 保持字节一致（仅允许换行差异）。
- 页面源文件更新后，走「复制 → 校验 SHA-256 → 重新录制 GIF / 截图 → secret 扫描 → 提交」的流程。
- **不在本仓库直接编辑 `index.html`**：价格、服务边界与合规声明一律以源文件为准。

## 访问

上述仓库均为私有。如需演示、架构讲解或源码 walkthrough，请通过 <https://github.com/zhetai> 所列联系方式沟通。
