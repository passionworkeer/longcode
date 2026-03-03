# Agent Team - 代理团队

> 定义 longcode 中使用的子代理及其协作方式

---

## 代理列表

| 代理 | 文件 | 职责 |
|------|------|------|
| Frontend | `FRONTEND.md` | 前端开发、UI 组件 |
| Backend | `BACKEND.md` | 后端 API、数据库 |
| Testing | `TESTING.md` | 单元测试、集成测试 |
| Security | `SECURITY.md` | 安全审查、漏洞扫描 |
| Code Review | `CODE_REVIEW.md` | 代码质量审查 |

---

## 代理调用规则

### 按任务类型选择

| 任务类型 | 主要代理 | 辅助代理 |
|---------|---------|---------|
| UI 组件开发 | Frontend | Code Review |
| API 端点开发 | Backend | Security, Testing |
| 数据库 schema | Backend | Security |
| 测试编写 | Testing | Code Review |
| Bug 修复 | Frontend/Backend | Testing, Code Review |

### 代理协作流程

```
主代理 (longcode)
    │
    ├── 任务: "创建用户登录功能"
    │
    ├─→ Backend Agent
    │       ├── 创建 User model
    │       ├── 实现 /api/login 端点
    │       └── 输出报告
    │
    ├─→ Frontend Agent (并行)
    │       ├── 创建 LoginForm 组件
    │       └── 输出报告
    │
    ├─→ Testing Agent (等待 Backend)
    │       ├── 编写登录 API 测试
    │       └── 输出报告
    │
    ├─→ Security Agent (并行)
    │       ├── 检查登录代码安全
    │       └── 输出报告
    │
    └─→ Code Review Agent (最后)
            ├── 审查所有代码
            └── 输出最终报告
```

---

## 代理通信格式

### 任务分发

```
主代理 → 代理:
====================
任务: 实现用户登录 API
端点: POST /api/auth/login
技术栈: Node.js + Express
需求:
- 接受 email/password
- 验证凭据
- 返回 JWT token
====================
```

### 任务完成

```
代理 → 主代理:
====================
[Backend Agent] 完成报告

✅ 创建/修改:
  - src/api/auth/login.ts
  - src/middleware/auth.ts

📝 实现:
  - POST /api/auth/login
  - JWT token 生成
  - 密码验证

⚠️ 依赖:
  - 需要 Frontend Agent 处理 token 存储

✅ 状态: 完成
====================
```

### 任务失败

```
代理 → 主代理:
====================
[Backend Agent] 失败报告

❌ 任务: 实现数据库连接
📝 原因:
  - 无法连接到数据库
  - 环境缺少数据库驱动

🔄 尝试:
  1. 安装 pg 驱动
  2. 检查连接字符串

📋 需要帮助:
  - 数据库连接配置
====================
```

---

## 代理数量限制

- **最大并行代理数**: 3
- **单个任务最大代理数**: 2
- **等待超时**: 30 分钟

---

## 执行模式

### 串行模式 (默认)
```
任务 A → 任务 B → 任务 C
```

### 并行模式 (可选)
```
任务 A ─┬─→ 代理 1
        ├─→ 代理 2
        └─→ 代理 3
```

---

## 代理状态

| 状态 | 描述 |
|------|------|
| idle | 空闲，等待任务 |
| working | 执行任务中 |
| completed | 任务完成 |
| failed | 任务失败 |
| blocked | 被阻塞（等待其他代理） |

---

## 错误处理

### 代理失败
1. 记录失败原因
2. 最多重试 2 次
3. 仍然失败则跳过任务

### 代理超时
- 单个代理最大等待: 30 分钟
- 超时后标记为失败

### 代理冲突
- 如果两个代理修改同一文件，后执行的代理需要 rebase

---

*Agent Team 定义 - v1.6.0*
