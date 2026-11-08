<p align="center"><img src="favicon.svg" width="64" height="64" alt=""></p>
<h1 align="center">温习有序 · Study Compass</h1>
<p align="center">把学习目标拆成每天能执行的任务。</p>
<p align="center">
  <a href="https://study-plan-pv0.pages.dev/"><strong>在线使用</strong></a>
  ·
  <a href="https://yangchunkitandy-a11y.github.io/study-plan/">GitHub Pages</a>
</p>

Study Compass 是一款面向学生的网页学习工具，适合日常复习、作业安排和考前冲刺。打开浏览器即可开始，支持简体中文和 English。

## 第一次使用

1. 在 **我的计划** 选择科目、填写学习目标，并设置每周可用时间和固定安排。初次打开会显示一份示例计划，可以按自己的情况调整。
2. 把要学的章节和练习加入 **我的学习清单**，填写预计用时和截止日期，预览后保存。
3. 在 **今日计划** 选择日期，查看或添加当天任务。可以手动排程，也可以让系统利用空闲时段补排任务。

## 学习工具

| 功能 | 用途 |
| --- | --- |
| 考前倒排 | 根据各科考期、剩余任务和可用时间估算进度，查看哪些内容可能来不及完成。 |
| 沉浸自习室 | 选择任务或自由自习，切换桌景并调节雨声和氛围音。计时支持 1–300 分钟，提前结束按实际用时记录。 |
| 资料库 | 将 PDF 和图片按科目整理，关联到任务。PDF 可指定页码和题号，阅读时可接续上次位置。 |
| 错题与主动回忆 | 保存题目和解析照片，按间隔复习。记录重做结果，回看反复出错的题目。 |
| 学习统计 | 查看专注时长、完成量和正确率，按日期或科目筛选，并导出 CSV 汇总。 |

## 账号与数据

- **访客模式**可直接使用，学习记录和上传的资料保存在当前浏览器。
- **登录后**可跨设备同步计划和学习记录。可以在 **偏好与设置 → 账号与同步** 合并访客记录，并在 **资料库** 同步本机附件。
- **备份**可在设置中导出和恢复 JSON。PDF 和图片原件可在资料库单独下载。两个在线入口的访客数据各自保存在对应网址下。

## 本地预览与部署

这个仓库提供可直接运行的静态站点。在仓库根目录运行以下命令，再用浏览器打开 `http://localhost:8000/`。

```sh
python3 -m http.server 8000
```

部署到 GitHub Pages 时，在仓库的 **Settings → Pages** 中选 **Deploy from a branch**，选择 `main` 和 `/(root)`。也可以把根目录发布到其他静态托管平台。发布时将 `index.html`、`favicon.svg`、`scene-*.webp` 和 `pdf-engine-*` 放在同一目录。

当前发布包连接线上版的账号同步服务。自建独立的账号与资料存储时，需要用自己的后端配置重新构建。PDF 阅读器的第三方许可见 [pdf-engine-LICENSE.txt](pdf-engine-LICENSE.txt)。

使用中遇到问题或有功能建议，欢迎在 [GitHub Issues](https://github.com/yangchunkitandy-a11y/study-plan/issues) 反馈。
