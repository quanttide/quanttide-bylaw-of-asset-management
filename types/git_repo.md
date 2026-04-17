# Git仓库

Git仓库指的是项目代码托管的版本控制仓库。

## 保留文件

保留文件指的是具有特定业务意义的文件。

标准保留文件包括：
- `README.md`: 项目概述、目录结构、快速开始
- `CONTRIBUTING.md`: 贡献指南、工作流、环境变量
- `AGENTS.md`: Agent导航、AI元认知
- `CHANGELOG.md`: 版本历史记录，遵循 [Keep a Changelog](https://keepachangelog.com/) 规范
- `ROADMAP.md`: 项目路线图、未来规划

## 保留目录

保留目录指的是具有特定业务意义的目录。

标准保留目录包括：
- `.agents/`: 智能体配置目录
- `.quanttide/`: 量潮配置目录

### 智能体配置

- `skills/`: 技能目录。每个技能装在一个次级目录里，即`.agents/skills/<skill-name>`。次级目录固定包括一个`SKILL.md`和AgentSkills规范定义的其他文件。

### 量潮配置

- `asset/`: 数字资产。包括`contract.yaml`数字资产契约等。
- `code/`: 氛围编程。包括`contract.yaml`氛围编程契约等。
- `docs/`: 文档工程。包括`contract.yaml`文档工程契约等。
