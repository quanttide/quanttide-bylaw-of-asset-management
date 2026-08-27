# CHANGELOG

## [Unreleased]

### Changed
- 重写 schema/second-brain.md：定位由务虚改为务实，标题改为《量潮第二大脑资产章程》，新增第六章仓库命名规则（领域/资产/主体/聚合容器/应用/工具集/实验室命名与挂载路径）
- 进一步收敛 schema/second-brain.md：明确 GitHub 公开仓库为主要资产形态，只保留命名规范，资产图式概念不再重复（见 meta 章程）
- 挂载路径修正：实验室挂载路径由 `examples/default` 改为 `examples/`
- 升级组织结构：挂载路径升级为双轴组织（领域轴 × 资产轴），命名规则穷举 20 类标准资产仓库，Platform 区分 `qt{}`（产品平台）与 `qtcloud-{}`（云平台）
- 重写总则：自包含定位，不再引用其他章程
- 文件更名为 `schema/public-second-brain.md`，标题改为《量潮公开第二大脑资产章程》：强调以 `quanttide/quanttide` 仓库为入口的第二大脑资产定义与维护规范
- 条款重排：第三条并入总则第一二条，聚合容器并入第五条（领域第二大脑/资产第二大脑），法人主体并入第六条；「不占格资产」改名为「默认资产」；以「领域第二大脑」「资产第二大脑」替代模糊概念
- 默认资产表补充 Archive 工作归档示例（quanttide-archive-of-business-entity）
- 第四条补充法人主体作为默认领域（business-entity 为默认领域，主体资产命名统一归入 `-of-{领域英文名}` 规则）

### Fixed
- index.md：修正 schema/second-brain.md 失效链接（原引用中文文件名）

## [v0.2.0] - 2025-04-21

### Added
- 添加第二大脑资产类别定义
- 添加工作章程功能定义（宗旨、原则、成员、修订流程）
- 添加资产名称定义：repo、tenant
- 添加资产类型定义：git_repo

### Changed
- 重新梳理章程和案例边界，章程聚焦治理纲领

### Removed
- 移除部分冗余文档结构