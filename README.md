# 破局学习系统（FDE）

以破局 CLI 为主要知识入口，持续收集、筛选、蒸馏和课程化 FDE 相关资料，帮助学习者从岗位认知走到可验证的业务交付练习。

> 当前版本：v0.1（第一阶段基座）

## 这是什么

本项目是一个可安装、可更新的 FDE 学习 Skill 和课程资料库。它把四件事接起来：

```text
破局 CLI 信息入口
  → 资料初筛与精筛
  → FDE 知识基座与课程
  → 讲解、练习、验收和项目实训
```

当前优先建设“破局学习系统（FDE）”本身；通用跨专业学习 Skill 只作为后续规划，不属于当前第一阶段承诺。

## 快速开始

### 方式一：克隆仓库

```powershell
git clone https://github.com/oopsdoes/poju-fde-learning-system.git
cd poju-fde-learning-system
```

### 方式二：下载发布包（后续提供）

当前 v0.1 先提供 GitHub 仓库克隆方式。后续发布 `.skill` 或 ZIP 包时，下载后将包含 `SKILL.md` 的目录放入你的 Agent 可发现的 Skills 目录。不同 Agent 的安装目录不同，请以其文档为准。

## 1. 安装破局 CLI

破局 CLI 是本系统的主要动态知识入口。

前置：Node.js（建议使用当前 LTS）。

```powershell
npm install -g @aipoju/breakout-cli
breakout version
breakout auth login
breakout auth status
breakout doctor
```

`auth login` 需要你在浏览器完成设备授权。不要把登录凭据、导出的诊断包或个人配置提交到仓库。

版本变化时，以 `breakout --help` 和 CLI 当前输出为准。查询结果可能受分页、同步延迟和账号权限影响。

没有安装或登录破局 CLI 时，仍可使用仓库中的课程骨架、公开资料索引和用户自己提供的 FDE 材料；只是不能执行破局动态检索。

## 2. 加入课程与 Knowledge 文件

仓库根目录的 `SKILL.md` 是公开 Skill 入口，`course/` 是公开课程内容，`sources/` 是来源登记和资料处理规则。

“Knowledge”层在本项目中表现为公开的知识地图、课程架构、资料筛选规则、课件模板和项目模板；使用者不需要额外获得私有 Knowledge 文件才能使用本 Skill。

本项目的课程方法采用结构化学习、知识地图、分块讲解、提问测试、练习验收和复盘更新等流程。它们已经编排为 FDE 学习系统自身的公开流程；本仓库不要求使用者获得任何私人方法文件。

推荐阅读顺序：

1. `course/FDE课程总览.md`
2. `course/FDE知识地图.md`
3. `course/01-FDE认知与岗位边界.md`
4. `course/02-FDE技术基础.md`
5. 根据个人目标选择项目实训模板。

## 3. 资料补充、筛选与入库

资料来源不限于破局，但统一走同一条入口：

```text
资料登记
  → 初筛（相关性、重复、可用性）
  → 精筛（事实、观点、案例、方法、反例）
  → 来源与状态标注
  → 蒸馏
  → 映射到知识地图
  → 判断是否更新课程、练习或验收标准
```

可接入的资料包括：

- 破局 CLI 主题和主题详情；
- FDE Guidance Book 及其公开章节；
- 公开学习仓库、文章、报告和案例；
- 用户获得的公开视频转写稿；
- 本地文字资料；
- 开源项目和真实练手项目资料。

资料处理规则见 [`sources/source-policy.md`](sources/source-policy.md)、[`sources/ingest-workflow.md`](sources/ingest-workflow.md) 和 [`sources/learning-dialogue-workflow.md`](sources/learning-dialogue-workflow.md)。
当前已登记的基础来源见 [`sources/source-registry.md`](sources/source-registry.md)。

## 4. 其他 Skill 与工具

| 名称 | 来源 | 在本项目中的作用 | 是否硬依赖 |
|---|---|---|---|
| `book-to-skill` | [virgiliojr94/book-to-skill](https://github.com/virgiliojr94/book-to-skill) | 从书籍、长文和文档提取框架、原则、方法和反模式 | 否 |
| `cangjie-skill` | [kangarooking/cangjie-skill](https://github.com/kangarooking/cangjie-skill) | 从书、课程、视频转写和访谈蒸馏可执行方法单元 | 否 |
| `poju-aiclub` | [`cleanbinggmail/poju-aiclub`](https://github.com/cleanbinggmail/poju-aiclub) | 破局 CLI 的命令编排、返回结构和实测陷阱参考 | 推荐；没有时可手动使用 CLI |
| `learning-notes-automation` | Agent 本地可选 Skill | 将视频转写转成学习笔记、闪卡和复习材料 | 否 |
| `markitdown-converter` | Agent 本地可选 Skill | 将 PDF、Word、Excel 等转成 Markdown 以便筛选 | 否 |

安装示例（请以原仓库当前说明为准）：

```powershell
git clone https://github.com/virgiliojr94/book-to-skill.git
git clone https://github.com/kangarooking/cangjie-skill.git
```

本项目默认提供来源与安装说明，不假定必须复制它们的完整文件。

## 5. 学习与实训流程

```text
明确学习目标
  → 建立知识地图
  → 找出知识缺口
  → 排学习顺序
  → 分块学习
  → 提问与自测
  → 练习和作业
  → 验收
  → 项目实训
  → 复盘与课程更新
```

练手项目不固定。当前可以使用招投标信息工作流，也可以替换为开源项目规划、企业知识库、销售流程或其他可验证的 AI 交付场景。项目必须写清用户、问题、输入、输出、人工确认、风险、验收和不做事项。

## 6. 安全边界

本项目用于学习和受控的 AI 工作流练习，不替代企业授权人员、法务、商务或项目负责人的最终判断。任何项目都不得默认自动完成资格判定、报价、盖章或提交；涉及这些环节时必须保留人工确认和合规审核。

## 7. 更新机制

破局每日新增内容不会直接覆盖课程正文。新增资料先进入资料登记，再经过筛选、去重、蒸馏和课程映射。只有在它改变能力要求、学习顺序、练习或验收标准时，才更新课程核心；普通案例作为资料增量保存。

资料入库状态与学习状态分开记录，因此 DSH 视频转写可以与正式学习并行；新增视频只会补充证据、对照复习或形成新的小练习，不会因为“已转写”就重复安排已经验收过的知识。

视频转写完成后，公开仓库只放可公开的索引、来源、摘要和已验证学习卡片；完整转写和中间文件留在本地工作区。

## 8. 目录

```text
SKILL.md     公开可安装的 Skill 入口
course/      课程总览、知识地图和课程正文
sources/     来源登记、筛选、蒸馏和更新规则
templates/   课程与项目模板
```

## 许可证

本项目自有代码、模板和文档采用 MIT License，详见 [`LICENSE`](LICENSE)。外部资料和外部 Skill 依其原始许可与使用规则。
