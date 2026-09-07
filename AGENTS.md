# AGENTS.md

本文件只约束 AI 在本仓库的工作方式；用户当前指令优先。内容规范与协作流程不在本文件重复，见对应文档。

## 开始

- 先读 `README.md`（定位与目录）、`ASSETS_INDEX.md`（资产命名规范源）、`CONTRIBUTING.md`（协作与入库流程）。
- 检查 `git status` 与已有 diff，保留用户未提交的修改。

## 内容去向

- 主线资产进 `assets/`，按 `ASSETS_INDEX.md` 入库并登记。
- 案例实验进 `topics/<topic>/`，新 Case 从 `_case-template/` 复制、编号递增，并同步主题索引。
- 每次 AI 生成在 `GENERATION_LOG.md` 记一行；失败版本保留，不删除。

## 提交

- 按 `CONTRIBUTING.md` 使用 Conventional Commits（`assets` / `docs` / `feat` / `chore`）。
- 不提交视频、归档、密钥、缓存与无关文件；一次提交只解决一个问题。
