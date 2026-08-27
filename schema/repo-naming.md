# 量潮GitHub仓库命名规范

## 第一章 总则

**第一条** 本规范规定量潮 GitHub 组织下各仓库的命名规则，与《量潮第二大脑资产图式章程》（schema/second-brain.md）配套，属于资产治理的务实层约定。

## 第二章 命名规则

**第二条** 领域仓库命名：`quanttide-{领域短名}`，如 `quanttide-agent`、`quanttide-crowd`、`quanttide-learn`。

**第三条** 资产子仓库命名：`quanttide-{资产类型}-of-{领域英文名}`，如 `quanttide-journal-of-crowd-sourcing`、`quanttide-bylaw-of-document-engineering`。

**第四条** 法人主体资产命名：`quanttide-{资产类型}-of-business-entity`，如 `quanttide-profile-of-business-entity`。

**第五条** 聚合容器命名：`quanttide-{资产类型}`，如 `quanttide-journal`、`quanttide-profile`、`quanttide-roadmap`、`quanttide-bylaw`。

**第六条** 应用命名：`qt{产品名}` 或 `qtcloud-{产品名}`，如 `qtcrowd`、`qtclass`、`qtcloud-learn`。

**第七条** 工具集命名：`quanttide-{领域}-toolkit`，如 `quanttide-crowd-toolkit`。

**第八条** 实验室命名：`quanttide-laboratory-of-{领域英文名}`，如 `quanttide-laboratory-of-crowdsourcing-management`。

## 第三章 挂载路径

**第九条** 领域仓库内挂载路径：`apps/` 挂应用，`packages/` 挂工具集，`examples/default` 挂实验室，`data/` 与 `docs/` 按资产类型挂载对应子仓库。

## 第四章 附则

**第十条** 本规范由资产治理团队维护和修订。
