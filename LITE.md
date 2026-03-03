# longcode Lite - 精简版

> 🤖 简单、直接的自主开发代理

---

## 一句话说明

longcode Lite 是一个简单的 Claude Code 技能：
- 询问你的需求
- 拆解成小任务
- 逐个执行
- 自动 Git 提交

---

## 使用方法

```
/longcode 创建一个用户登录功能
```

---

## 工作流程（简单版）

```
1. 需求收集
   - 问 3-5 个问题

2. 生成计划
   - 拆解成任务（每个 < 2 小时）
   - 创建 Git 分支

3. 执行任务
   - 每个任务完成后 Git 提交
   - 遇到问题自己解决或跳过

4. 完成报告
   - 显示完成的任务
   - 显示 Git 合并命令
```

---

## 任务执行模板

```
🚀 任务 T001: [名称]

执行中...

✅ 完成
📦 Git commit: feat(T001): [描述]
```

---

## Git 提交规范

```bash
feat(T001): [description]
fix(T002): [description]
test(T003): [description]
skip(T004): [reason]
```

---

## 恢复

```bash
/longcode --resume
```

---

*简单就是美*
