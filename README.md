# ai-nichijyou

日常用的 AI skills 合集（AI の日常）。每个 skill 一个目录，放在 [`skills/`](skills/) 下，可用 [`skills`](https://github.com/vercel-labs/skills) CLI 安装到 Claude Code、Codex、Cursor 等 agent。

## Skills

| Skill | 用途 |
| --- | --- |
| [`deepen`](skills/deepen/SKILL.md) | 开工前做深一件事：并行派各学科的独立子代理，找出你想不到、但顶尖从业者会做的事，把任务改写成「更深而不是更大」的版本；做完后把暴露的盲区固化成检查 |
| [`state-machine`](skills/state-machine/SKILL.md) | 把有重试、轮询、多出口、失败恢复的小脚本写成声明式状态机（纯数据 machine + 动作函数 + 实时 ASCII 状态图）；线性流水线会被劝退。文章与 playground 见 [taterboom/state-machine](https://github.com/taterboom/state-machine) |
| [`unstick-procrastination`](skills/unstick-procrastination/SKILL.md) | 把一件一直拖着的事从模糊拆到清晰：先诊断拖延类型（模糊 / 决策 / 恐惧 / 厌烦 / 意义 / 疲劳），再给一个 30 分钟内能做的下一步，能一起做就当场一起做 |

## Install

安装全部：

```
npx skills add taterboom/ai-nichijyou -g
```

只装某一个：

```
npx skills add taterboom/ai-nichijyou -g -s deepen
```

查看仓库里有哪些 skill：

```
npx skills add taterboom/ai-nichijyou -l
```

本地开发时可以直接从目录安装：`npx skills add ./ -g -s <name>`。

## 新增 skill

```
skills/<name>/SKILL.md      # 必需，frontmatter 含 name 与 description；name 与目录名一致，用英文
skills/<name>/references/   # 可选，按需读取的参考资料
skills/<name>/scripts/      # 可选，skill 调用的脚本
```

加完后在上面的表格里补一行。

## License

MIT
