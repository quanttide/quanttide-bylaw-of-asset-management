# 量潮公开平台资产契约章程

## 第一章 总则

**第一条** 量潮公开平台资产是量潮产品与服务的基础设施载体，分为 Git 仓库与 S3 存储桶两大类。本章程规定公开平台资产的定义、分类、生命周期与维护规范。

**第二条** 公开平台资产必须遵循"分类明确、生命周期清晰、上架可控"的原则，禁止资产长期停留在未分类状态（如 `others` 分类）。

## 第二章 资产分类

**第三条** 公开平台资产按业务归属分类，每个资产必须属于明确的业务线：

| 业务线 | 前缀 | 示例 |
|:----|:----|:----|
| 量潮课堂 | `qtclass-` | `qtclass-video`、`qtclass-private` |
| 量潮众包 | `qtcrowd-` | `qtcrowd-data`、`qtcrowd-static` |
| 量潮云平台 | `qtcloud-` | `qtcloud-api`、`qtcloud-cdn` |

**第四条** 资产分类决定其访问权限与存储位置：
- **私有资产**（`*-private`）：仅内部访问，用于开发、测试、暂存
- **公有资产**（无 `-private` 后缀）：对外提供服务，用于生产环境

## 第三章 Git 仓库规范

**第五条** Git 仓库用于存放代码、配置、文档等版本化资产，包括：
- 应用代码仓库（Provider、Studio、CLI、SDK）
- 配置仓库（环境变量、部署配置）
- 文档仓库（用户文档、开发者文档）

**第六条** Git 仓库命名必须遵循 `{业务线前缀}-{组件类型}` 格式：

| 组件类型 | 命名模式 | 示例 |
|:----|:----|:----|
| Provider 服务端 | `{业务线}-provider` | `qtclass-provider` |
| Studio 工作台 | `{业务线}-studio` | `qtclass-studio` |
| CLI 命令行 | `{业务线}-cli` | `qtclass-cli` |
| SDK 开发包 | `{业务线}-{lang}-sdk` | `qtclass-python-sdk` |

**第七条** Git 仓库管理规则：
- 所有仓库必须启用分支保护，main 分支禁止直接推送
- 必须使用 Pull Request 进行代码审查
- 提交信息必须遵循约定式提交规范（Conventional Commits）

## 第四章 S3 存储桶规范

**第八条** S3 存储桶用于存放静态资源、部署产物、用户数据等非版本化资产，包括：
- **Site 站点**：前端部署产物（HTML/CSS/JS）
- **Studio 工作台**：GUI 客户端资源
- **Provider 服务端**：API 静态资源、上传文件
- **Private 私有数据**：未上架的业务数据、备份

**第九条** S3 存储桶命名必须遵循 `{业务线前缀}-{用途}` 格式：

| 用途 | 命名模式 | 示例 |
|:----|:----|:----|
| Site 站点 | `{业务线}-site` | `qtclass-site` |
| Studio 工作台 | `{业务线}-studio-static` | `qtclass-studio-static` |
| Provider 静态资源 | `{业务线}-provider-static` | `qtclass-provider-static` |
| Private 私有数据 | `{业务线}-private` | `qtclass-private` |
| 公开视频 | `{业务线}-video` | `qtclass-video` |
| 静态资源 | `{业务线}-static` | `qtcrowd-static` |
| 备份归档 | `{业务线}-archive` | `qtcloud-archive` |

**第十条** S3 存储桶分类规则：
- 私有存储桶（`*-private`）用于存放未上架的业务数据
- 公开存储桶用于存放已上架的正式数据
- 禁止将业务数据直接放入公开存储桶，必须先经过私有存储桶暂存

**第十一条** S3 存储桶上架规则：
- Site 存储桶必须配置 CDN 加速和 HTTPS
- 所有公开存储桶必须设置访问日志和监控告警
- 私有存储桶必须设置访问策略，禁止公开访问

## 第五章 附则

**第十二条** 本章程由资产治理团队维护和修订。

**第十三条** 本章程自发布之日起生效，适用于所有新建和存量公开平台资产。