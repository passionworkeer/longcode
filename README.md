# longcode

> 🤖 Autonomous Development Agent for Claude Code
>
> 只需描述你的需求，longcode 会自主完成从需求分析到代码提交的全流程。

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Skill-blue)](skill.json)
[![Version](https://img.shields.io/badge/Version-1.0.0-green)](skill.json)

## 🎯 一句话说清楚

**longcode** 是一个 Claude Code 技能（Skill），能够让你像指挥项目经理一样开发软件——只需说出你想要什么，它会自动完成剩余所有工作。

```
你： "用 longcode 创建一个实时聊天功能"
longcode： "好的，让我开始..."

2小时后...
longcode： "✅ 完成！已提交 12 个任务到 feature 分支"
```

---

## ✨ 核心能力

| 能力 | 说明 |
|------|------|
| 🤖 **全自动化** | 一次描述需求，全程无需参与 |
| 📋 **智能拆解** | 自动将大任务拆成 < 2 小时的小任务 |
| 🛡️ **质量保证** | 编译 → 测试 → 安全 → 审查，四重关卡 |
| 🔄 **容错机制** | 失败自动重试 3 次，仍失败则跳过继续 |
| 📦 **原子提交** | 每个任务独立 Git 提交，可追溯可回滚 |
| 📊 **完整报告** | 生成计划、执行日志、完成总结 |

---

## 🚀 对比其他方案

| 方案 | 自动化程度 | 质量控制 | Git 管理 | 适用场景 |
|------|-----------|---------|---------|---------|
| **longcode** | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | 大型功能开发 |
| 手动开发 | ⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | 小任务 |
| Cursor/Copilot | ⭐⭐⭐ | ⭐⭐ | ⭐⭐ | 代码补全 |
| GPT Engineer | ⭐⭐⭐⭐ | ⭐⭐ | ⭐⭐ | 快速原型 |

---

## 📖 工作流程

```
┌─────────────────────────────────────────────────────────────────┐
│ 阶段 1：需求收集 (唯一与用户交互)                                │
│                                                                 │
│  longcode 会问你 10+ 个问题，确保完全理解你的需求：             │
│  - 功能描述、技术栈、数据模型、用户流程                         │
│  - 性能要求、安全要求、验收标准                                 │
└─────────────────────────────────────────────────────────────────┘
                                ↓
┌─────────────────────────────────────────────────────────────────┐
│ 阶段 2：生成计划                                                │
│                                                                 │
│  创建 LONGCODE_PLAN.md：                                        │
│  - 任务拆解（每个 < 2 小时）                                   │
│  - 依赖关系分析                                                 │
│  - Git feature 分支创建                                          │
└─────────────────────────────────────────────────────────────────┘
                                ↓
┌─────────────────────────────────────────────────────────────────┐
│ 阶段 3：自主执行 (无需用户参与)                                  │
│                                                                 │
│  对每个任务循环执行：                                           │
│    1. 启动相关子代理（前端/后端/测试/安全/审查）               │
│    2. 执行开发                                                  │
│    3. 验收检查：                                               │
│       ✅ 编译通过 → ✅ 测试通过 → ✅ 安全审查 → ✅ 代码审查    │
│    4. 通过 → Git 提交                                          │
│    5. 失败 → 重试 3 次                                         │
│    6. 仍失败 → 跳过并记录原因                                  │
│    7. 自动继续下一个任务                                        │
└─────────────────────────────────────────────────────────────────┘
                                ↓
┌─────────────────────────────────────────────────────────────────┐
│ 阶段 4：完成报告                                                │
│                                                                 │
│  生成 LONGCODE_SUMMARY.md：                                     │
│  - 完成的任务列表 + Git commits                                 │
│  - 跳过的任务及原因                                             │
│  - Git 合并建议                                                 │
└─────────────────────────────────────────────────────────────────┘
```

---

## 🕐 什么时候用

| 场景 | 推荐度 |
|------|--------|
| 实现一个完整的新功能 | ⭐⭐⭐⭐⭐ |
| 需要前后端同时开发 | ⭐⭐⭐⭐⭐ |
| 多个模块需要同时重构 | ⭐⭐⭐⭐ |
| 修复一个 bug | ⭐ (太小，用手动) |
| 写一个函数 | ⭐ (太小，用手动) |

---

## 📋 使用方法

### 触发方式

```bash
# 方式 1：slash command
/longcode

# 方式 2：直接描述需求
用 longcode 创建一个用户认证系统
用 longcode 实现实时聊天功能
用 longcode 开发一个博客系统
```

### 第一次使用

```
你： /longcode

longcode：
══════════════════════════════════════════════════════════════
🚀 longcode - 长时间自主开发代理
══════════════════════════════════════════════════════════════

我将帮你完成一个完整的开发任务。

工作流程：
1. 📋 了解你的需求（交互式提问）
2. 📝 制定详细计划
3. 🚀 自主执行（无需你参与）
4. ✅ 完成后报告结果

准备好了！请告诉我你想实现什么功能？
```

---

## ⚙️ 配置选项

在 `skill.json` 中可自定义：

| 配置项 | 默认值 | 说明 |
|--------|--------|------|
| `max_task_duration` | 120 分钟 | 单任务超时时间 |
| `max_retries` | 3 | 验收失败重试次数 |
| `git_branch_pattern` | feature/longcode-{ts} | 分支命名规则 |
| `log_level` | balanced | 日志详细程度 |
| `require_questions` | 10 | 需求收集问题数 |

---

## 📁 项目文件

```
longcode/
├── README.md                   # 本文件
├── LICENSE                     # MIT 许可证
├── CONTRIBUTING.md            # 贡献指南
├── CODE_OF_CONDUCT.md         # 行为准则
├── skill.json                 # 技能元数据
├── prompt.md                  # 主执行提示词
├── commands/
│   └── longcode.md           # /longcode 命令
├── templates/
│   ├── PLAN_TEMPLATE.md       # 计划文档模板
│   ├── SUMMARY_TEMPLATE.md   # 完成总结模板
│   └── STATE_TEMPLATE.json   # 状态文件模板
└── docs/
    └── skill.md              # 详细技术文档
```

---

## 🔧 安装

```bash
# 复制到 Claude Code 技能目录
cp -r longcode ~/.claude/skills/

# 重启 Claude Code 使其生效
```

---

## 🤝 贡献

欢迎贡献！请阅读 [CONTRIBUTING.md](CONTRIBUTING.md)。

---

## 📄 许可证

MIT License - 详见 [LICENSE](LICENSE)

---

## 🔗 相关链接

- [Claude Code 官方文档](https://docs.anthropic.com/en/docs/claude-code/overview)
- [Claude Code Skills 文档](https://docs.anthropic.com/en/docs/claude-code/extend-your-capabilities-with-skills)
- [Axiom Skills](https://github.com/passionworkeer/axiom) - 另一个 Claude Code 技能集

---

*让开发变得更简单*
