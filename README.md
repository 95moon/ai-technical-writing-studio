# AI Technical Writing Studio

**AI 辅助专业技术教材创作工作室**

从真实软件与技术材料出发，通过可靠的逆向研究、教学设计、专业创作和独立协作，形成读者真正能够学习、理解和迁移的技术教材。

本项目不是提示词合集、自动生成全书的流水线，也不是源码审计工具。它提供一套可组合使用的创作方法和 Agent Skill，以及适用于多个独立 AI 对话或人类作者的轻量协作机制。

> 当前版本为 v0.1.0。方法源自真实教材创作实践；首版不含公开案例。独立编辑试验与跨领域应用仍需进一步实践。

## 方法体系

| 阅读入口 | 适合何时使用 |
| --- | --- |
| [逆向研究与技术学习](skills/reverse-tech-doc-writing/references/research.md) | 面对陌生软件、真实行为或技术疑问，建立可靠认识 |
| [专业技术教材创作](skills/reverse-tech-doc-writing/references/writing.md) | 教学设计、成熟素材继承、技术深化和成篇编辑 |
| [工作流与任务模板](skills/reverse-tech-doc-writing/references/workflow.md) | 启动或接续实际任务，选择合适的工作方式 |
| [工作室协作指南](skills/reverse-tech-doc-writing/references/collaboration.md) | 独立角色交流、研究接续和决策边界 |

核心原则是以学习成果为中心、以可靠认识约束表达、让读者看见并推理真实机制、组织而非堆积知识、以实际书稿和阅读效果判断质量。

研究、学习、设计、写作、编辑可以相互促进，不必全部变成固定阶段。已有成熟材料时直接开展创作；遇到真正的认知障碍再深入研究。多版本是作品逐渐成熟的结果，而不是规定的审读轮数。

## 快速开始

### 在 Codex 中使用 Skill

将 [skills/reverse-tech-doc-writing](skills/reverse-tech-doc-writing/) 整个文件夹复制到你的教材项目的 `.agents/skills/` 下（不要只复制 SKILL.md）。三个方法论与协作指南均随 Skill 保存，支持按任务读取。保留你项目原有 AGENTS.md，在其中补充必要的项目事实、目标读者、权限和材料入口。

目录位置及技能发现机制可参考 [Codex 官方技能文档](https://developers.openai.com/codex/skills)。在任务中明确要求使用 `$reverse-tech-doc-writing`，或以自然语言描述需要开展的研究和创作。

### 在其他 AI 对话或人工协作中使用

无需安装额外程序。向当前作者提供对应方法论、具体项目材料及当前授权；如果工具能够访问共享目录，也可使用下述协作模板。仅能阅读上传文件的对话可以由用户提供必要材料，但不具备自动写入本地文件的能力。

### 建立工作室（可选）

1. 将 [collaboration/workspace](collaboration/workspace/) 复制到你自己的项目中，改名为 `studio-local` 或其他明确的本地目录。
2. 根据[角色提示词](collaboration/roles.md)建立所需角色。单人创作不必设置多个角色。
3. 将[共同项目指令](collaboration/project-instructions.md)中的路径替换为实际共享入口，使各角色能够读写同一份文件。
4. 按实际需要发布独立记录，保存正式决定、专业交流和研究接续位置。[记录模板](collaboration/record-templates.md)仅用于降低开始成本，不要求每次汇报。

各角色共享材料，不保证共享实时对话上下文，不会自动唤醒其他对话，也不会因读取某条建议而取得新的执行权限。共享区无需服务器、数据库或自动多 Agent 调度。

## 仓库结构

```text
skills/reverse-tech-doc-writing/
  SKILL.md
  references/
    research.md
    writing.md
    workflow.md
    collaboration.md
collaboration/
  roles.md
  project-instructions.md
  record-templates.md
  workspace/
    README.md
    decisions/
    discussions/
    research/
CHANGELOG.md
LICENSE
```

## 实践案例与后续方向

当前没有公开案例。后续可以补充获得公开授权、完成脱敏并保留可靠证据边界的真实研究、教学和编辑实践。不用自拟示例冒充项目实绩。

后续研究关注教学设计的回流、正文与配套知识的协同编辑、不同成熟版本的实际阅读效果，以及跨技术领域使用的条件。方法改进以真实工作为基础，不追求规则或角色数量。

## 发布范围与授权

本仓库仅含通用方法、Skill 和空白协作模板，不附源项目源码、业务数据、正式书稿、凭据、历史讨论或内部路径。仓库内发布的材料采用 [MIT License](LICENSE)，版权署名为 95moon。该许可不适用于未纳入仓库的原项目材料或第三方材料。

## English overview

AI Technical Writing Studio is a methodology and a portable agent skill for studying real software, designing technical learning material, authoring and editing textbooks, and collaborating across independent roles. It emphasizes evidence, reader-oriented reasoning, professional autonomy and reusable technical knowledge. The initial version contains Chinese-language methods and collaboration templates; public case studies are not included yet.
