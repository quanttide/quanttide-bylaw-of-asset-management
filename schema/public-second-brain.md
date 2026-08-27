# 量潮公开第二大脑资产章程

## 第一章 总则

**第一条** 量潮公开第二大脑以 GitHub 组织 `quanttide` 的根仓库 `quanttide/quanttide` 为入口。GitHub 公开仓库是其资产的主要形态：20 类标准资产（18 类九宫格资产 + Context、Archive 两类不占格资产）均以公开仓库为载体，由根仓库统一组织。

**第二条** 本章程规定量潮公开第二大脑资产的定义与维护规范，包括各仓库的命名、组织结构与挂载路径，为仓库创建与维护提供依据。

**第三条** 本章程适用于以 `quanttide/quanttide` 为入口的公开第二大脑体系下的全部公开仓库，新增仓库须按本章程命名与组织。

## 第二章 双轴组织

**第四条** 量潮第二大脑通过**领域轴**与**资产轴**双轴组织：

- 领域轴：每个领域对应一个领域仓库 `quanttide-{领域短名}`（如 quanttide-crowd、quanttide-learn），是领域第二大脑的统一载体
- 资产轴：20 类标准资产（18 类九宫格资产 + Context、Archive 两类不占格资产），每类资产按领域落地为资产子仓库
- 双轴交点：`quanttide-{资产类型}-of-{领域英文名}`（领域仓库内按资产类型挂载的资产子仓库）
- 聚合容器：`quanttide-{资产类型}` 按领域聚合各资产子仓库（如 quanttide-journal 聚合各领域日志）

**第五条** 法人主体资产位于主体轴与资产轴交点：`quanttide-{资产类型}-of-business-entity`。

## 第三章 仓库命名

**第六条** 领域仓库：`quanttide-{领域短名}`，如 `quanttide-agent`、`quanttide-crowd`、`quanttide-learn`。

**第七条** 资产子仓库通用命名：`quanttide-{资产类型}-of-{领域英文名}`，如 `quanttide-journal-of-crowd-sourcing`、`quanttide-bylaw-of-document-engineering`。

20 类标准资产的仓库命名如下：

**程序型记忆九宫格（9 类）：**

| 资产类型 | 仓库命名 | 示例 |
|:----|:----|:----|
| Bylaw 工作章程 | `quanttide-bylaw-of-{领域英文名}` | quanttide-bylaw-of-document-engineering |
| Specification 工程标准 | `quanttide-specification-of-{领域英文名}` | quanttide-specification-of-course-development |
| Toolkit 工具箱 | `quanttide-{领域}-toolkit` | quanttide-crowd-toolkit |
| Handbook 工作手册 | `quanttide-handbook-of-{领域英文名}` | quanttide-handbook-of-software-engineering |
| Gallery 工作案例 | `quanttide-gallery-of-{领域英文名}` | quanttide-gallery-of-course-development |
| Platform 平台 | `qt{产品名}`（产品平台）或 `qtcloud-{产品名}`（云平台） | qtcrowd、qtclass；qtcloud-learn、qtcloud-course |
| Tutorial 工作教程 | `quanttide-tutorial-of-{领域英文名}` | quanttide-tutorial-of-course-development |
| Essay 工作札记 | `quanttide-essay-of-{领域英文名}` | quanttide-essay-of-course-development |
| Example 示例程序 | `quanttide-laboratory-of-{领域英文名}` | quanttide-laboratory-of-crowdsourcing-management |

**陈述型记忆九宫格（9 类）：**

| 资产类型 | 仓库命名 | 示例 |
|:----|:----|:----|
| Report 工作报告 | `quanttide-report-of-{领域英文名}` | quanttide-report-of-software-engineering |
| Library 工作参考 | `quanttide-library-of-{领域英文名}` | quanttide-library-of-philosophy |
| History 工作历史 | `quanttide-history-of-{领域英文名}` | quanttide-history-of-devops |
| Journal 工作日志 | `quanttide-journal-of-{领域英文名}` | quanttide-journal-of-crowd-sourcing |
| Profile 工作档案 | `quanttide-profile-of-{领域英文名}` | quanttide-profile-of-course-development |
| Brochure 宣传册 | `quanttide-brochure-of-{领域英文名}` | quanttide-brochure-of-course-development |
| Roadmap 路线图 | `quanttide-roadmap-of-{领域英文名}` | quanttide-roadmap-of-learning-management |
| Insight 工作洞察 | `quanttide-insight-of-{领域英文名}` | quanttide-insight-of-product-development |
| Intention 工作意图 | `quanttide-intention-of-{领域英文名}` | quanttide-intention-of-crowd-sourcing |

**不占格资产（2 类）：**

| 资产类型 | 仓库命名 | 示例 |
|:----|:----|:----|
| Context 工作语境 | `quanttide-context-of-{领域英文名}` | quanttide-context-of-agent-engineering |
| Archive 工作归档 | `quanttide-archive-of-{领域英文名}` | — |

**第八条** 聚合容器：`quanttide-{资产类型}`，如 `quanttide-journal`、`quanttide-profile`、`quanttide-roadmap`、`quanttide-bylaw`。

**第九条** 法人主体资产：`quanttide-{资产类型}-of-business-entity`，如 `quanttide-profile-of-business-entity`。

## 第四章 组织结构

**第十条** 领域仓库（领域轴与资产轴交点的载体）内部按统一结构组织：

```
quanttide-{领域短名}/
├── apps/          # Platform 平台资产（qt{产品名} / qtcloud-{产品名}）
├── packages/      # Toolkit 工具箱资产（quanttide-{领域}-toolkit）
├── examples/      # Example 示例资产（quanttide-laboratory-of-{领域英文名}）
├── data/          # 陈述型记忆与不占格资产
│   ├── context/ journal/ profile/ roadmap/ insight/ intention/
│   └── report/ library/ history/ brochure/ archive/
└── docs/          # 程序型记忆资产
    ├── bylaw/ specification/ handbook/ gallery/ tutorial/ essay/
```

**第十一条** 资产聚合容器（资产轴聚合层）：`quanttide-{资产类型}` 容器按 `default/`（法人主体）与 `domains/`（领域）聚合对应资产子仓库，如 `quanttide-journal` 下挂 `default/company` 与 `domains/{agent, data, crowd, ...}`。

## 第五章 附则

**第十二条** 本章程由资产治理团队维护和修订。
