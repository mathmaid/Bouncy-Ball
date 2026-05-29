# BOUNCY · 弹球消砖块

一个霓虹风的弹球消砖块小游戏：瞄准发射一串小球，敲掉上方带数字的方块，吃到橙色 `+1` 球就能让下回合多一颗球，越攒越多。别让方块压到底线！

纯前端单文件（HTML + Canvas + 原生 JS），**无后端、无构建步骤**，最高分用浏览器 `localStorage` 本地保存。

## 本地预览

直接用浏览器打开 `index.html` 即可。或者起一个本地静态服务器：

```bash
npx serve .
# 然后访问终端里打印的地址（默认 http://localhost:3000）
```

## 部署到 Vercel

### 方式一：网页导入 Git 仓库（推荐）

1. 把代码推到 GitHub（本仓库已经是了）。
2. 打开 [vercel.com](https://vercel.com)，点 **Add New → Project**，**Import** 这个仓库。
3. **Framework Preset** 选 **Other**（纯静态，无需框架）。
4. **Build Command** 和 **Output Directory** 都留空——Vercel 会直接把根目录下的 `index.html` 作为首页。
5. 点 **Deploy**，完成后即可通过分配的 `*.vercel.app` 域名直接游玩。

之后每次 `git push`，Vercel 会自动重新部署。

### 方式二：Vercel CLI

```bash
npm i -g vercel   # 安装 CLI
vercel            # 在仓库根目录运行，生成预览部署
vercel --prod     # 发布到生产环境
```

## 文件说明

| 文件 | 作用 |
| --- | --- |
| `index.html` | 游戏本体（结构 / 样式 / 逻辑都在这一个文件里） |
| `vercel.json` | Vercel 静态部署配置（安全响应头） |
| `.gitignore` | 忽略 `.vercel` 等本地文件 |
