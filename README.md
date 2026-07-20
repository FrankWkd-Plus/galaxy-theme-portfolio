# 🌌 Darkness — Modern Dark Portfolio & Studio Theme

<p align="center">
  <strong>基于 Astro 6 与 Three.js 构建的极简暗黑风作品集 & 个人主页主题</strong>
</p>

<p align="center">
  搭载 GPU 加速的 5,000 动态交互圆形光晕粒子星空背景，兼具极致性能体验与现代极客审美。
</p>

<p align="center">
  <a href="https://astro.build/"><img src="https://img.shields.io/badge/Astro-6.x-883AEA?style=for-the-badge&logo=astro&logoColor=white" alt="Astro 6"></a>
  <a href="https://threejs.org/"><img src="https://img.shields.io/badge/Three.js-v0.184-black?style=for-the-badge&logo=three.js&logoColor=white" alt="Three.js"></a>
  <a href="https://www.typescriptlang.org/"><img src="https://img.shields.io/badge/TypeScript-5.9-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-41D1FF?style=for-the-badge" alt="License"></a>
</p>

---

- ⚡️ **GPU 驱动的三维粒子背景**：基于 Three.js 动态生成高斯羽化径向渐变贴图，展现真实圆形光晕梦幻星空。
- 📱 **单屏全端自适应**：首页精确锁定单屏展示，配合全端响应式悬浮导航与移动端抽屉菜单。
- 👤 **独立美化 About Studio 页面**：内置高度结构化的个人简历、技能 Shields 徽章矩阵、项目 Showcase 与联系方式网格。
- 🎨 **极客暗黑主题**：纯正高对比度通透暗黑底色 (`#030712`)，搭配流畅文字荧光笔划过动画与无雾呼吸闪烁。
- 🚀 **Astro 6 极致性能**：零 JS 运行时开销，开箱即用的静态生成与云端无缝部署。

---

## 🛠️ 快速开始

> 💡 **运行环境要求**：Node.js **v22.0.0+** (以完全支持 Astro 6)。

```bash
# 1. 克隆项目仓库
git clone https://github.com/FrankWkd-Plus/My-Personal-Introduction.git
cd My-Personal-Introduction

# 2. 安装依赖包
npm install

# 3. 启动开发服务器
npm run dev

# 4. 构建生产环境包
npm run build
```

---

## 📘 详细配置指南 (Configuration Guide)

本项目采用模块化开发结构，绝大部分配置均可通过修改对应文件轻松完成：

### 1. 首页大屏与标语配置 (`src/components/Hero.astro`)

控制首页的核心文字、按钮跳转与荧光划过动画：

- **问候语与大标题**：
  ```html
  <div class="greeting">HELLO, I'M</div>
  <h1 class="hero-title">
    <span class="title-text">Outwardly Verse</span>
  </h1>
  ```
- **按钮跳转设置**：
  - `About Me` 按钮跳转站内页面：`href={`${base}about/`}`
  - `Read Blog` 按钮跳转外部独立博客：`href="https://your-blog-domain.com"`（已配置斜右上重定向图标 `↗`）
- **文字荧光笔划过特效**：
  在 `.title-text` 的 CSS 中通过 `highlighterSweep` 动画控制白色透明荧光笔划过的扫光周期：
  ```css
  animation: 
    highlighterSweep 3.5s cubic-bezier(0.4, 0, 0.2, 1) infinite,
    gradientFlow 5s ease infinite,
    cleanBreathe 3s ease-in-out infinite;
  ```

---

### 2. 顶部导航栏与 GitHub 图标 (`src/components/Navigation.astro`)

配置顶部悬浮导航栏与左上角社交图标：

- **左上角 Logo 与 GitHub 个人主页图标**：
  在 `.nav-left` 中修改 Logo 名称与左上角 GitHub 地址：
  ```html
  <div class="nav-left">
    <a href={base} class="logo">Outwardly Verse</a>
    <a href="https://github.com/Your-GitHub-ID" target="_blank" rel="noopener noreferrer" class="github-link">
      <!-- GitHub Icon SVG -->
    </a>
  </div>
  ```
