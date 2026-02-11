---
name: skill-dashboard-generator
description: Generate and maintain a visual dashboard for all Claude Code skills. Automatically scans skill directories, extracts metadata, and creates Obsidian-compatible status documents with wikilinks. Use when users want to see all their installed skills, check for updates, or organize their skill library.
version: 1.0.0
created_at: 2026-02-11
license: MIT
---

# Skill Dashboard Generator

> **版本**: 1.0.0
> **目的**: 为 Claude Code 技能生成可视化仪表盘，自动扫描和索引所有技能
> **说明**: 支持多种输出格式（Markdown、Canvas），包含完整生成脚本
> **更新**: 2026-02-11

---

## 🎯 功能概述

这个技能帮助 Claude Code 自动生成和维护技能状态仪表盘：

1. **自动扫描** - 扫描所有技能位置的 SKILL.md 文件
2. **提取元数据** - 读取技能名称、描述、版本
3. **生成仪表盘** - 创建 Obsidian 兼容的状态文档
4. **设置符号链接** - 在 Vault 中创建指向技能目录的链接
5. **分类组织** - 按功能分组（开发工具、工作流等）
6. **调用追踪** - 记录本次对话使用的技能
7. **更新检查** - 检查技能是否有新版本

---

## 📁 使用方式

### 调用方式

用户说以下任一内容时触发：

- "生成技能仪表盘"
- "扫描所有技能"
- "更新技能状态"
- "管理技能"
- "技能统计"

### 输出格式

支持多种输出格式：

| 格式 | 说明 | 使用方式 |
|------|------|------|----------|
| **Markdown (完整版)** | 包含所有技能的详细列表，可直接搜索和跳转 | 默认 |
| **Markdown (优化版)** | 使用 Callout、折叠块、emoji 图标（需手动启用） | \`--format markdown-optimized\` |
| **Canvas 可视化** | JSON Canvas 格式，节点式展示，可拖拽整理（需要 Canvas 插件） | \`--format canvas\` |

---

## 🔧 扫描和生成

### 扫描位置

\`\`\`bash
SCAN_DIRS=(
  "$HOME/.claude/skills"           # 全局技能
  "$HOME/.claude/plugins"          # Claude Code 插件
)
\`\`\`

### 扫描命令

\`\`\`bash
# 扫描所有技能文件
find "$HOME/.claude/skills" -maxdepth 2 -name "SKILL.md" -type f
\`\`\`

---

## 📊 仪表盘模板

### Markdown 完整版模板

包含所有 54 个技能的详细列表，按 6 大类分组：

1. 🛠️ 开发工具
2. 🔄 工作流
3. 🔍 代码质量
4. 📄 文档演示
5. 🎨 设计
6. ⚙️ 技能管理

---

## 💡 使用说明

### 在 Obsidian 中

1. **搜索** - 输入 /技能名 快速定位
2. **跳转** - 点击 [[skill/SKILL]] 直接打开
3. **分类** - 按 6 大类组织，便于查找

### 确保符号链接

在 Vault 中创建符号链接：

\`\`\`bash
ln -s ~/.claude/skills "{VAULT}/99-全局技能"
\`\`\`

---

## 🚨 实现注意事项

1. **数字验证** - 禁止虚假或预设数字，必须来自实际扫描
2. **链接有效性** - 使用标准 wikilink 格式
3. **完整扫描** - 不要只列出部分技能

---

## 📦 开源准备

本技能可以独立开源，提供完整的技能可视化管理方案。

**许可**: MIT

---

**技能版本**: 1.0.0
**最后更新**: 2026-02-11
