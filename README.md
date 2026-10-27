# Apex Controller Coach · Apex 手柄陪练

[English](#english) | [简体中文](#chinese)

<a id="english"></a>

## English

### Overview

A local Codex skill for Apex Legends controller practice: plan a session, respond to feedback, record what actually happened, and carry the next starting point into a later chat.

**Use your own controller settings, goals, and training records. Works in a regular Codex chat.**

Display name: **Apex 手柄陪练**  
Skill ID: `apex-controller-coach`

The skill instructions and default responses are primarily in Chinese. You can request another response language.

### What it does

| Stage | What happens |
| --- | --- |
| 1. Read the handoff | Find the latest actual progress and the next starting point in your project. |
| 2. Check in and plan | Ask a few relevant questions, then adapt the session to your answers and agreed budget. |
| 3. Practice and feedback | Help with the problems you report without turning an old issue into a permanent daily question. |
| 4. Record and hand off | Save actual practice, optional account statistics, unfinished work, and where to resume. |
| 5. Review | Review comparable progress and adjust the longer-term framework when requested. |

- **Keep the workload manageable:** Suggest about 30 minutes for focused practice plus logging unless you agree on another budget. The default order is Aim Lab, when used, then the firing range, a break if needed, matches, and logging. Match time is recorded afterward rather than assigned as a daily requirement.
- **Continue accurately:** A training-day number reflects recorded sessions, not elapsed calendar days or the number of chats. Continuing on the same day does not advance it again. Planned work is never recorded as completed work.
- **Use your current settings:** Read confirmed settings only when relevant. Suggestions remain separate from configurations you have actually adopted.
- **Read screenshots:** Extract relevant account or personal match statistics directly from images. Calculate daily increases only from comparable, non-reset cumulative records; missing data stays unknown.
- **Recommend videos when wanted:** Keep highlights and short tips separate, verify original pages, and avoid repeating a video. Video recommendations can be skipped.
- **Review real progress:** Consider completed practice, physical condition, gameplay feedback, and comparable statistics. No promised rank or deadline.

### Requirements

This is an instruction-based skill. It contains no executable programs, installation scripts, game integration, or automatic telemetry collection.

| Feature | Required capability |
| --- | --- |
| Load and use the skill | A Codex environment that supports local skills |
| Continue between chats | Read access to your Apex project and latest records |
| Save plans and records | Write access to that project |
| Read account or match screenshots | Image-reading capability |
| Verify videos or current game/device details | Web access; unavailable verification is disclosed |
| Rename a daily training chat | An available Codex chat-management tool |

Aim Lab is optional. Without it, the coach can use firing-range practice. Without chat-management tools, name the chat manually. Without file-writing access, the coach provides a reusable handoff in the chat and says it has not been saved.

### Installation

#### Option 1: Ask Codex to install it

1. Download or clone this repository. If you download a ZIP, extract it and name the skill folder `apex-controller-coach`.
2. Reference that folder in a local Codex chat, or provide its actual path.
3. Send:

   > Install this apex-controller-coach folder in a user skill directory that this Codex environment can discover. Preserve the complete directory structure. If a skill with the same name already exists, tell me first. Install it only; do not start training or change my training records. After installation, check whether I can invoke $apex-controller-coach.

4. Grant access to the installation directory if your environment requests it.

#### Option 2: Install manually

Copy the complete folder into the user skill directory:

```text
~/.agents/skills/apex-controller-coach/SKILL.md
```

On Windows:

```text
%USERPROFILE%\.agents\skills\apex-controller-coach\SKILL.md
```

Keep `SKILL.md`, `agents/`, and `references/` together. Avoid an extra nested folder with the same name or duplicate installations. Codex detects skill changes automatically; restart it if the skill does not appear. See the [official skill discovery documentation](https://learn.chatgpt.com/docs/build-skills).

### Invocation and scope

Include `$apex-controller-coach` and the task you want to perform. Codex may also select this skill when your request matches its description; automatic selection remains enabled.

Starting training, continuing a session, logging results, reviewing a week, and consulting settings are separate tasks. Uploading a screenshot does not automatically start a new training day. Discussing, editing, or installing the skill does not start training or change training progress.

The coach does not create chats or scheduled reminders. Archiving old chats requires your authorization.

### First use

#### If you already have an Apex project

Open a chat in that project, or tell the coach where the project is. For example:

> Use $apex-controller-coach with my existing Apex project. Read its rules and latest handoff, then start today's training. Ask about relevant unknowns before giving the full plan. Keep the current file names and controller settings.

The skill uses your project's applicable `AGENTS.md` and existing files, keeping their current names and layout.

#### If you have no records yet

Choose a separate folder for your Apex training project and send:

> Use $apex-controller-coach to set up an Apex controller training project in the folder I specify. Ask about my platform, controller experience, goals, and available practice time. Suggest a starting plan and save the agreed plan and necessary records there. Do not record any training as completed yet.

Provide any settings you already use. You do not need to fill in every device parameter or have account screenshots before starting. Suggested file roles are explained in [project setup](references/project-setup.md); existing names and layouts take priority.

### Everyday examples

| Task | Example message |
| --- | --- |
| Start | “Use $apex-controller-coach to start today's training from my latest handoff.” |
| Continue | “Continue today's session. I have finished the firing-range part; matches are still pending.” |
| Feedback | “Use $apex-controller-coach to help with the problem I describe, based on my latest records.” |
| Log results | “Today's session is over. Here is my actual practice time and feedback; record it and prepare the next handoff.” |
| Add a screenshot | “Read this account statistics screenshot. Update the comparable records without starting a new day.” |
| Review | “Use $apex-controller-coach to review the last week and suggest changes within my existing budget.” |
| Settings | “Read my confirmed controller settings and discuss this question. Keep suggestions separate from adopted settings.” |

For a past session, specify the real date. Approximate times are accepted. If you do not want account tracking or videos, say so; the rest of the workflow can continue.

### Where your data lives

Keep your personal project separate from this skill repository. Plans, current settings, screenshots, account statistics, and training progress belong to your project or the current chat. The skill folder stores reusable instructions only.

Cross-chat continuity relies on accessible, up-to-date files. An attachment in one chat may not be available in another. Keep the latest handoff in the project or bring the handoff into the next chat.

### Repository contents

```text
apex-controller-coach/
├── .gitignore
├── README.md
├── LICENSE.md
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── project-setup.md
    └── video-selection.md
```

### License

The instruction text and documentation are licensed under **CC BY-NC-SA 4.0**. See [LICENSE.md](LICENSE.md) and the [full license terms](https://creativecommons.org/licenses/by-nc-sa/4.0/legalcode.en) for attribution, noncommercial use, and ShareAlike conditions.

### Credits

Created by Arlowkey. Portions of the content were written with assistance from AI tools.

---

<a id="chinese"></a>

## 简体中文

### 简介

用于 Apex Legends 手柄训练的本地 Codex 技能：安排当天练习、承接训练反馈、记录实际完成情况，再把下次起点交接给后续聊天。

**使用你自己的手柄设置、训练目标与进度记录，普通 Codex 对话即可使用。**

显示名称：**Apex 手柄陪练**  
技能标识：`apex-controller-coach`

技能规则与默认回答以中文为主，也可要求使用其他语言回答。

### 核心功能与训练流程

| 阶段 | 主要内容 |
| --- | --- |
| 1. 读取交接 | 读取项目最新实际进度与下次起点。 |
| 2. 开场与计划 | 集中询问少量相关问题，按答复及已确认预算安排当天训练。 |
| 3. 训练中反馈 | 你反馈问题时提供帮助，不把某个历史问题固定为每日必问。 |
| 4. 记录与交接 | 保存实际训练、可选账号数据、未完成项与下次安排。 |
| 5. 周复盘 | 按需回顾可比进展，调整长期训练框架。 |

- **控制专项预算**：默认建议专项加记录约 30 分钟，以你已确认的预算为准。默认顺序为 Aim Lab（使用时）→ 靶场 → 按需休息 → 实战 → 收尾记录。实战时长在结束后记录，默认不设每天必须打多久。
- **准确衔接进度**：训练编号依据实际记录推进，与日历天数、聊天数量分别处理；同日继续不再次递增，计划内容不会记成已经完成。
- **沿用当前配置**：涉及设置时读取已确认配置，把建议与实际采用的设置分开记录。
- **读取截图**：直接读取账号或本人单局数据；只有统计范围一致且未重置的相邻累计记录才能计算新增，缺失项保持未知。
- **按需推荐视频**：集锦与每日小知识分开推荐、核验和去重；也可跳过视频。
- **依据实际表现复盘**：结合完成量、身体状态、交火反馈及可比数据，不承诺达到某段位的时间。

### 使用环境

本技能由规则与参考文档组成，不含可执行程序、安装脚本、游戏接口或自动遥测采集。

| 功能 | 所需能力 |
| --- | --- |
| 读取和使用技能 | 支持本地 skills 的 Codex 环境 |
| 跨聊天衔接 | 能读取 Apex 项目和最新记录 |
| 保存计划与记录 | 能写入该项目 |
| 读取账号或结算截图 | 图片读取能力 |
| 核验视频及当前机制、设备参数 | 联网能力；无法核验时会说明 |
| 自动命名每日训练聊天 | 可用的 Codex 聊天管理工具 |

Aim Lab 为可选项，没有时可采用靶场练习。没有聊天管理工具时可手动命名；没有文件写入能力时，会在聊天中交付可复用交接，并明确尚未保存。

### 安装

#### 方式一：让 Codex 帮你安装

1. 下载或克隆本仓库；如下载 ZIP，先解压，将技能文件夹命名为 `apex-controller-coach`。
2. 在本地 Codex 聊天中引用该文件夹，或提供它在电脑上的实际路径。
3. 发送：

   > 请把这个 apex-controller-coach 文件夹安装到本机 Codex 能发现的用户技能目录，保留完整目录结构。如果已有同名技能，请先告诉我。现在只安装，不启动训练或修改训练记录。安装后检查是否能调用 `$apex-controller-coach`。

4. 如系统要求授予安装目录的访问权限，按实际位置处理。

#### 方式二：手动安装

把整个文件夹放进用户技能目录：

```text
~/.agents/skills/apex-controller-coach/SKILL.md
```

Windows 路径示例：

```text
%USERPROFILE%\.agents\skills\apex-controller-coach\SKILL.md
```

保留 `SKILL.md`、`agents/` 与 `references/`，不要只复制入口文件，也不要套两层同名文件夹或重复安装。Codex 会自动检测技能变更；没有出现时可重启后检查。见 [官方技能发现说明](https://learn.chatgpt.com/docs/build-skills)。

### 调用方式与范围

在消息里引用 `$apex-controller-coach` 并说明本次任务。保留自动选择能力，Codex 也可能在请求匹配技能描述时选用它。

开始训练、同日继续、补记训练、读取截图、周复盘和设置咨询分别进入对应流程。仅上传截图不会自动开启新训练日；讨论、编辑或安装技能不会开始训练或变更训练进度。

技能不自动新建聊天或定时提醒。归档旧聊天需要你的授权。

### 第一次使用

#### 已有 Apex 项目

在该项目聊天中使用，或明确告诉陪练项目位置。例如：

> 使用 `$apex-controller-coach`，读取我现有 Apex 项目的规则和最新交接，开始今天的训练。先询问影响安排但尚不明确的信息，再给完整计划。沿用原有文件名和当前手柄设置。

技能会读取你项目中适用的 `AGENTS.md` 与已有记录，沿用原有文件名和目录结构。

#### 还没有训练记录

为个人训练选一个独立项目文件夹，发送：

> 使用 `$apex-controller-coach`，在我指定的文件夹建立 Apex 手柄训练项目。先了解我的平台、手柄经验、目标和专项可用时间，再给起步方案，把确认后的计划和必要记录保存到项目。现在不要把任何训练记为已经完成。

有当前键位与灵敏度时一并提供即可，不需要先填齐全部设备参数，也不要求先有账号截图。[项目准备说明](references/project-setup.md) 给出建议文件用途；已有名称和结构优先。

### 日常使用示例

| 任务 | 可发送的消息 |
| --- | --- |
| 每日开场 | “使用 `$apex-controller-coach`，根据最新交接开始今天的训练。” |
| 同日继续 | “继续今天的训练，靶场已经练完，实战还没开始。” |
| 反馈问题 | “使用 `$apex-controller-coach`，结合最新记录分析我这次反馈的问题。” |
| 日终打卡 | “今天结束了，这是实际用时和反馈，请记录并更新下次交接。” |
| 提供截图 | “读取这张账号数据页，更新可比记录，不开启新训练日。” |
| 周复盘 | “使用 `$apex-controller-coach`，复盘最近一周，在现有预算内提出调整。” |
| 设置咨询 | “读取我确认在用的手柄设置，讨论这个问题，把建议与已采用配置分开。” |

补记过去训练时说明实际日期；用时可以粗估。不想跟踪账号数据或不需要视频时，直接说明即可继续其余流程。

### 个人数据保存在哪里

个人项目与技能仓库分开保存。训练计划、当前设置、截图、账号数据及训练进度属于你的项目或当前聊天；技能目录只保存可复用方法。

跨聊天衔接依靠可读取的最新文件。同一聊天的附件未必能在另一个聊天直接读取，因此请把最新交接保存在项目中，或带入下次聊天。

### 仓库内容

```text
apex-controller-coach/
├── .gitignore
├── README.md                    本说明
├── LICENSE.md                   许可与署名
├── SKILL.md                     技能入口与共用规则
├── agents/
│   └── openai.yaml              显示名称、简介与默认提示
└── references/
    ├── project-setup.md         首次使用、文件用途与交接字段
    └── video-selection.md       视频核验、筛选与推荐去重
```

### 许可

本项目的指令文本与说明文档采用 **CC BY-NC-SA 4.0（署名—非商业性使用—相同方式共享 4.0 国际版）**。署名、非商业使用及相同方式共享条件详见 [LICENSE.md](LICENSE.md) 和 [完整许可条款](https://creativecommons.org/licenses/by-nc-sa/4.0/legalcode.en)。

### 制作说明

制作：Arlowkey；部分内容使用 AI 工具辅助编写。
