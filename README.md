# Visual Asset Hub

面向 AI 视频创作的视觉资产中枢：按主题沉淀爆款案例、参考素材、Prompt、风格规范与可复用经验。

> A structured visual asset library for AI video creation — reference cases, prompts, styles, and reusable knowledge, organized by topic.

## 定位

这个仓库不是普通的素材文件夹，核心链路是：

**案例 → 拆解 → Prompt → 风格 → 经验 → Skill → Workflow**

另有一条与案例并行的主线资产库（`assets/`），存放人物、服装、脸谱、意境参考等长期复用的资产；案例实验仍在 `topics/` 下按主题沉淀。资产索引见 `ASSETS_INDEX.md`，AI 生成记录见 `GENERATION_LOG.md`。

## 目录结构

```text
visual-asset-hub/
├── README.md
├── ASSETS_INDEX.md          # 主线资产索引与当前状态
├── GENERATION_LOG.md        # AI 生成记录
├── assets/                  # 主线资产：人物/服装/脸谱/参考/待处理（图片入库，视频不入库）
│   ├── characters/
│   ├── costumes/
│   ├── facepaint/
│   ├── references/
│   └── inbox/
└── topics/
    ├── _case-template/      # 新案例模板
    └── transition/          # 当前主题：转场
```

## 核心概念

- **Topic（主题）**：按主题组织，如 `transition`。不按平台、不按文件类型拆。
- **Case（案例）**：一次生成实验 / 一条爆款案例，是最小管理单元。每个 Case 从 `_case-template/` 复制，编号如 `001-xxx`。

一个 Case 包含：`reference/`（参考）、`input/`（输入）、`prompts/`（图/视频 Prompt）、`outputs/`（生成结果，experiments + selected）、`style.md`（视觉风格拆解）、`README.md`（总结与实验记录）。

## 约定

1. **图片入库，视频不入库**：Prompt、拆解、规范、索引、README 与 `assets/` 下的图片都进 git；视频 / 归档文件不入库（见 `.gitignore`），原文件放本地或对象存储，在 README 中记录引用地址。
2. **失败不删除**：所有生成版本都记入 Case README 的实验表，这是提炼 Skill / Workflow 的数据来源。
3. **Skills / Workflows 先不建目录**：等从多个 Case 中抽出稳定规律后再建。
4. 目录与文件名用英文小写 + 数字前缀；内容描述可用中文。

## 命名规范

- 主题目录：`topics/<topic>/`，如 `transition`
- 案例目录：`topics/<topic>/<NNN>-<slug>/`，如 `001-phone-transition`
- 生成版本：`outputs/experiments/v01.mp4` 递增；采用结果放 `outputs/selected/`
- 资产目录与文件名：见 `ASSETS_INDEX.md`「命名与存放约定」（`ai/ real/ ref/` 分层 + `{对象}_{视图}[_{变体}]` 模式），规范以该文件为唯一出处
