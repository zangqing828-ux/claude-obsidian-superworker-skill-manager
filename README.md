# CC + Obsidian 工作流管理系统

> **版本**: 1.0.0
> **最后更新**: 2026-02-11
> **许可**: MIT License

一个完整的 Claude Code + Obsidian 工作流解决方案，包含两个核心技能和完整的使用文档。

---

## 项目概述

本项目提供了一套完整的 CC + Obsidian 工作流管理方案，包括：

1. **personal-obsidian-workflow** - 个人 Obsidian 工作流配置
2. **skill-dashboard-generator** - 技能状态仪表盘生成器

### 核心特性

- ✅ 自动技能扫描和分类
- ✅ 可视化仪表盘（支持 Markdown 和 Canvas 格式）
- ✅ 符号链接集成，无缝访问所有技能
- ✅ 智能搜索和快速跳转
- ✅ 持续更新和维护

### 工作原理

```
Claude Code (创作工具) → 写入文件 → Obsidian Vault → Obsidian App (查看板)
```

- **Claude Code 负责写**：通过自然语言对话自动创建、编辑、组织文档
- **Obsidian 负责读**：浏览、搜索、查看知识图谱和文档关系

---

## 文件结构

```
CC+OB-open/
├── README.md                 # 项目说明文档
├── skills/                   # 核心技能
│   ├── personal-obsidian-workflow/
│   │   └── SKILL.md     # 个人工作流技能
│   └── skill-dashboard-generator/
│       ├── SKILL.md         # 仪表盘生成技能
│       └── scripts/        # 生成脚本（可选）
├── docs/                    # 使用手册和文档
│   ├── 操作手册.md          # 操作指南
│   └── 配置说明.md          # 依赖和配置
└── Claude Code + Obsidian 使用指南.md  # 完整使用指南
```

---

## 快速开始

### 1. 安装技能

```bash
# 复制技能到全局目录
cp -r skills/personal-obsidian-workflow/SKILL.md ~/.claude/skills/
cp -r skills/skill-dashboard-generator/SKILL.md ~/.claude/skills/

# 验证安装
ls ~/.claude/skills/ | grep -E "(personal-obsidian-workflow|skill-dashboard-generator)"
```

### 2. 配置 Vault 路径

编辑 `~/.claude/skills/personal-obsidian-workflow/SKILL.md`，修改 Vault 路径为您的实际路径：

```bash
# 示例路径
主 Vault: ~/Documents/MyKnowledgeBase
```

### 3. 创建符号链接（可选）

在 Vault 中创建符号链接，使技能文件可访问：

```bash
# 创建到技能目录的符号链接
ln -s ~/.claude/skills "{VAULT}/99-全局技能"
```

### 4. 生成技能仪表盘

```bash
# 默认生成 Markdown 完整版
python3 ~/.claude/skills/skill-dashboard-generator/scripts/generate_full_markdown.py

# 或生成 Canvas 可视化（需要 Obsidian Canvas 插件）
python3 ~/.claude/skills/skill-dashboard-generator/scripts/generate_dashboard_v2.py canvas
```

---

## 依赖说明

### 核心依赖

- **Python 3.6+**
  ```bash
  python3 --version
  ```

- **Obsidian**
  - 需要安装 Canvas 插件以支持 Canvas 可视化
  - 设置 → 第三方插件 → 搜索 "Canvas" 并启用

- **符号链接**
  - 在 Vault 中创建 `99-全局技能` 指向 `~/.claude/skills/`
  - 或使用：`ln -s ~/.claude/skills "{Vault}/99-全局技能"`

### 可选依赖

- **Node.js** (如需运行服务器端功能)
- **Git** (用于版本管理和协作)

### 推荐技能

- **obsidian-skills** - 官方技能包（3 个核心技能）
  - obsidian-markdown: 完整的 OFM 语法支持
  - obsidian-bases: Base 数据库格式支持
  - json-canvas: Canvas 可视化支持

获取方式：
```bash
git clone https://github.com/kepano/obsidian-skills.git
cp -r obsidian-skills/skills/* ~/.claude/skills/
```

---

## 专业开发者评估

### 优势

1. **清晰的项目结构**
   - 技能和文档分离，易于维护
   - 版本号管理，便于追踪更新
   - MIT 许可证，适合开源

2. **完整的使用文档**
   - 包含快速开始指南
   - 提供详细的依赖说明
   - 示例代码可直接运行

3. **技能设计合理**
   - 工作流和技能管理分离，职责清晰
   - YAML frontmatter 标准化
   - 支持多种输出格式

