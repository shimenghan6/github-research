# github-research

GitHub 项目调研与对比分析工具。一键搜索、获取详情、横向对比、给出选型建议。

## 安装

```bash
cp SKILL.md ~/.claude/skills/github-research/
```

## 使用

在 Claude Code 中说：

> "查一下 GitHub 上的 xxx"
> "对比一下 xxx 和 yyy"
> "有没有类似 xxx 的工具"
> "推荐几个 xxx 的 skill"

Agent 自动三步走：
1. 搜索发现（GitHub API / WebSearch）
2. 获取详情（curl README / WebFetch）
3. 对比输出（单项目详情 / 多项目矩阵）

## 功能

- 单项目调研：Stars、语言、安装、核心能力、适用场景、局限
- 多项目对比：排行表 + 功能矩阵 + 选型建议
- 磁盘缓存：`~/.claude/github-cache/` 24h 过期避免重复查询
- 并行调研：多项目同时 curl 加速

## License

MIT
