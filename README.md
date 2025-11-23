# Vue OpenLayers Examples

一个基于 Vue 3 + TypeScript + Vite 的 OpenLayers 地图示例项目，提供各种地图功能和交互示例。

## 🗺️ 项目特性

- 🚀 **Vue 3** - 使用 Composition API 和 `<script setup>` 语法
- 📍 **OpenLayers 10.7.0** - 强大的开源地图库
- 📘 **TypeScript** - 完整的类型支持
- 🎨 **Less** - CSS 预处理器支持
- 🛠️ **Vite** - 快速的前端构建工具
- 🧭 **Vue Router** - 路由管理
- ✨ **ESLint + Prettier** - 代码规范和格式化

## 📦 技术栈

- **前端框架**: Vue 3.5.22
- **地图库**: OpenLayers 10.7.0
- **开发语言**: TypeScript
- **构建工具**: Vite 7.1.11
- **样式预处理**: Less 4.4.2
- **路由**: Vue Router 4.6.3
- **包管理器**: pnpm
- **代码规范**: ESLint + Prettier
- **CI/CD**: GitHub Actions

## 🚀 快速开始

### 环境要求

- Node.js ^20.19.0 || >=22.12.0
- npm 或 yarn 或 pnpm

### 安装依赖

```sh
npm install
```

### 开发模式

```sh
npm run dev
```

启动开发服务器，访问 http://localhost:5173

### 生产构建

```sh
npm run build
```

### 预览构建结果

```sh
npm run preview
```

## 📖 示例访问

### 在线访问
部署完成后，您可以通过以下链接访问示例：

- **主应用**：`https://sogrey.github.io/vue-ol-examples/`
- **绘制几何图形示例**：`https://sogrey.github.io/vue-ol-examples/examples/draw-geometric-shapes.html`

### 本地访问
在开发模式下，您可以：
- 启动开发服务器：`npm run dev`
- 访问主应用：`http://localhost:5173`
- 访问示例：`http://localhost:5173/examples/draw-geometric-shapes.html`

## 🚀 部署

### GitHub Pages 自动部署

项目配置了 GitHub Actions 自动部署功能：

- 当代码推送到 `main` 分支时，会自动触发构建和部署流程
- 构建后的文件会自动部署到 GitHub Pages
- 使用 Node.js 20 环境进行构建
- 使用 npm 作为包管理器，确保依赖版本一致性
- 支持并发部署管理
- 仅在 `main` 分支推送时执行实际部署

#### 部署流程说明：
1. **代码检出** - 获取最新代码
2. **环境设置** - 安装 Node.js 20
3. **依赖安装** - 使用 `npm install` 安装项目依赖（支持pnpm-lock.yaml）
4. **项目构建** - 执行 `npm run build` 生成生产版本
5. **页面配置** - 设置 GitHub Pages 配置
6. **上传构建产物** - 上传 `dist/` 目录
7. **自动部署** - 部署到 GitHub Pages

部署工作流文件位置：`.github/workflows/deploy.yml`

### 手动部署

如果需要手动部署到其他平台：

```sh
# 构建生产版本
npm run build

# 构建后的文件在 dist/ 目录
# 可以将 dist/ 目录内容部署到任何静态文件服务器
```

### 本地预览

在部署前，可以在本地预览构建结果：

```sh
# 构建项目
npm run build

# 启动预览服务器
npm run preview
```

### 代码检查和修复

```sh
npm run lint
```

### 代码格式化

```sh
npm run format
```

### 类型检查

```sh
npm run type-check
```

## 📁 项目结构

```
src/
├── components/          # 公共组件
├── views/              # 页面组件
│   └── 00-Quick-Start.vue  # 快速开始示例
├── assets/             # 静态资源
├── router/             # 路由配置
├── App.vue             # 根组件
└── main.ts             # 入口文件

public/
├── favicon.ico         # 网站图标
├── examples/           # 可直接访问的示例文件
│   └── draw-geometric-shapes.html  # 绘制几何图形示例
└── ...
```

## 🗺️ 示例说明

### 00-Quick-Start (src/views/00-Quick-Start.vue)
基础的 OpenLayers 地图示例，展示如何：
- 创建地图实例
- 添加 OSM 瓦片图层
- 设置地图视图
- 管理地图生命周期

### draw-geometric-shapes (public/examples/draw-geometric-shapes.html)
OpenLayers 绘制几何图形示例，包含功能：
- 支持多种几何图形绘制：点、线、面、圆、正方形、矩形
- 使用高德地图作为底图
- 交互式绘制工具
- 自定义样式和交互体验
- 鼠标位置显示控件
- **可直接访问**：部署后可通过 `/examples/draw-geometric-shapes.html` 直接访问

#### 技术特点：
- 使用 OpenLayers Vector 图层进行矢量图形绘制
- 支持规则图形的几何函数
- 响应式UI设计
- 优雅的样式和用户体验
- 独立的HTML文件，无需构建环境即可运行

更多示例持续更新中...

## 🛠️ 开发工具推荐

### IDE 配置
推荐使用 [VS Code](https://code.visualstudio.com/) + [Vue (Official)](https://marketplace.visualstudio.com/items?itemName=Vue.volar) 扩展（禁用 Vetur）。

### 浏览器开发工具

**基于 Chromium 的浏览器（Chrome、Edge、Brave 等）：**
- [Vue.js devtools](https://chromewebstore.google.com/detail/vuejs-devtools/nhdogjmejiglipccpnnnanhbledajbpd)
- [在 Chrome DevTools 中开启 Custom Object Formatter](http://bit.ly/object-formatters)

**Firefox：**
- [Vue.js devtools](https://addons.mozilla.org/en-US/firefox/addon/vue-js-devtools/)
- [在 Firefox DevTools 中开启 Custom Object Formatter](https://fxdx.dev/firefox-devtools-custom-object-formatters/)

## 🔧 自定义配置

详细配置请参考 [Vite Configuration Reference](https://vite.dev/config/)。

## 📄 许可证

[MIT License](LICENSE)

## 🤝 贡献

欢迎提交 Issue 和 Pull Request！

## 📚 相关资源

- [Vue 3 官方文档](https://vuejs.org/)
- [OpenLayers 官方文档](https://openlayers.org/)
- [TypeScript 官方文档](https://www.typescriptlang.org/)
- [Vite 官方文档](https://vite.dev/)
