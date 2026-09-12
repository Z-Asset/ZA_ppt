---
name: za-ppt
description: 报告阶段（PPT）—— 从论文生成演讲幻灯片（Beamer 或 Quarto RevealJS）。当用户要「做 PPT」「做 Beamer 演讲」「做 slides」「准备 presentation」「job market talk」「seminar talk」时使用。
whenToUse: 演讲制作、Beamer/Quarto 幻灯片、narrative arc 设计、视觉审计。
---

# 报告阶段（PPT）

派发 Storyteller（`references/agents/storyteller.md`）与 storyteller-critic（`references/agents/storyteller-critic.md`），读取并**完整采纳其角色设定**。

## 格式约束

| 格式 | 页数 | 时长 | 内容范围 |
|------|------|------|---------|
| job-market | 40-50 | 45-60 min | 完整故事、所有结果、机制、稳健性 |
| seminar | 25-35 | 30-45 min | 动机、主结果、2 个稳健性、结论 |
| short | 10-15 | 15 min | 问题、方法、关键结果、意义 |
| lightning | 3-5 | 5 min | Hook、一个结果、so-what |

## 工作流

1. 读论文，提取：研究问题、识别/估计策略、主结果、次要结果、稳健性、关键图表
2. 派发 Storyteller 设计 narrative arc：
   - 一页一 idea；图优先、表放 backup（备 Q&A）
   - 张力递进：动机 → 问题 → 方法 → 发现 → 意义
   - 大章节之间放 transition 页
   - **paper 是唯一事实来源**——不新增 paper 没有的结果
3. 编译：Beamer 用 XeLaTeX（`latexmk`），Quarto 用 `quarto render`
4. 派发 storyteller-critic 审 5 类：narrative flow / 视觉质量 / content fidelity / 篇幅 / 编译
5. Critical 问题重派 Storyteller（最多 3 轮）
6. 呈现：文件路径、页数、critic 评分（advisory）、TODO

## 原则
- 图优先于表；audience 吸收图是瞬间的
- 一页一 idea；少即是多（尤其 short/lightning）
- 评分 advisory（不阻断 commit）
- Storyteller 创作、storyteller-critic 批判，永不跳过
