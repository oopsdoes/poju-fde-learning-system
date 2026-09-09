# 外部 Skill 来源与使用说明

本文件只登记公开来源和本项目中的职责，不内嵌私人研发方法文件。

## book-to-skill

- 来源：[virgiliojr94/book-to-skill](https://github.com/virgiliojr94/book-to-skill)。
- 作用：从书籍、长文、PDF、网页等资料提取框架、原则、技术、反模式和术语。
- 在本项目中的用法：处理 FDE Guidance Book 和长篇 FDE 资料，输出候选知识单元，再由课程流程筛选和验证。
- 依赖：可选。没有它时，可人工或用其他工具完成资料提炼。
- 版本与许可证：以原始仓库当前声明为准。

## cangjie-skill

- 来源：[kangarooking/cangjie-skill](https://github.com/kangarooking/cangjie-skill)。
- 作用：把书、课程、视频转写、播客和访谈中的方法论蒸馏成可执行方法单元。
- 在本项目中的用法：处理后续视频转写和复杂课程资料，生成方法、案例、反例和待核对项。
- 依赖：可选。没有它时，可按 `sources/ingest-workflow.md` 手动提炼。
- 版本与许可证：以原始仓库当前声明为准。

## poju-aiclub

- 来源：[cleanbinggmail/poju-aiclub](https://github.com/cleanbinggmail/poju-aiclub)。
- 作用：提供破局 CLI 的命令编排、返回结构、错误陷阱和实测参考。
- 在本项目中的用法：作为破局 CLI 的主要信息入口和使用参考，不替代资料筛选与课程验收。
- 依赖：推荐但非硬依赖；没有时仍可手动安装 `@aipoju/breakout-cli`。

## knowledge 方法层

本公开项目只发布已经编排完成的 FDE 学习流程，不内嵌私人 Knowledge Skill、私人蒸馏文件或内部提示词。使用者直接使用本项目公开的课程、资料和验收流程即可。
