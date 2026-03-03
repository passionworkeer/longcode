# 贡献指南

感谢你对 longcode 项目的兴趣！我们欢迎任何形式的贡献，包括但不限于：

- 🐛 报告 Bug
- 💡 提出新功能或改进建议
- 📝 完善文档
- 💻 提交代码修复或新功能

---

## 如何贡献

### 1. 报告 Bug

如果你发现了 bug，请：

1. 搜索 [Issues](https://github.com/passionworkeer/longcode/issues) 确保没有被报告过
2. 创建一个新的 Issue，包含：
   - 清晰的标题和描述
   - 复现步骤
   - 期望行为和实际行为
   - 环境和版本信息

### 2. 提出新功能

如果你有新功能的想法，请：

1. 搜索现有 Issues 和 PRs
2. 创建一个新的 Feature Request，包含：
   - 清晰的功能描述
   - 使用场景
   - 可能的实现方案
   - 任何相关的参考资料

### 3. 提交代码

#### 流程

1. **Fork** 本仓库
2. **Clone** 你的 Fork：
   ```bash
   git clone https://github.com/YOUR_USERNAME/longcode.git
   cd longcode
   ```

3. **创建**一个新分支：
   ```bash
   git checkout -b feature/your-feature-name
   # 或
   git checkout -b fix/bug-description
   ```

4. **修改**代码并提交：
   ```bash
   git add .
   git commit -m "feat: add new feature"
   # 或
   git commit -m "fix: resolve issue description"
   ```

5. **Push** 到你的 Fork：
   ```bash
   git push origin feature/your-feature-name
   ```

6. 创建 **Pull Request**

#### 提交信息规范

我们使用 [Conventional Commits](https://www.conventionalcommits.org/)：

```
<type>(<scope>): <description>

[可选的正文]

[可选的脚注]
```

类型 (type)：
- `feat`: 新功能
- `fix`: Bug 修复
- `docs`: 文档修改
- `style`: 代码格式（不影响功能）
- `refactor`: 重构（不影响功能）
- `test`: 测试相关
- `chore`: 构建/工具相关

示例：
```
feat(skill): add auto-retry mechanism
fix(prompt): correct acceptance criteria description
docs: update README with new examples
```

### 4. 完善文档

文档改进同样重要！包括：
- 拼写和语法修正
- 补充示例
- 完善 API 说明

---

## 开发设置

### 本地测试

```bash
# 复制技能到本地 Claude Code 配置
cp -r longcode ~/.claude/skills/

# 重启 Claude Code 使其生效
```

### 技能结构

```
longcode/
├── skill.json          # 技能元数据
├── prompt.md           # 主提示词
├── commands/           # slash commands
├── templates/          # 模板文件
└── docs/              # 详细文档
```

---

## 代码规范

### prompt.md

- 使用中文编写注释和说明
- 保持清晰的章节结构
- 每个规则块需要有明确的目的说明

### skill.json

- 遵循 JSON Schema 格式
- 保持配置项简洁明了

---

## 问题解答

### Q: 如何测试我的修改？

A: 将修改后的技能复制到 `~/.claude/skills/longcode/`，然后重启 Claude Code 即可测试。

### Q: 我的 PR 多久会被合并？

A: 我们会尽快审查，通常在 1-3 天内。如果长时间没有响应，请留言提醒。

### Q: 我可以添加新的配置项吗？

A: 可以！但请确保：
1. 有合理的默认值
2. 在 README.md 中说明用途
3. 不破坏现有功能

---

## 行为准则

请阅读并遵守我们的 [Code of Conduct](CODE_OF_CONDUCT.md)（如果适用）。

我们期待你的贡献！

---

*本贡献指南基于 [Contributing Guide Template](https://github.com/passionworkeer/axiom)*
