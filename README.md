# 想清楚

一个用于 WorkBuddy 的对话 Skill：通过分轮追问，帮你厘清计划、决定和想法中的关键未知。需要可交付结果时，使用 `grill-with-docs` 模式，在追问结束后形成完整文档。

## 用法

安装后，在 WorkBuddy 对话中输入：

- `/想清楚 帮我想清楚这个方案：……`：直接调用 Skill，分轮追问，结束后交付文档。
- `拷打一下我的计划：……`：普通追问模式。可选择追问强度，以及是否记录决策。
- `grill-with-docs：帮我想清楚这个方案：……`：同样进入文档模式。

追问强度可选浅问、常规、细问、深挖、拷打，并可在过程中调整。

文档模式默认在当前可写项目的 `docs/<英文主题>.md` 保存 Markdown。你可以指定文档位置或格式；如果没有可写项目，Skill 会在对话中给出可复制的完整 Markdown。文档会区分已确认的决定、事实、推断、建议与待定问题。

## 安装

将仓库中的 `grill` 文件夹完整复制到 WorkBuddy 的用户技能目录 `~/.workbuddy/skills/`，使其包含 `~/.workbuddy/skills/grill/SKILL.md`。技能标识为“想清楚”，在对话输入 `/想清楚` 调用；如菜单尚未刷新，重新打开 WorkBuddy 对话。若 WorkBuddy 提供“上传 Skill”入口，也可将 `grill` 文件夹打包后导入。

## 来源与许可

本 Skill 基于 [nagi-studio/skills 的 grill](https://github.com/nagi-studio/skills/tree/main/skills/pondering/grill) 修改，增加了 `grill-with-docs` 文档交付模式。保留原项目的 MIT 许可证及版权声明，详见 [`grill/LICENSE`](grill/LICENSE)。

