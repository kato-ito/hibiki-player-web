# Hibiki Player 网页版（单文件）

**⬇️ 直接下载：[`hibiki-player.html`](https://github.com/kato-ito/hibiki-player-web/releases/latest/download/hibiki-player.html)**
—— 93 KB 单文件，双击用浏览器打开即用，不需要安装、不需要服务器、不联网也能播放本地音乐。

本地音乐播放器网页版：**波形 · 频谱 · 声谱图 · 声场** 四种可视化，Apple Music 风格播放界面，
歌词逐行高亮，歌单矩阵主界面 + 迷你播放条。歌单与设置只保存在浏览器本机（localStorage），
不上传任何服务器、没有任何遥测。

## 怎么用

1. 下载 `hibiki-player.html`（或直接克隆本仓库）；
2. 双击用 Chrome / Edge 打开；
3. 🎵 多选文件、📂 选整个文件夹，或把文件 / 文件夹直接拖进页面即可播放；
   同名 `.lrc` 歌词一起导入会自动配对，也可以在界面里手动载入。

## 网页版没有的能力（需要桌面版）

- **杜比 / DTS 解码**（AC-3 · E-AC-3 · TrueHD · DTS · WMA 及内含这些音轨的 MP4 / MKV / MKA）——
  浏览器不能播放这些编码，桌面版内置 FFmpeg 转码后播放；
- **B 站音频下载 / 扫码登录**（原始音频封装为 M4A、会员音质等）；
- **本地歌单持久化**（保存绝对路径、重开自动恢复）——浏览器受权限限制，重开页面需重新导入；
- 麦克风权限由主进程放行；网页版若被浏览器拦截授权，可在本文件所在目录执行
  `python -m http.server`，再访问 `http://localhost:8000/hibiki-player.html`。

## 相关仓库

- Windows 桌面版（含安装包直接下载）：[hibiki-player](https://github.com/kato-ito/hibiki-player)
- 安卓版（APK）：[hibiki-player-android](https://github.com/kato-ito/hibiki-player-android)

## 说明

- 单文件、零外部依赖：样式 / 脚本 / 二维码库全部内联，页面不请求任何外部资源；
- 与桌面版同源：桌面版工程在 `hibiki-player` 仓库的 `app/`，界面改动两边需手工同步；
- 建议使用最新版 Chrome / Edge（需要 Web Audio 与 `AudioContext` 图形分析能力）。

## 许可

[MIT](LICENSE) © 2026 Zai
