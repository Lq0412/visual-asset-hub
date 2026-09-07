# Asset Index — 主线资产

这里承载当前项目的主线资产（aron 主线）。媒体文件统一放在 `assets/`，图片进 git，视频不入库；本文件记录资产说明、状态与入库约定。

微信接收到的原包（中文命名）保留在原接收目录，仅作来源备份，不作为项目内工作副本。

## 资产与当前状态

```text
assets/
├── characters/
│   └── huibin/               人物基准：ai/ + real/ + ref/
├── costumes/
│   ├── man_a/                男装 a：ai/ + real/
│   ├── man_b/                男装 b：ai/ + real/
│   ├── man_c/                男装 c：ai/ + real/
│   └── woman_a/              女装 a（暂无头饰变体）：ai/ + real/
├── facepaint/yingge_001/     脸谱：pattern / material / applied
├── references/
│   ├── moodboard_stage_01/   17 张意境参考（mood_01 ~ mood_17）
│   └── video_links.txt       抖音参考链接
└── inbox/                    待处理资产
    ├── man_unknown/          男装实拍（归属未定）+ 网上参考
    └── woman_unknown/        女装网上参考
```

| 资产 | 当前状态 |
|---|---|
| characters/huibin | 可用；`ref/` 三张参考图**来源待确认**，确认前不用于正式出图；侧脸等多角度后续再补 |
| costumes/man_a / man_c | 可用；实拍缺 `headpiece_detail`（可选项，不强制） |
| costumes/man_b | 可用；`ai/` 含双基准：服装三视图 `threeview_headpiece` + 人物三视图 `threeview_character` |
| costumes/woman_a | 暂用「无头饰」版；头饰变体后续再定 |
| facepaint/yingge_001 | 暂不绑定服装，出图时临时指定并记入生成记录 |
| references/moodboard_stage_01 | **意境参考**：只借鉴氛围 / 风格 / 镜头感觉，不直接照抄画面 |
| references/video_links.txt | 链接索引，需要拆解时逐条补充 |
| inbox | **待处理**，保留原样，等归属确认后按下方规范改名移入对应目录 |

## 命名与存放约定（规范源）

> 资产命名规范的唯一出处，README 与案例模板引用此处；要改规范先改这里。

1. **分类与字符**：资产按 `characters / costumes / facepaint / references / inbox` 分类；目录与文件名一律小写英文 + 下划线，不带中文，人名可用拼音代号（如 huibin）。
2. **来源分层**：每个资产目录内按来源分三种子目录——`ai/`（AI 生成）、`real/`（实拍）、`ref/`（网络等外部参考）。`ref/` 内容必须在上方状态表登记来源，**未登记来源的不得用于正式出图**。
3. **文件名模式**：`{对象}_{视图}[_{变体}]`，如 `face_front_01.jpg`、`threeview_headpiece_v01.png`。同类内容全库统一用词，不造同义新词：
   - 三视图统一 `threeview_*`：服装版 `threeview_headpiece`、人物版 `threeview_character`、无头饰 `threeview_noheadpiece`
4. **版本与序号**：AI 生成文件带 `_v01` 依次递增；实拍同视图多张用两位序号 `_01`、`_02`。
5. **最小采集集**（缺项在状态表标注）：服装 `front / side / back` 必拍，`headpiece_detail` 等细节可选；人物 `face_front` 必拍，侧脸等多角度后续再补。
6. 项目内不保留 heic：收到先转 jpg 再入库。
7. 动作素材、脸部多角度采集：暂缓，需要时再补。
8. `inbox/` 不适用以上规则：保留原样；迁入正式目录时按本规范改名并登记。

## 入库登记（暂从简）

新增资产时，在 `GENERATION_LOG.md` 或本文件对应表格补三项：**名称 / 来源 / 状态（可用、待定、没处理）**。更严格的入库验收标准以后再补充，不追溯整理旧资产。
