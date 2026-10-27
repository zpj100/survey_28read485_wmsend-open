# survey_28read485_wmsend-open

`survey_28read485_wmsend` 的**版本检查公开仓库**。

本仓库**只放版本清单**，不含任何源码、配置、口令或采集数据。
客户端程序 `survey_28read485_wmsend` 的「检查更新」功能读取
[`survey_28read485_wmsend.json`](survey_28read485_wmsend.json)，与本地版本号比较后提示是否有新版本。

## 文件

| 文件 | 说明 |
|---|---|
| `survey_28read485_wmsend.json` | 版本清单：`version` / `date` / `notes` / `channel` / `platform` / `updated_at` |

程序按以下顺序尝试读取清单，取版本号最高者：

```
https://gitee.com/zpj100/survey_28read485_wmsend-open/raw/master/survey_28read485_wmsend.json
https://raw.giteeusercontent.com/zpj100/survey_28read485_wmsend-open/raw/master/survey_28read485_wmsend.json
https://fastly.jsdelivr.net/gh/zpj100/survey_28read485_wmsend-open@master/survey_28read485_wmsend.json
https://cdn.jsdelivr.net/gh/zpj100/survey_28read485_wmsend-open@master/survey_28read485_wmsend.json
https://gitee.com/api/v5/repos/zpj100/survey_28read485_wmsend-open/releases/latest
https://raw.githubusercontent.com/zpj100/survey_28read485_wmsend-open/master/survey_28read485_wmsend.json
https://api.github.com/repos/zpj100/survey_28read485_wmsend-open/releases/latest
```

## 发版流程

1. 私有仓库打 tag（`v1.3.0`）并上传打包产物 `survey_28read485_wmsend_V1.3.0.zip` 到 Releases；
2. 改本仓库 `survey_28read485_wmsend.json` 的 `version`、`date`、`notes`、`updated_at`；
3. 推送 `master`（jsdelivr 有缓存，`@master` 的 CDN 链接可能延迟数十分钟，Gitee/raw 链接即时生效）。

`version` 支持 `1.3.0`、`v1.3.0`、`survey_28read485_wmsend-1.3.0` 三种写法，程序会自动剥掉前缀再比较。

## 版本历史

| 版本 | 日期 | 摘要 |
|---|---|---|
| 1.3.0 | 2026-10-27 | 秒级零值修复（保持最近有效值）、原始报文单文件日志、项目更名 |
| 1.2.0 | 2026-10-27 | 按 ID 多路解析（提速约 19 倍）、超量程不再静默写 0、帧长自适应 |
| 1.1.0 | 2026-10-13 | 初始版本 |
