# longcode

> 🤖 长时间自主开发代理 - 从需求收集到代码部署的全流程自动化

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Version](https://img.shields.io/badge/version-1.0.0-green.svg)](skill.json)

longcode 是一个 Claude Code (Claude Code) 技能，能够帮助你完成大型开发任务。它会：
- 深度理解你的需求
- 自动拆解为小任务
- 自主执行开发工作
- 自动测试、审查、提交代码

**执行期间无需你参与，遇到问题自己解决或跳过。**

---

## ✨ 特性

- 🎯 **深度需求理解** - 交互式收集 10+ 个关键问题，确保理解完整
- 📋 **精细任务拆解** - 将大任务分解为 < 2 小时的小任务
- 🤖 **按需子代理** - 根据任务类型启动相关代理（前端/后端/测试/安全/审查）
- ✅ **严格验收** - 编译 → 测试 → 安全审查 → 代码审查，四道关卡
- 🔄 **失败重试** - 每个任务最多重试 3 次
- 📦 **自动 Git** - 每个任务独立提交到 feature 分支
- 🚫 **零交互** - 执行期间完全不问你问题
- ⏭️ **自动继续** - 完成任务后自动进入下一个

---

## 🚀 快速开始

### 触发方式

```
# 方式 1：使用 slash command
/longcode

# 方式 2：直接描述需求
用 longcode 创建一个实时聊天功能
```

---

## 📖 工作流程

```
┌─────────────────────────────────────────────────────────────┐
│ 阶段一：需求收集                                             │
│ (唯一与用户交互的阶段)                                       │
│ - 交互式提问 10+ 个问题                                      │
│ - 确保理解完整                                              │
└─────────────────────────────────────────────────────────────┘
                            ↓
┌─────────────────────────────────────────────────────────────┐
│ 阶段二：生成计划                                             │
│ - 创建详细任务计划 (每个任务 < 2小时)                        │
│ - 分析依赖关系                                               │
│ - 创建 Git feature 分支                                     │
└─────────────────────────────────────────────────────────────┘
                            ↓
┌─────────────────────────────────────────────────────────────┐
│ 阶段三：自主执行 (无需用户参与)                               │
│                                                             │
│  对每个任务:                                                │
│   1. 启动相关子代理 (2-3个)                                │
│   2. 执行开发                                               │
│   3. 验收检查 (4道关卡)                                    │
│   4. 通过 → Git 提交                                        │
│   5. 失败 → 重试 3 次                                      │
│   6. 仍失败 → 跳过，记录原因                                │
│   7. 自动继续下一个任务                                     │
│                                                             │
└─────────────────────────────────────────────────────────────┘
                            ↓
┌─────────────────────────────────────────────────────────────┐
│ 阶段四：完成报告                                             │
│ - 完成的任务列表                                             │
│ - 跳过/失败的任务及原因                                      │
│ - Git 合并建议                                              │
└─────────────────────────────────────────────────────────────┘
```

---

## 📁 文件结构

```
longcode/
├── README.md                    # 本文件
├── LICENSE                      # MIT 许可证
├── CONTRIBUTING.md              # 贡献指南
├── skill.json                   # 技能元数据
├── prompt.md                    # 主提示词
├── commands/
│   └── longcode.md             # slash command
├── templates/
│   ├── PLAN_TEMPLATE.md        # 计划文档模板
│   ├── SUMMARY_TEMPLATE.md     # 完成总结模板
│   └── STATE_TEMPLATE.json     # 状态文件模板
└── docs/
    └── skill.md                # 详细技术文档
```

---

## ⚙️ 配置

| 配置项 | 默认值 | 描述 |
|--------|--------|------|
| max_task_duration | 120 分钟 | 单任务最大执行时间 |
| max_retries | 3 | 验收失败重试次数 |
| git_branch_pattern | feature/longcode-{timestamp} | Git 分支命名模式 |
| log_level | balanced | 日志详细程度 |

详见 [skill.json](skill.json)

---

## 📝 验收标准

### 必选项（全部通过才能提交）

- ✅ 代码能编译/构建通过
- ✅ 相关测试通过
- ✅ 安全审查无 High/Critical 问题
- ✅ 代码审查通过（无 Critical 问题）

### 可选项

- ⏹️ 测试覆盖率 ≥ 80%
- ⏹️ 性能指标达标

---

## 🤝 贡献

欢迎贡献！请阅读 [CONTRIBUTING.md](CONTRIBUTING.md) 了解贡献流程。

---

## 📄 许可证

MIT License - 详见 [LICENSE](LICENSE)

---

## 🔗 相关链接

- [Claude Code 官方文档](https://docs.anthropic.com/en/docs/claude-code/overview)
- [Claude Code Skills](https://docs.anthropic.com/en/docs/claude-code/extend-your-capabilities-with-skills)
- [Axiom Skills](https://github.com/passionworkeer/axiom) - 另一个实用的 Claude Code 技能集

---

*Made with ❤️ by Claude + User*
