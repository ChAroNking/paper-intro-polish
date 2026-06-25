# paper-intro-polish

将学术论文的中文摘要和引言润色至 Nature / Science / 顶刊水平。基于对 **902 篇**顶刊论文（326 篇 Nature + 52 篇 Science + arXiv/bioRxiv/JSV 等）的全文系统分析，提炼出结构、叙事、过渡和语言的全套写作规范。

## 功能

- 摘要润色：重构结构、强化缺口陈述、优化 "Here we" 枢纽句位置、精炼语言
- 引言润色：梳理漏斗型叙事弧线、优化段落逻辑、强化贡献陈述、调整路线图使用
- 诊断 + 重构 + 精炼 + 输出 四步工作流，输出 `.md` 文件含修改说明

## 安装

### Claude Code 插件安装

```bash
claude plugins install github.com/ChAroNking/paper-intro-polish
```

### 手动安装

将本目录复制到你的项目 `.claude/skills/paper-intro-polish/` 下即可生效。

## 触发词

中文：润色摘要、改写引言、论文润色、顶刊风格、提升论文写作、摘要修改、引言修改、学术写作优化

English: polish abstract, refine introduction, academic writing, Nature/Science style

## 数据基础

所有建议均基于 18 个 agent 对 902 篇论文的交叉验证分析：

| 维度 | 关键发现 |
|------|----------|
| 摘要 A 型（背景→缺口→Here we→结果→意义） | 整体 ~45%，Nature 批次 ~55-88% |
| "Here we" 使用率 | Nature ~85%，Science ~50%（IRRC 格式避开） |
| 显性缺口标记率 | 整体 ~56%，Nature ~56-87% |
| 引言段落数 | Nature 标准：摘要 + 3 段正文（77-87%） |
| 漏斗型叙事 | ~55-60% |
| 路线图使用 | Nature 几乎为 0%，工程类常见 |

## 使用示例

```
用户：帮我润色这篇摘要
[粘贴摘要文本]

Skill 输出：
1. 诊断：结构偏离 A 型模板，缺口句在第 5 句，枢纽句缺失
2. 重构：缺口句前移至第 2 句，"本文提出…"作为第 3 句枢纽
3. 精炼：删除 "显著提升" → 补充具体数字，统一术语
4. 输出润色后摘要 + 修改要点
```

## 文件结构

```
paper-intro-polish/
├── SKILL.md    # Skill 定义与完整写作指南（326 行）
└── README.md   # 本文件
```

## 许可

MIT
