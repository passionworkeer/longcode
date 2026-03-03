# 项目名称 - longcode 执行计划

> 生成时间: {{TIMESTAMP}}
> 版本: 1.0.0

---

## 📋 元信息

| 属性 | 值 |
|------|-----|
| 项目名称 | {{PROJECT_NAME}} |
| 开始时间 | {{START_TIME}} |
| 预计结束 | {{ESTIMATED_END}} |
| 预计时长 | {{ESTIMATED_DURATION}} |
| 总任务数 | {{TOTAL_TASKS}} |
| 当前进度 | {{PROGRESS}} |

---

## 一、需求概述

### 1.1 功能描述

{{FEATURE_DESCRIPTION}}

### 1.2 用户场景

{{USER_SCENARIOS}}

### 1.3 验收标准

{{ACCEPTANCE_CRITERIA}}

---

## 二、技术栈

| 层级 | 技术选择 | 理由 |
|------|---------|------|
| 前端 | {{FRONTEND}} | {{FRONTEND_REASON}} |
| 后端 | {{BACKEND}} | {{BACKEND_REASON}} |
| 数据库 | {{DATABASE}} | {{DATABASE_REASON}} |
| 其他 | {{OTHER}} | {{OTHER_REASON}} |

---

## 三、架构设计

### 3.1 系统架构

```
{{ARCHITECTURE_DIAGRAM}}
```

### 3.2 数据模型

```typescript
{{DATA_MODEL_TYPESCRIPT}}
```

### 3.3 API 设计

| 端点 | 方法 | 描述 |
|------|------|------|
| {{ENDPOINT}} | {{METHOD}} | {{DESCRIPTION}} |

---

## 四、任务列表

### 4.1 任务组 A: 基础设施 (可并行)

| ID | 任务名称 | 负责代理 | 预估时间 | 依赖 | 状态 | Git Commit |
|----|---------|---------|---------|------|------|------------|
| T001 | {{TASK_NAME}} | {{AGENT}} | {{ESTIMATE}} | - | ⏳ pending | - |
| T002 | {{TASK_NAME}} | {{AGENT}} | {{ESTIMATE}} | - | ⏳ pending | - |
| T003 | {{TASK_NAME}} | {{AGENT}} | {{ESTIMATE}} | - | ⏳ pending | - |

### 4.2 任务组 B: 核心功能 (依赖组A)

| ID | 任务名称 | 负责代理 | 预估时间 | 依赖 | 状态 | Git Commit |
|----|---------|---------|---------|------|------|------------|
| T004 | {{TASK_NAME}} | {{AGENT}} | {{ESTIMATE}} | T001 | ⏳ pending | - |
| T005 | {{TASK_NAME}} | {{AGENT}} | {{ESTIMATE}} | T002 | ⏳ pending | - |
| T006 | {{TASK_NAME}} | {{AGENT}} | {{ESTIMATE}} | T003 | ⏳ pending | - |

### 4.3 任务组 C: 测试与文档 (依赖组B)

| ID | 任务名称 | 负责代理 | 预估时间 | 依赖 | 状态 | Git Commit |
|----|---------|---------|---------|------|------|------------|
| T007 | {{TASK_NAME}} | {{AGENT}} | {{ESTIMATE}} | T004,T005 | ⏳ pending | - |
| T008 | {{TASK_NAME}} | {{AGENT}} | {{ESTIMATE}} | T004,T005 | ⏳ pending | - |

---

## 五、依赖关系图

```
{{DEPENDENCY_GRAPH}}
```

---

## 六、执行日志

| 时间 | 任务 | 代理 | 状态 | 耗时 | Git Commit |
|------|------|------|------|------|------------|
| {{TIMESTAMP}} | T001 | Frontend | ✅ | 45min | a1b2c3d |
| {{TIMESTAMP}} | T002 | Backend | ✅ | 60min | d4e5f6g |
| ... | ... | ... | ... | ... | ... |

---

## 七、进度追踪

### 总体进度

```
进度: {{PROGRESS_BAR}} {{PERCENTAGE}}%
```

### 按状态

| 状态 | 数量 |
|------|------|
| ⏳ Pending | {{PENDING_COUNT}} |
| 🔄 In Progress | {{IN_PROGRESS_COUNT}} |
| ✅ Completed | {{COMPLETED_COUNT}} |
| ❌ Failed | {{FAILED_COUNT}} |

### 按代理

| 代理 | 已完成 | 进行中 | 待处理 |
|------|--------|--------|--------|
| Frontend | {{FRONTEND_DONE}} | {{FRONTEND_ACTIVE}} | {{FRONTEND_TODO}} |
| Backend | {{BACKEND_DONE}} | {{BACKEND_ACTIVE}} | {{BACKEND_TODO}} |
| Testing | {{TESTING_DONE}} | {{TESTING_ACTIVE}} | {{TESTING_TODO}} |
| Security | {{SECURITY_DONE}} | {{SECURITY_ACTIVE}} | {{SECURITY_TODO}} |

---

## 八、风险与问题

| 风险/问题 | 严重程度 | 状态 | 解决方案 |
|-----------|---------|------|---------|
| {{RISK}} | {{SEVERITY}} | {{STATUS}} | {{SOLUTION}} |

---

## 九、决策记录

| 时间 | 决策 | 理由 |
|------|------|------|
| {{TIMESTAMP}} | {{DECISION}} | {{REASON}} |

---

*文档生成: longcode skill v1.0.0*
*最后更新: {{LAST_UPDATE}}*