- **桌面端与移动端抽屉菜单**：
  修改 `.nav-links`（桌面端）与 `.mobile-menu-content`（移动端抽屉）中的导航链接及重定向图标。

---

### 3. 独立 About 个人简历页面配置 (`src/pages/about.astro`)

展示完整的工作室品牌、技能矩阵与项目体验：

- **Studio 标题 & 写在前面提示框**：
  修改 `.studio-title`、`.studio-slogan` 与 `.tip-alert` 中的欢迎词与沟通风格提示。
- **个人标签 (Tags)**：
  在 `.tags-container` 中调整个人身份标记（如 `独立开发者`、`ENFJ 主人公`、`摄影发烧友` 等）。
- **技能 Shields 徽章矩阵 (`.skills-matrix`)**：
  根据个人技术栈替换 Shields.io 徽章图片地址（包含 System, Languages, Tools, AI, OI 等大类）：
  ```html
  <img src="https://img.shields.io/badge/-Linux-FCC624?style=flat-square&logo=linux&logoColor=black" alt="Linux" />
  ```
- **项目作品 Showcase (`.projects-grid`)**：
  在卡片列表中添加您的作品名称、描述、演示地址 (Demo) 与 GitHub 开源仓库地址。
- **联系方式卡片 (`.contacts-grid`)**：
  支持 Email、GitHub、Telegram、Nodeloc、CodeForces、小红书等卡片链接配置。

---

### 4. 3D 动态粒子星空配置 (`src/components/ThreeBackground.astro`)

定制背景 3D WebGL 交互粒子效果：

- **粒子数量与颜色**：
  ```typescript
  const particlesCount = 5000; // 调整粒子总数
  ```
  通过 `colorArray` 配置紫、粉、蓝三色渐变粒子的生成比例。
- **圆形真实光晕生成算法**：
  通过 `createCircleGlowTexture` 在 Canvas 2D 中生成径向渐变，消除硬件默认的方块边缘，结合 `AdditiveBlending` 实现透亮融合。

---

### 5. 主题配色与 Design Tokens (`src/styles/global.css`)

统一修改全站的主色彩系统：

```css
:root {
  /* 基础配色 */
  --color-bg-dark: #030712;       /* 深邃通透极客暗黑底色 */
  --color-bg-card: #0B132B;       /* 玻璃拟物卡片背景色 */
  --color-primary: #3B82F6;       /* 主色调天蓝 */
  --color-accent-purple: #8B5CF6; /* 渐变紫 */
  --color-accent-pink: #EC4899;   /* 渐变粉 */
  --color-text: #F8FAFC;          /* 高对比主体文本 */
}
```

---

## 🚀 部署发布指南

### 1. 部署到 Cloudflare Pages (推荐)

1. 在 Cloudflare Dashboard 创建新的 **Workers & Pages** 项目。
2. 关联您的 GitHub 仓库。
3. 填入构建配置：
   - **Framework preset（框架预设）**：`Astro`
   - **Build command（构建命令）**：`npm run build`
   - **Build output directory（输出目录）**：`dist`
   - **Root directory（根目录）**：留空（或填 `/`）

> ⚠️ **排查提示**：如果在自定义二级域名部署时遇到静态资源 404 MIME 类型报错，请确认 `astro.config.mjs` 中不要误加额外的 `base` 路径。

---

## 📂 项目结构概览

```text
src/
├── components/
│   ├── Navigation.astro      # 顶部悬浮导航栏 (含 GitHub 图标与移动端菜单)
│   ├── Hero.astro            # 首页单屏大屏 (含荧光笔划过动画)
│   └── ThreeBackground.astro # Three.js 5,000 圆形光晕粒子背景
├── layouts/
│   └── BaseLayout.astro      # 全局 HTML/CSS 结构与 ClientRouter 布局
├── pages/
│   ├── index.astro           # 首页 (单屏视口锁定)
│   └── about.astro           # 独立 About Studio 简历页面 (可纵向滚动)
└── styles/
    └── global.css            # 全局 CSS 变量与主色彩标记
```

---

## 📄 开源许可证

本项目采用 [MIT License](LICENSE) 许可协议。

---

<p align="center">
  Crafted with ❤️ by <a href="https://github.com/FrankWkd-Plus">FrankWkd</a>
</p>
