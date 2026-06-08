# Paper Reports Static Package

本包为本地静态站点，包含 10 篇自动驾驶 VLA/LLM/WM 论文报告与 `records.json`。

## 已生成
- `index.html`: 首页，新论文顺序已按本次列表排在最前。
- `report/<stable-id>/index.html`: 每篇论文深度中文 Blog。
- `report/<stable-id>/figures/*`: 论文 PDF 或官方项目页抽取的真实图像。
- `records.json`: 按飞书多维表字段生成的记录。
- `.nojekyll`: GitHub Pages 需要。

## 未执行
- GitHub Pages 发布与 main 分支 push。
- 飞书 PDF 上传。
- 飞书多维表同步。

## 交给 Codex/本地后端执行
1. 将本包解压到 `paper-reports` 仓库根目录。
2. 确认环境变量中存在 `GITHUB_TOKEN`、`FEISHU_APP_ID`、`FEISHU_APP_SECRET`。
3. commit + push 到 main。
4. 使用 `records.json` 写入已有飞书表格：app_token=M114bQyfXa4ixLsZUHWcpb36nqf, table_id=tblsRBwpkiRQzRcr。
5. 上传每篇原始 PDF 到“论文文件”字段；OpenDriveVLA 当前提供 PDF URL source txt，后端可从 AAAI URL 下载后上传。

计划公网首页：https://ixgnozeix.github.io/paper-reports/
