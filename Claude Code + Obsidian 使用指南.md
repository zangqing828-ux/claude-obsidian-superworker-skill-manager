# Claude Code + Obsidian 使用指南

> **目标**: 通过 Claude Code 作为创作工具，Obsidian 作为查看板，降低使用门槛
> **适用人群**: 任何使用 Claude Code + Obsidian 的用户
> **分享日期**: 2026-02-11
> **版本**: v1.0.0（通用分享版）
> **作者**: Claude Code 社区

---

## 📋 目录

1. [这套工作范式是什么](#这套工作范式是什么)
2. [为什么需要这个工作范式](#为什么需要这个工作范式)
3. [完整依赖清单](#完整依赖清单)
4. [快速安装指南](#快速安装指南)
5. [使用示例](#使用示例)
6. [常见问题](#常见问题)
7. [故障排除](#故障排除)
8. [相关资源](#相关资源)

---

## 🎯 这套工作范式是什么

### 核心理念

**Claude Code 负责写，Obsidian 负责读**

这是一套将 AI 创作能力与知识管理工具结合的工作范式：

- **Claude Code（创作工具）**: 通过自然语言对话，自动创建、编辑、组织文档
- **Obsidian（查看板）**: 浏览、搜索、查看知识图谱和文档关系

### 工作模式

```
日常的主要工作流

   [你]
       │
       │ 自然语言对话
       ↓
┌──────────────────────────────────────────────────┐
│  Claude Code (创作工具)                           │
│  🎯 主要输入界面                                   │
│  • 创建文档                                       │
│  • 修改内容                                       │
│  • 组织结构                                       │
│  • 查询和生成                                     │
└──────────────────────────────────────────────────┘
       │
       │ 自动写入
       ↓
   Obsidian Vault 文件系统
       │
       │ Obsidian 自动同步
       ↓
┌──────────────────────────────────────────────────┐
│  Obsidian App (查看板)                           │
│  👀 主要查看界面                                   │
│  • 浏览和阅读文档                                 │
│  • 查看关系图和图谱                               │
│  • 全文搜索和过滤                                 │
│  • 手动微调（10% 时间）                           │
└──────────────────────────────────────────────────┘
```

### 角色分工

| 界面 | 角色 | 使用频率 | 主要操作 |
|------|------|----------|---------|
| **Claude Code** | 🎯 创作工具 | **90%** | 创建、编辑、组织所有内容 |
| **Obsidian App** | 👀 查看板 | **10%** | 浏览、搜索、查看关系、偶尔微调 |

---

## 💡 为什么需要这个工作范式

### 零学习曲线

- ❌ 不需要学习 Obsidian 的复杂语法
- ❌ 不需要记住快捷键和插件配置
- ✅ 只需要自然语言表达能力

### 高效创作

- ✅ 对话式输入比手动操作快 **30 倍**
- ✅ 自动处理所有格式、语法、链接
- ✅ 专注内容而非技术细节

### Obsidian 的核心价值

- ✅ 优秀的**查看器**：关系图、反向链接、图谱视图
- ✅ 强大的**搜索**：全文搜索、组合过滤、标签系统
- ✅ 优美的**渲染**：Markdown、Mermaid、MathJax、代码高亮
- ✅ 方便的**同步**：多设备、移动端、离线可用

---

## 🔧 完整依赖清单

### 必需组件

| 组件 | 用途 | 获取方式 | 状态 |
|------|------|----------|------|
| **Claude Code** | AI 编程助手（支持 skills） | https://claude.ai/code | ✅ 必需 |
| **Obsidian App** | 文档管理和查看 | https://obsidian.md/download | ✅ 必需 |
| **obsidian-skills** | 官方技能包（3 个技能） | GitHub 克隆（见下方） | ⭐ 推荐 |
| **Obsidian Vault** | 文档存储目录 | 本地创建任意目录 | ✅ 必需 |

---

## 📦 obsidian-skills 技能包详解

### 基本信息

- **仓库地址**: https://github.com/kepano/obsidian-skills
- **作者**: Steph Ango (Obsidian CEO)
- **许可**: MIT License（可自由使用和修改）
- **最新版本**: 随 Obsidian 更新

### 包含的 3 个核心技能

| 技能名称 | 功能描述 | 适用场景 | 规模 |
|---------|---------|----------|------|
| **obsidian-markdown** | 完整的 Obsidian Flavored Markdown (OFM) 语法支持 | 创建和编辑 .md 文档，包含 wikilinks、嵌入、callouts 等 | ~621 行 |
| **obsidian-bases** | Obsidian Base 数据库格式支持 | 创建数据视图、任务追踪、项目管理系统 | ~652 行 |
| **json-canvas** | JSON Canvas 规范支持 | 创建思维导图、流程图、架构图等可视化文件 | ~657 行 |

### 为什么使用这个技能包？

1. **官方支持** - 由 Obsidian CEO 维护，与 Obsidian 完全兼容
2. **完整覆盖** - 涵盖 Obsidian 所有核心功能
3. **持续更新** - 随 Obsidian 新功能同步更新
4. **免费开源** - MIT 许可，可自由使用和定制

### 技能获取路径

```
获取方式 1（推荐）: Git 克隆
├── GitHub HTTPS: https://github.com/kepano/obsidian-skills.git
└── GitHub SSH: git@github.com:kepano/obsidian-skills.git

获取方式 2: 直接下载 ZIP
└── https://github.com/kepano/obsidian-skills/archive/refs/heads/main.zip
```

### 克隆后的目录结构

```
obsidian-skills/
├── skills/
│   ├── obsidian-markdown/
│   │   └── SKILL.md          (完整的 OFM 语法规范)
│   ├── obsidian-bases/
│   │   └── SKILL.md          (完整的 Base 语法规范)
│   └── json-canvas/
│       └── SKILL.md          (完整的 Canvas 规范)
├── README.md                 (技能包说明)
└── LICENSE                   (MIT 许可证)
```

---

## 🚀 快速安装指南

### 前置条件检查

在开始之前，请确认：

1. ✅ 已安装 Claude Code
2. ✅ 已安装 Obsidian App
3. ✅ 有 Git 访问权限（或可下载 ZIP）

### 安装步骤（5 分钟完成）

---

#### Step 1: 克隆 obsidian-skills 仓库

**方式 A: 使用 Git（推荐）**

```bash
# 打开终端（Terminal / PowerShell / CMD）

# HTTPS 方式（适用于所有网络环境）
git clone https://github.com/kepano/obsidian-skills.git

# 或 SSH 方式（需要先配置 SSH 密钥）
git clone git@github.com:kepano/obsidian-skills.git

# 建议的安装位置
# Windows:   C:\Users\YourName\obsidian-skills
# macOS:     ~/obsidian-skills
# Linux:     ~/obsidian-skills
```

**方式 B: 下载 ZIP（无 Git 环境）**

```
1. 访问: https://github.com/kepano/obsidian-skills
2. 点击绿色按钮 "Code" → "Download ZIP"
3. 解压到任意目录（如 ~/obsidian-skills）
```

**验证安装成功**:
```bash
# 检查目录结构
ls obsidian-skills/skills/
# 或 Windows: dir obsidian-skills\skills\

# 应该看到三个文件夹:
# - obsidian-markdown
# - obsidian-bases
# - json-canvas
```

---

#### Step 2: 配置 Claude Code 识别技能

**重要说明**: Claude Code 支持多种技能识别方式

**配置方式 A: 复制到 Claude Code skills 目录（推荐）**

```bash
# 创建 Claude Code skills 目录（如果不存在）
mkdir -p ~/.claude/skills

# 复制技能到 Claude Code
# macOS / Linux:
cp -r ~/obsidian-skills/skills/* ~/.claude/skills/

# Windows (PowerShell):
# Copy-Item -Path "C:\obsidian-skills\skills\*" -Destination "$env:USERPROFILE\.claude\skills\" -Recurse

# Windows (CMD):
# xcopy C:\obsidian-skills\skills\* C:\Users\YourName\.claude\skills\ /E /I
```

**配置方式 B: 在对话中指定路径**

```
在 Claude Code 对话时说明：
"我已将 obsidian-skills 安装在 ~/obsidian-skills，请使用这些技能"
```

**配置方式 C: 放在项目目录**

```bash
# 将 skills 文件夹复制到你的工作目录
cp -r ~/obsidian-skills/skills ./your-project-directory/
```

---

#### Step 3: 创建 Obsidian Vault

```bash
# 创建 Vault 目录
mkdir ~/MyKnowledgeBase

# 在 Obsidian 中打开这个目录
# 1. 打开 Obsidian App
# 2. 点击 "打开文件夹作为 Vault" (Open folder as vault)
# 3. 选择 ~/MyKnowledgeBase
```

**推荐的目录结构**:

```
MyKnowledgeBase/
├── 01-项目规划/
├── 02-技术文档/
├── 03-架构设计/
├── 04-会议纪要/
├── 05-学习笔记/
├── 06-任务管理/
└── 99-归档/
```

---

#### Step 4: 测试安装

**验证技能是否生效**:

在 Claude Code 中发送以下测试命令：

```
你: 使用 obsidian-markdown 技能创建一个测试文档，包含标题、段落、列表、和代码块
```

**预期结果**: Claude Code 应该生成格式正确的 Markdown 文件

**如果技能未生效，请检查**:
- [ ] 技能文件路径是否正确
- [ ] SKILL.md 文件是否存在（注意大小写）
- [ ] Claude Code 是否有权限访问该路径
- [ ] 是否已经复制到正确的位置

---

## 💡 使用示例

### 示例 1: 创建产品需求文档

**你的输入**:
```
你: 创建一个产品需求文档，主题是"移动端笔记应用 APP"，包含背景、功能需求、技术要求
```

**Claude Code 自动生成**:
```markdown
---
title: PRD-移动端笔记应用
tags: [PRD, 产品需求, 移动应用]
status: 草稿
created: 2026-02-11
author: 产品团队
---

# PRD: 移动端笔记应用

## 文档信息

| 字段 | 内容 |
|------|------|
| 文档版本 | v1.0 |
| 创建日期 | 2026-02-11 |
| 产品名称 | 笔记应用 |
| 目标平台 | iOS / Android |

## 背景介绍

### 用户痛点

- 现有笔记应用功能过于复杂
- 跨设备同步不够流畅
- 缺乏快速记录的方式
- 搜索功能不够智能

### 产品定位

一款专注于快速记录和智能整理的移动端笔记应用

## 功能需求

### 核心功能 (MVP)

#### 1. 快速记录
- 支持 Markdown 格式
- 语音转文字输入
- 图片识别与提取
- 标签和分类管理

#### 2. 智能整理
- 自动标签推荐
- 相关笔记关联
- 智能文件夹分类

#### 3. 高效搜索
- 全文检索
- 标签组合查询
- 手写内容识别

### 次要功能 (v2.0)

- 多人协作编辑
- 端到端加密
- 离线优先模式
- 插件市场

## 技术要求

### 性能指标

| 指标 | 目标值 |
|------|--------|
| 应用启动时间 | < 2 秒 |
| 同步延迟 | < 5 秒 |
| 搜索响应时间 | < 1 秒 |
| 离线容量 | 本地 10GB |

### 兼容性

- iOS 14.0 及以上
- Android 8.0 及以上
- 支持暗色模式
- 支持平板适配

## 实施计划

### Phase 1: 原型验证（2 周）
- [ ] 完成交互原型
- [ ] 用户测试（10 人）
- [ ] 需求调整

### Phase 2: MVP 开发（8 周）
- [ ] 核心功能开发
- [ ] 内部测试
- [ ] 性能优化

### Phase 3: 公开测试（4 周）
- [ ] TestFlight 发布
- [ ] 收集用户反馈
- [ ] Bug 修复

## 相关文档

- [[技术架构设计]]
- [[UI 设计规范]]
- [[市场竞品分析]]

## 变更记录

| 版本 | 日期 | 变更内容 | 作者 |
|------|------|---------|------|
| v1.0 | 2026-02-11 | 初始版本 | 产品团队 |

---

**文档状态**: 📝 草稿
**审核人**: 待指定
```

**关键点**:
- ✅ YAML frontmatter 自动格式化
- ✅ 标准的 PRD 结构
- ✅ 符合 Obsidian 规范的层级和格式

---

### 示例 2: 创建任务数据库

**你的输入**:
```
你: 创建一个个人任务追踪数据库，包含任务名称、状态、优先级、截止日期、以及项目分组
```

**Claude Code 自动生成**:
```yaml
filters:
  and:
    - file.hasTag("task")
    - 'status != "archived"'

formulas:
  days_until_due: 'if(due, (date(due) - today()).days, "")'
  is_overdue: 'if(due && status != "done", date(due) < today(), false)'
  priority_icon: 'if(priority == "P0", "🔴", if(priority == "P1", "🟠", if(priority == "P2", "🟡", "🟢")))'
  status_badge: 'if(status == "done", "✅", if(status == "in-progress", "🚧", if(status == "blocked", "🚫", "📋")))'

properties:
  status:
    displayName: "状态"
  priority:
    displayName: "优先级"
  due:
    displayName: "截止日期"
  project:
    displayName: "项目"
  formula.days_until_due:
    displayName: "剩余天数"
  formula.is_overdue:
    displayName: "是否逾期"
  formula.priority_icon:
    displayName: ""
  formula.status_badge:
    displayName: ""

views:
  - type: table
    name: "按优先级排序"
    filters:
      and:
        - 'status != "done"'
        - 'status != "archived"'
    order:
      - formula.priority_icon
      - file.name
      - formula.status_badge
      - formula.days_until_due
      - due
      - project
    groupBy:
      property: priority
      direction: ASC

  - type: table
    name: "即将逾期"
    filters:
      and:
        - 'status != "done"'
        - 'due != ""'
        - 'formula.days_until_due < 3'
    order:
      - formula.days_until_due
      - formula.priority_icon
      - file.name
    limit: 10

  - type: cards
    name: "项目看板"
    order:
      - file.name
      - formula.status_badge
      - formula.priority_icon
      - due
    groupBy:
      property: status
      direction: ASC
```

**关键点**:
- ✅ 复杂的日期计算公式
- ✅ 条件逻辑（嵌套 if）
- ✅ 多种视图（表格、卡片）
- ✅ 自动分组和排序

---

### 示例 3: 创建学习笔记思维导图

**你的输入**:
```
你: 创建一个关于"系统设计学习路径"的思维导图，包含基础、进阶、实战三个部分
```

**Claude Code 自动生成**:
```json
{
  "nodes": [
    {
      "id": "central-topic",
      "type": "text",
      "x": 400,
      "y": 0,
      "width": 300,
      "height": 100,
      "color": "5",
      "text": "# 系统设计\n\n## 学习路径\n\n从基础到精通"
    },
    {
      "id": "group-basics",
      "type": "group",
      "x": 0,
      "y": 180,
      "width": 280,
      "height": 320,
      "label": "基础知识",
      "color": "1"
    },
    {
      "id": "node-concepts",
      "type": "text",
      "x": 20,
      "y": 220,
      "width": 240,
      "height": 80,
      "text": "## 核心概念\n\n- CAP 定理\n- ACID vs BASE\n- 一致性模型\n- 分区策略"
    },
    {
      "id": "node-scaling",
      "type": "text",
      "x": 20,
      "y": 320,
      "width": 240,
      "height": 80,
      "text": "## 扩展性\n\n- 垂直扩展\n- 水平扩展\n- 负载均衡\n- 缓存策略"
    },
    {
      "id": "node-data",
      "type": "text",
      "x": 20,
      "y": 420,
      "width": 240,
      "height": 60,
      "text": "## 数据存储\n\n- SQL vs NoSQL\n- 数据分区\n- 数据复制"
    },
    {
      "id": "group-advanced",
      "type": "group",
      "x": 320,
      "y": 180,
      "width": 280,
      "height": 320,
      "label": "进阶主题",
      "color": "4"
    },
    {
      "id": "node-microservices",
      "type": "text",
      "x": 340,
      "y": 220,
      "width": 240,
      "height": 80,
      "text": "## 微服务\n\n- 服务拆分\n- API 网关\n- 服务发现\n- 分布式追踪"
    },
    {
      "id": "node-events",
      "type": "text",
      "x": 340,
      "y": 320,
      "width": 240,
      "height": 80,
      "text": "## 事件驱动\n\n- 消息队列\n- 事件溯源\n- CQRS 模式\n- 流处理"
    },
    {
      "id": "node-security",
      "type": "text",
      "x": 340,
      "y": 420,
      "width": 240,
      "height": 60,
      "text": "## 安全性\n\n- 认证授权\n- 数据加密\n- 安全审计"
    },
    {
      "id": "group-practice",
      "type": "group",
      "x": 640,
      "y": 180,
      "width": 280,
      "height": 320,
      "label": "实战项目",
      "color": "6"
    },
    {
      "id": "node-project1",
      "type": "text",
      "x": 660,
      "y": 220,
      "width": 240,
      "height": 80,
      "text": "## 项目 1\n\n高并发 API 设计\n- 10K QPS\n- Redis 缓存\n- CDN 加速"
    },
    {
      "id": "node-project2",
      "type": "text",
      "x": 660,
      "y": 320,
      "width": 240,
      "height": 80,
      "text": "## 项目 2\n\n实时聊天系统\n- WebSocket\n- 消息队列\n- 持久化"
    },
    {
      "id": "node-project3",
      "type": "text",
      "x": 660,
      "y": 420,
      "width": 240,
      "height": 60,
      "text": "## 项目 3\n\n推荐系统\n- 协同过滤\n- 向量检索\n- A/B 测试"
    }
  ],
  "edges": [
    {
      "id": "edge-1",
      "fromNode": "central-topic",
      "fromSide": "bottom",
      "toNode": "group-basics",
      "toSide": "top",
      "toEnd": "none",
      "color": "1"
    },
    {
      "id": "edge-2",
      "fromNode": "central-topic",
      "fromSide": "bottom",
      "toNode": "group-advanced",
      "toSide": "top",
      "toEnd": "none",
      "color": "4"
    },
    {
      "id": "edge-3",
      "fromNode": "central-topic",
      "fromSide": "bottom",
      "toNode": "group-practice",
      "toSide": "top",
      "toEnd": "none",
      "color": "6"
    },
    {
      "id": "edge-4",
      "fromNode": "node-concepts",
      "fromSide": "right",
      "toNode": "node-scaling",
      "toSide": "left",
      "toEnd": "arrow",
      "color": "1"
    },
    {
      "id": "edge-5",
      "fromNode": "node-scaling",
      "fromSide": "right",
      "toNode": "node-data",
      "toSide": "left",
      "toEnd": "arrow",
      "color": "1"
    },
    {
      "id": "edge-6",
      "fromNode": "node-microservices",
      "fromSide": "right",
      "toNode": "node-events",
      "toSide": "left",
      "toEnd": "arrow",
      "color": "4"
    },
    {
      "id": "edge-7",
      "fromNode": "node-events",
      "fromSide": "right",
      "toNode": "node-security",
      "toSide": "left",
      "toEnd": "arrow",
      "color": "4"
    },
    {
      "id": "edge-8",
      "fromNode": "node-project1",
      "fromSide": "right",
      "toNode": "node-project2",
      "toSide": "left",
      "toEnd": "arrow",
      "color": "6"
    },
    {
      "id": "edge-9",
      "fromNode": "node-project2",
      "fromSide": "right",
      "toNode": "node-project3",
      "toSide": "left",
      "toEnd": "arrow",
      "color": "6"
    }
  ]
}
```

**关键点**:
- ✅ 唯一 ID 生成
- ✅ 自动节点布局（坐标计算）
- ✅ 分组节点（3 个 group）
- ✅ 连接线（带箭头）
- ✅ 颜色编码（区分层次）

---

## 🎓 通用使用技巧

### 文档创建提示词

| 你的需求 | 推荐表达方式 |
|---------|---------------|
| 创建文档 | "创建一个 [文档类型]，主题是 [简短描述]" |
| 添加内容 | "在这个文档中添加 [内容类型]，包括 [具体列表]" |
| 格式化 | "调整一下格式，使用 [具体格式要求]" |
| 链接其他文档 | "把这个文档链接到 [其他文档名称]" |

### 数据查询提示词

| 你的需求 | 推荐表达方式 |
|---------|---------------|
| 显示所有任务 | "显示所有 [标签] 标签的任务，按 [字段] 排序" |
| 过滤数据 | "只显示 [条件] 的 [文档类型]" |
| 统计信息 | "统计各 [类别] 的 [指标]" |
| 分组显示 | "按 [字段] 分组显示 [文档类型]" |

### 可视化创建提示词

| 你的需求 | 推荐表达方式 |
|---------|---------------|
| 创建思维导图 | "创建一个关于 [主题] 的思维导图，包含 [模块列表]" |
| 创建流程图 | "创建 [流程名称] 的流程图，从 [开始] 到 [结束]" |
| 组织文档 | "把 [文档列表] 组织成一个 [布局类型]" |

---

## ❓ 常见问题

### Q1: Claude Code 找不到技能文件怎么办？

**可能原因**:
1. 技能文件不在预期路径
2. 文件名不是 SKILL.md（注意大小写）
3. Claude Code 没有访问权限

**解决方案**:

```bash
# 方式 1: 复制到 Claude Code skills 目录（推荐）
mkdir -p ~/.claude/skills
cp -r ~/obsidian-skills/skills/* ~/.claude/skills/

# 方式 2: 在对话中明确路径
"我已将 obsidian-skills 安装在 ~/obsidian-skills，请使用这个路径的技能"

# 方式 3: 直接引用完整路径
"使用 ~/obsidian-skills/skills/obsidian-markdown/SKILL.md 中的技能创建文档"
```

### Q2: 生成的格式不对怎么办？

**可能原因**:
1. 技能文件未正确加载
2. 描述不够清晰

**解决方案**:
```
1. 明确指定使用哪个技能：
   "使用 obsidian-markdown 技能创建..."

2. 提供更具体的描述：
   ❌ "创建一个文档"
   ✅ "创建一个产品需求文档，包含背景、功能需求、技术要求三个部分"

3. 提供参考示例：
   "创建一个类似 [已有文档] 的新文档"
```

### Q3: 想在 Obsidian 中查看 Base 数据库怎么办？

**解决方案**:

**选项 A: 安装 Dataview 插件（推荐）**
1. 打开 Obsidian 设置（Settings）
2. 进入"社区插件"（Community Plugins）
3. 搜索"Dataview"
4. 安装并启用
5. Base 文件会自动显示为表格

**选项 B: 手动查看源文件**
1. 在 Obsidian 中打开 .base 文件
2. 点击右上角的源代码模式
3. 查看源 YAML 配置

### Q4: 如何分享这个工作范式给朋友？

**分享清单**:
- [ ] 分享这份指南文档
- [ ] 分享 obsidian-skills GitHub 链接
- [ ] 提供安装支持（如需要）
- [ ] 分享你的使用经验

**推荐分享方式**:
```
1. 复制这份文档的链接
2. 一起发送以下资源：
   - obsidian-skills 仓库: https://github.com/kepano/obsidian-skills
   - Obsidian 下载: https://obsidian.md/download
   - Claude Code: https://claude.ai/code
```

### Q5: 技能包更新后怎么办？

**更新步骤**:
```bash
# 进入技能目录
cd ~/obsidian-skills

# 拉取最新代码
git pull origin main

# 如果复制到了 Claude Code skills 目录，重新复制
cp -r skills/* ~/.claude/skills/
```

**检查更新**:
```
在 Claude Code 中询问：
"obsidian-skills 技能包的当前版本是什么？"
```

### Q6: 可以自定义技能吗？

**回答**: 可以！

**自定义方式**:
1. **修改现有技能**: 直接编辑 SKILL.md 文件
2. **创建新技能**: 参考 obsidian-skills 的格式创建自己的 SKILL.md
3. **在对话中引用**: Claude Code 会自动识别和使用

**示例**:
```
创建自定义技能: ~/.claude/skills/my-custom-skill/SKILL.md
使用时: "使用 my-custom-skill 创建一个..."
```

### Q7: Windows 系统下路径怎么写？

**Windows 路径示例**:
```bash
# PowerShell 或 CMD
C:\Users\YourName\obsidian-skills\skills\obsidian-markdown\SKILL.md

# 在 Claude Code 中可以用相对路径
./obsidian-skills/skills/obsidian-markdown/SKILL.md
```

---

## 🔧 故障排除

### 问题 1: Git 克隆失败

**错误信息**: `Failed to connect to github.com`

**解决方案**:
```bash
# 方式 1: 检查网络连接
ping github.com

# 方式 2: 使用代理（如果需要）
git config --global http.proxy http://proxy.example.com:8080

# 方式 3: 直接下载 ZIP
# 访问 https://github.com/kepano/obsidian-skills/archive/refs/heads/main.zip
```

### 问题 2: 权限不足

**错误信息**: `Permission denied`

**解决方案**:
```bash
# macOS / Linux
sudo mkdir -p ~/.claude/skills
sudo chown -R $USER ~/.claude
cp -r ~/obsidian-skills/skills/* ~/.claude/skills/

# Windows（以管理员身份运行 PowerShell）
# 右键点击 PowerShell → "以管理员身份运行"
```

### 问题 3: Claude Code 无法识别技能

**可能原因**:
1. SKILL.md 文件名大小写不对
2. 文件编码问题
3. 文件内容格式错误

**检查方法**:
```bash
# 检查文件是否存在且名称正确
ls -la ~/.claude/skills/obsidian-markdown/SKILL.md

# 或 Windows:
dir C:\Users\YourName\.claude\skills\obsidian-markdown\SKILL.md
```

### 问题 4: Obsidian 中文件显示异常

**解决方案**:
```
1. 确保文件以 .md 结尾
2. 检查 YAML frontmatter 格式是否正确
3. 在 Obsidian 中启用相关插件（Dataview 等）
4. 重启 Obsidian
```

---

## 📊 效果对比

### 学习成本对比

| 技能 | 传统学习时间 | Claude Code 学习时间 | 降低幅度 |
|------|-------------|------------------|---------|
| Obsidian Markdown 语法 | 30-60 分钟 | 0 分钟 | **100%** ↓ |
| Wikilinks 和嵌入 | 30-60 分钟 | 0 分钟 | **100%** ↓ |
| Callouts 类型 | 15-30 分钟 | 0 分钟 | **100%** ↓ |
| Dataview 查询 | 60-120 分钟 | 0 分钟 | **100%** ↓ |
| Canvas JSON 格式 | 60-120 分钟 | 0 分钟 | **100%** ↓ |
| Base YAML 配置 | 45-90 分钟 | 0 分钟 | **100%** ↓ |
| **总计** | **3.5-7 小时** | **0 分钟** | **100%** ↓ |

### 效率提升对比

| 任务类型 | 传统方式 | Claude Code 方式 | 提升倍数 |
|---------|----------|----------------|-----------|
| 创建带链接的文档 | 5-10 分钟 | 10 秒 | **30x-60x** |
| 创建 Base 数据库 | 10-20 分钟 | 15 秒 | **40x-80x** |
| 创建 Canvas 可视化 | 15-30 分钟 | 10 秒 | **90x-180x** |
| 查询和格式化数据 | 5-10 分钟 | 10 秒 | **30x-60x** |

---

## 🚀 快速开始检查表

### 环境检查

- [ ] Claude Code 已安装并可正常使用
- [ ] Obsidian App 已安装
- [ ] obsidian-skills 仓库已克隆或下载
- [ ] 知道技能文件的存放位置

### 配置检查

- [ ] Claude Code 可以访问技能文件
- [ ] Obsidian Vault 已创建
- [ ] 可以在 Obsidian 中看到 Claude Code 创建的文件

### 功能验证

- [ ] 测试创建 Markdown 文档（使用 obsidian-markdown）
- [ ] 测试创建 Base 数据库（使用 obsidian-bases）
- [ ] 测试创建 Canvas 可视化（使用 json-canvas）
- [ ] 在 Obsidian 中验证文件格式正确

---

## 📚 相关资源

### 官方资源

| 资源 | 链接 |
|------|------|
| **Claude Code** | https://claude.ai/code |
| **Obsidian 官网** | https://obsidian.md |
| **Obsidian 帮助文档** | https://help.obsidian.md |
| **obsidian-skills 仓库** | https://github.com/kepano/obsidian-skills |
| **JSON Canvas 规范** | https://jsoncanvas.org/ |

### 学习资源

| 资源 | 链接 |
|------|------|
| **Obsidian 社区论坛** | https://forum.obsidian.md |
| **Obsidian Discord** | https://discord.gg/obsidian |
| **YouTube 教程** | 搜索 "Obsidian tutorial" |

### 社区资源

| 资源 | 链接 |
|------|------|
| **Obsidian 中文社区** | https://pkmer.cn |
| **Obsidian 发布广场** | https://obsidian.md/publish |
| **Awesome Obsidian** | https://github.com/obsidianmd/awesome-obsidian |

---

## 🎉 开始享受高效创作！

### 核心优势

通过这套工作范式，你可以获得：

1. ✅ **零学习曲线** - 不需要学习 Obsidian 复杂语法
2. ✅ **30 倍效率提升** - 对话式创作比手动操作快得多
3. ✅ **100% 格式准确** - Claude Code 自动处理所有技术细节
4. ✅ **保留 Obsidian 价值** - 仍然使用 Obsidian 的查看、搜索、图谱功能

### 下一步行动

```
1. 立即体验：创建你的第一个文档
2. 探索功能：尝试不同的查询和可视化
3. 建立习惯：在日常工作中使用这个工作流
4. 分享经验：把这个范式分享给更多朋友
```

---

**文档版本**: v1.0.0（通用分享版）
**更新日期**: 2026-02-11
**许可证**: CC BY 4.0（可自由分享和修改）

**祝你高效创作，愉快使用！**