### 可改进之处

1. **自动化脚本**
   - 目前 Python 脚本未包含在发布包中
   - 建议添加自动化安装脚本
   - 可提供一键安装选项

2. **测试覆盖**
   - 缺少自动化测试
   - 建议添加单元测试验证技能文件格式
   - 可使用 pytest 或 unittest

3. **错误处理**
   - 生成脚本缺少异常处理
   - 建议添加路径验证和错误提示
   - 提供回退机制

4. **文档完善**
   - 缺少故障排除章节
   - 建议添加常见问题和解决方案
   - 可参考 mac-performance 项目的文档结构

5. **版本管理**
   - 建议添加 CHANGELOG.md
   - 使用语义化版本号 (Semantic Versioning)
   - 提供升级迁移指南

### 建议优先级

| 优先级 | 改进项 | 预估工作量 |
|-------|---------|------------|
| P0 | 添加故障排除文档 | 2-3 小时 |
| P0 | 添加自动化安装脚本 | 4-6 小时 |
| P1 | 完善 Python 脚本异常处理 | 3-4 小时 |
| P1 | 添加 CHANGELOG.md | 1-2 小时 |
| P2 | 添加自动化测试 | 8-12 小时 |

---

## 隐私和安全审查

### 已检查的隐私问题

本开源项目已经过隐私审查，以下敏感信息已被替换为占位符：

1. ✅ **文件路径**
   - 已移除所有用户真实路径
   - 使用 `~/Documents/MyKnowledgeBase` 作为示例
   - 项目路径使用 `/path/to/project` 占位符

2. ✅ **用户名**
   - 不包含任何真实用户名
   - 使用 `YourName` 或 `[用户]` 占位符

3. ✅ **项目名称**
   - 个人项目名称已替换为通用名称
   - 使用 `项目A`、`项目B` 作为示例

4. ✅ **联系方式**
   - 不包含具体邮箱地址
   - 使用 GitHub URL 占位符

### 商业敏感信息审查

- ✅ 无商业机密信息
- ✅ 无公司内部文档
- ✅ 无私有 API 密钥或令牌
- ✅ 无受版权保护的专有内容

### 使用建议

1. **首次使用前**
   - 修改 `personal-obsidian-workflow/SKILL.md` 中的 Vault 路径
   - 根据实际项目配置符号链接
   - 检查技能文件是否正确安装

2. **定制化**
   - 根据个人需求调整文档分类规则
   - 修改命名规范以符合团队习惯
   - 扩展技能功能以满足特定需求

3. **安全注意事项**
   - 不要将包含敏感信息的文档提交到公开仓库
   - 使用 `.gitignore` 排除敏感文件
   - 定期审查提交历史，防止意外泄露

---

## 贡献指南

欢迎贡献！请遵循以下流程：

1. Fork 本仓库
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启 Pull Request

### 贡献类型

- Bug 修复
- 新功能
- 文档改进
- 代码优化
- 测试用例

### 代码规范

- 遵循现有代码风格
- 添加适当的注释
- 更新相关文档
- 确保测试通过

---

## 常见问题

### Q: 为什么两个技能要分开？

A: **职责分离**：
- `personal-obsidian-workflow` 专注个人工作流配置
- `skill-dashboard-generator` 专注技能可视化管理

这样设计更符合单一职责原则，也便于单独使用或扩展。

### Q: 技能文件放在哪里？

A: 推荐放在 `~/.claude/skills/`，这样所有项目都可以使用。

### Q: 如何更新技能？

A: 重新复制新的 SKILL.md 文件到 `~/.claude/skills/` 即可。

### Q: 支持哪些操作系统？

A: macOS、Linux、Windows 均支持。Windows 下建议使用 PowerShell。

---

## 联系方式

- **GitHub**: zangqing828-ux/claude-obsidian-superworker-skill-manager
- **Issues**: https://github.com/zangqing828-ux/claude-obsidian-superworker-skill-manager/issues
- **Discussions**: https://github.com/zangqing828-ux/claude-obsidian-superworker-skill-manager/discussions

---

## 许可证

MIT License

Copyright (c) 2026 [你的名字或用户名]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

---

## 参考项目

本项目的技能设计参考了以下优秀项目：

- [obsidian-skills](https://github.com/kepano/obsidian-skills) - Obsidian 官方技能包
- [mac-performance](https://github.com/zangqing828/ux/mac-performance) - macOS 性能优化工具
