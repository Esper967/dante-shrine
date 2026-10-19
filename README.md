# 恶魔五月哭 · 循环祭坛（GitHub Pages 版）

《恶魔五月哭》AI 短剧的 9 分钟循环播放页：有声音、有歌单、有意义不明的祭坛特效。
纯静态，两个文件即可托管。

## 文件

| 文件 | 说明 |
| --- | --- |
| `index.html` | 页面本体（HTML/CSS/JS 全内联） |
| `dante.mp4` | 视频，976×720 / H.264 + AAC，约 39.7 MB |
| `.nojekyll` | 告诉 GitHub Pages 不要跑 Jekyll，直接按静态文件发布 |

> 没有上传 `cloudflared.exe`、本地服务器脚本或临时二维码，这些只用于本地临时分享。

## 上传到 GitHub Pages（网页操作）

1. 登录 GitHub，新建一个 **Public** 仓库，例如 `dante-shrine`。
2. 把本目录下的 `index.html`、`dante.mp4`、`.nojekyll` 上传到仓库根目录。
   - 网页端「Add file → Upload files」一次拖入即可；超过 25 MB 的文件网页端可能要求用 Git 命令行。
3. 进入仓库 **Settings → Pages**：
   - Source 选 **Deploy from a branch**
   - Branch 选 `main`，目录选 `/ (root)`，保存。
4. 等 1～2 分钟，访问 `https://<你的用户名>.github.io/dante-shrine/`。

## 上传到 GitHub Pages（命令行）

```bash
git init
git add index.html dante.mp4 .nojekyll
git commit -m "dante shrine"
git branch -M main
git remote add origin https://github.com/<你的用户名>/dante-shrine.git
git push -u origin main
```

然后在仓库 Settings → Pages 里启用 `main` 分支根目录。

## 注意

- **仓库必须是 Public**：GitHub 免费账号只能给公开仓库开 Pages，等于视频也会公开。
- 视频 39.7 MB，低于 GitHub 单文件 50 MB 警告线、100 MB 硬上限，可以直接提交；仓库历史里只存一份，不要反复替换大文件。
- Pages 站点有 1 GB 容量、每月约 100 GB 流量的软限制；这个页面按 40 MB/次播放计算，朋友小范围分享完全够用。
- 这是对 TikTok 创作者 `@the.radiant.studios` 内容的转载页面，建议在页面或 README 里注明出处；公开仓库属于再分发，若原作者投诉需要自行下架。
- 国内访问 `github.io` 有时较慢，微信内置浏览器也可能提示「非微信官方网页」；必要时可绑定自己的域名或继续用临时隧道。
