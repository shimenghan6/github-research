# github-research

> "帮我查一下 GitHub 上最火的 Python 爬虫框架"、"对比 React 和 Vue 生态"、"有没有类似 Redis 的国产替代"——跟 Claude 说句话，自动搜、读 README、排 Stars、出对比矩阵、给选型建议。

**会调研、会对比、会排名、会给建议。就像雇了个专门帮你翻 GitHub 的技术助理。**

### 谁需要这个

| 你 | 为什么你需要 |
|----|------------|
| 选开源方案时不知道用哪个 | 自动对比 Stars/功能/场景，帮你选 |
| 经常在 GitHub 上翻项目 | 一条命令完成搜索+详情+对比 |
| 想了解某个项目值不值得用 | 一键出调研报告：能力/局限/适用场景 |

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
