<div align="center">
  <h1>🌌 星系风格个人介绍主页 | Galaxy Theme Portfolio</h1>
</div>

<p align="center">
  <strong>基于 Astro 6 + Three.js 打造的高颜值、沉浸式暗黑星空个人主页 & 作品集</strong>
</p>

<p align="center">
  <a href="https://astro.build/"><img src="https://img.shields.io/badge/Astro-6.x-883AEA?style=for-the-badge&logo=astro&logoColor=white" alt="Astro 6"></a>
  <a href="https://threejs.org/"><img src="https://img.shields.io/badge/Three.js-v0.184-black?style=for-the-badge&logo=three.js&logoColor=white" alt="Three.js"></a>
  <a href="https://www.typescriptlang.org/"><img src="https://img.shields.io/badge/TypeScript-5.9-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-GPL--3.0-blue?style=for-the-badge" alt="License"></a>
</p>

<p align="center">
  <a href="README.md"><strong>🇨🇳 中文文档</strong></a> ·
  <a href="README_EN.md"><strong>🇺🇸 English</strong></a> ·
  <a href="https://ai-work-team-demo.pages.dev"><strong>🔮 DEMO</strong></a> ·
  <a href="#快速开始"><strong>🚀 快速开始</strong></a> ·
  <a href="#网站内容配置"><strong>📔 网站配置</strong></a>
</p>

---

## ✨ 功能

- 🌌 **3D 粒子梦幻星空**：基于 Three.js 动态生成的羽化圆形发光粒子，随鼠标平滑交互与正弦波明暗呼吸。
- 🧪 **4 套实验性暗黑主题**：顶部右侧 Labs 图标一键切换【幽蓝】、【翡翠】、【紫粉】与【琥珀金】主题，3D 粒子色彩无缝联动。
- 💫 **360° 流水转圈按钮**：核心按钮自带顺时针激光流光边框，搭配文字白色透明荧光笔划过动画。
- 📱 **单屏与自适应响应式**：首页锁定单屏极简展示，About 页面提供卡片化丰富履历。

---

## 快速开始

只需简单的 3 个步骤，即可拥有属于您自己的星系风格个人主页：

### Fork本仓库

点击本仓库右上角的 **Fork** 按钮复制到您自己的 GitHub 账号下，或在本地克隆：

```bash
git clone https://github.com/FrankWkd-Plus/galaxy-theme-portfolio.git
cd galaxy-theme-portfolio
npm install
```

---

### 网站内容配置

#### 🔹 1. 首页文字与按钮 (`src/components/Hero.astro`)
- 修改 `HELLO, I'M` 与 `Outwardly Verse` 大标题文字。
- 修改 `About Me` 跳转链接与 `Read Blog` 外部博客链接。

#### 🔹 2. 顶部导航与 GitHub 图标 (`src/components/Navigation.astro`)
- 修改 Logo 名字 `Outwardly Verse`。
- 将左上角与抽屉菜单中的 `https://github.com/FrankWkd-Plus` 替换为您自己的 GitHub 主页地址。

#### 🔹 3. 个人简历与技能卡片 (`src/pages/about.astro`)
- 修改工作室名称、Slogan 与提示框。
- 在 `.skills-matrix` 中修改或替换您擅长技术的 Shields.io 徽章。
- 在 `.projects-grid` 与 `.contacts-grid` 中填入您的个人项目及联系方式（Email、小红书、Telegram 等）。

---

### 部署到 Cloudflare Pages

1. 登录 [Cloudflare Dashboard](https://dash.cloudflare.com/)，进入 **Workers & Pages** -> **Create application** -> **Pages**。
2. 选择 **Connect to Git** 并关联您刚才 Fork 的 GitHub 仓库。
3. 在构建设置中填入以下参数：

| 配置项 (Setting) | 填写内容 (Value) |
| :--- | :--- |
| **Framework preset (框架预设)** | `Astro` |
| **Build command (构建命令)** | `npm run build` |
| **Build output directory (输出目录)** | `dist` |
| **Root directory (根目录)** | 留空（或填 `/`） |

4. 点击 **Save and Deploy**

---

## 🛠️ 进行贡献

```bash
# 启动本地开发服务器
npm run dev

# 构建生产环境代码
npm run build

# 本地预览打包产物
npm run preview
```

---

## 📄 开源许可证

本项目采用 [GNU General Public License v3.0 (GPL-3.0)](LICENSE) 开源许可协议。

---

<p align="center">
  Crafted with ❤️ by <a href="https://github.com/FrankWkd-Plus">FrankWkd</a>
</p>
