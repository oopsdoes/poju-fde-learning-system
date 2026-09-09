# 破局 CLI 在 FDE 学习系统中的使用

## 前置检查

```powershell
breakout auth status --json
breakout doctor
```

## 查询原则

- FDE 关键词：`FDE`、`前线部署工程师`、`驻场交付工程师`、`Field Deployment Engineer`；
- 先列表/搜索，再读取详情；
- 使用返回的 `topicId` 和 `websiteUrl`，不猜 URL；
- 增量更新按 URL 或 topicId 去重；
- 记录查询日期、分页、筛选条件和失败原因。

## 证据边界

CLI 搜索结果是资料入口，不是自动课程结论。主题详情仍需筛选、深读和来源标注。同步延迟、分页差异和账号权限可能影响结果。

## 参考

详细命令和实测陷阱见公开项目 [`poju-aiclub`](https://github.com/cleanbinggmail/poju-aiclub) 的 `references/commands.md`、`references/pitfalls.md` 和 `docs/TEST-REPORT.md`。
