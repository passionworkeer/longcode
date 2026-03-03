# 执行总结 - {{PROJECT_NAME}}

> 完成时间: {{COMPLETION_TIME}}
> 执行时长: {{DURATION}}
> Git 分支: {{GIT_BRANCH}}

---

## 📊 执行概览

| 指标 | 数值 |
|------|------|
| 总任务数 | {{TOTAL_TASKS}} |
| 已完成 | {{COMPLETED_TASKS}} |
| 跳过/失败 | {{FAILED_TASKS}} |
| 成功率 | {{SUCCESS_RATE}}% |
| Git 提交 | {{COMMITS}} 次 |
| 重试次数 | {{RETRY_COUNT}} |

---

## ✅ 完成的任务

| ID | 任务名称 | 代理 | 耗时 | 重试 | 提交 |
|----|---------|------|------|------|------|
| T001 | {{TASK_NAME}} | {{AGENT}} | {{DURATION}} | {{RETRY}} | {{COMMIT}} |
| T002 | {{TASK_NAME}} | {{AGENT}} | {{DURATION}} | {{RETRY}} | {{COMMIT}} |
| ... | ... | ... | ... | ... | ... |

---

## ❌ 跳过/失败的任务

| ID | 任务名称 | 失败原因 | 重试次数 |
|----|---------|---------|---------|
| T005 | {{TASK_NAME}} | {{FAILURE_REASON}} | 3 |
| T012 | {{TASK_NAME}} | {{FAILURE_REASON}} | 3 |

### 需要手动处理的问题

1. **T005: {{TASK_NAME}}**
   - 失败原因: {{FAILURE_REASON}}
   - 建议处理: {{SUGGESTION}}

2. **T012: {{TASK_NAME}}**
   - 失败原因: {{FAILURE_REASON}}
   - 建议处理: {{SUGGESTION}}

---

## 📁 创建/修改的文件

```
{{FILE_TREE}}
```

### 新增文件

| 文件 | 说明 |
|------|------|
| {{FILE_PATH}} | {{DESCRIPTION}} |

### 修改文件

| 文件 | 说明 |
|------|------|
| {{FILE_PATH}} | {{DESCRIPTION}} |

---

## 🧪 质量指标

| 指标 | 数值 | 状态 |
|------|------|------|
| 测试覆盖率 | {{COVERAGE}}% | {{STATUS}} |
| 代码审查 | {{REVIEW_COUNT}} 次 | {{STATUS}} |
| 安全审查 | {{SECURITY_COUNT}} 次 | {{STATUS}} |
| 编译警告 | {{WARNINGS}} | {{STATUS}} |
| 代码行数 | +{{LINES_ADDED}} / -{{LINES_REMOVED}} | - |

---

## 🔒 安全审查结果

| 检查项 | 结果 |
|--------|------|
| SQL 注入 | ✅ 通过 |
| XSS | ✅ 通过 |
| CSRF | ✅ 通过 |
| 敏感信息泄露 | ✅ 通过 |
| 依赖漏洞 | ✅ 无高危 |

---

## 🎯 验收标准

| 标准 | 状态 |
|------|------|
| {{CRITERION_1}} | ✅ |
| {{CRITERION_2}} | ✅ |
| {{CRITERION_3}} | ✅ |

---

## 📝 决策记录

| 决策 | 理由 |
|------|------|
| {{DECISION_1}} | {{REASON_1}} |
| {{DECISION_2}} | {{REASON_2}} |

---

## 🚀 部署状态

```
{{DEPLOYMENT_STATUS}}
```

---

## 💡 后续建议

1. {{SUGGESTION_1}}
2. {{SUGGESTION_2}}
3. {{SUGGESTION_3}}

---

## 🔄 Git 操作

### 当前状态
- 分支: `{{GIT_BRANCH}}`
- 提交数: {{COMMITS}}
- 状态: {{MERGE_STATUS}}

### 合并到主分支
```bash
# 查看更改
git checkout main
git diff {{GIT_BRANCH}}

# 如果一切正常，合并
git merge {{GIT_BRANCH}}

# 删除 feature 分支
git branch -d {{GIT_BRANCH}}
```

### 如果需要手动修复
```bash
# 保留 feature 分支，手动修复失败任务后再合并
git checkout {{GIT_BRANCH}}
# [手动修复...]
git checkout main
git merge {{GIT_BRANCH}}
```

---

## 📝 决策记录

| 时间 | 决策 | 理由 |
|------|------|------|
| {{TIME_1}} | {{DECISION_1}} | {{REASON_1}} |
| {{TIME_2}} | {{DECISION_2}} | {{REASON_2}} |

---

*生成: longcode skill v1.0.0*
*项目: {{PROJECT_NAME}}*
*完成时间: {{COMPLETION_TIME}}*
