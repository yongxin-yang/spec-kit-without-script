# 实现计划：[FEATURE]

**分支**：`[###-feature-name]` | **日期**：[DATE] | **规格**：[link]
**输入**：来自 `/specs/[###-feature-name]/spec.md` 的功能规格说明

**注意**：此模板由 `/speckit.plan` 命令填写。有关执行工作流程，请参阅 `commands-zh/speckit.plan.md`。

## 摘要

[从功能规格中提取：主要需求 + 来自研究的技术方法]

## 技术背景

<!--
  需要操作：用项目的技术详细信息替换本节中的内容。
  此处的结构以咨询身份呈现，以指导迭代过程。
-->

**语言/版本**：[例如，Python 3.11、Swift 5.9、Rust 1.75 或需要澄清]  
**主要依赖项**：[例如，FastAPI、UIKit、LLVM 或需要澄清]  
**存储**：[如适用，例如，PostgreSQL、CoreData、文件或不适用]  
**测试**：[例如，pytest、XCTest、cargo test 或需要澄清]  
**目标平台**：[例如，Linux 服务器、iOS 15+、WASM 或需要澄清]
**项目类型**：[单一/网页/移动 - 决定源代码结构]  
**性能目标**：[特定领域，例如，1000 req/s、10k lines/sec、60 fps 或需要澄清]  
**约束条件**：[特定领域，例如，<200ms p95、<100MB 内存、离线功能或需要澄清]  
**规模/范围**：[特定领域，例如，10k 用户、1M LOC、50 个屏幕或需要澄清]

## 宪章检查

*门控：必须在第 0 阶段研究之前通过。在第 1 阶段设计后重新检查。*

[根据宪章文件确定的门控]

## 项目结构

### 文档（此功能）

```text
specs/[###-feature]/
├── plan.md              # 此文件（/speckit.plan 命令输出）
├── research.md          # 第 0 阶段输出（/speckit.plan 命令）
├── data-model.md        # 第 1 阶段输出（/speckit.plan 命令）
├── quickstart.md        # 第 1 阶段输出（/speckit.plan 命令）
├── contracts/           # 第 1 阶段输出（/speckit.plan 命令）
└── tasks.md             # 第 2 阶段输出（/speckit.tasks 命令 - 不由 /speckit.plan 创建）
```

### 源代码（仓库根目录）
<!--
  需要操作：用此功能的具体布局替换下面的占位符树。
  删除未使用的选项，并用真实路径扩展所选结构（例如，apps/admin、packages/something）。
  交付的计划不得包含选项标签。
-->

```text
# [如未使用则删除] 选项 1：单一项目（默认）
src/
├── models/
├── services/
├── cli/
└── lib/

tests/
├── contract/
├── integration/
└── unit/

# [如未使用则删除] 选项 2：Web 应用程序（当检测到"前端"+"后端"时）
backend/
├── src/
│   ├── models/
│   ├── services/
│   └── api/
└── tests/

frontend/
├── src/
│   ├── components/
│   ├── pages/
│   └── services/
└── tests/

# [如未使用则删除] 选项 3：移动 + API（当检测到"iOS/Android"时）
api/
└── [与上面的后端相同]

ios/ or android/
└── [平台特定结构：功能模块、UI 流程、平台测试]
```

**结构决策**：[记录所选结构并引用上面捕获的真实目录]

## 复杂性跟踪

> **仅在宪章检查有必须证明的违规时填写**

| 违规 | 为什么需要 | 拒绝更简单替代方案的原因 |
|-----------|------------|-------------------------------------|
| [例如，第 4 个项目] | [当前需求] | [为什么 3 个项目不足] |
| [例如，仓库模式] | [具体问题] | [为什么直接数据库访问不足] |
