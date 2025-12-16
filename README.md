# 🎬 AudioVisual Web版 - Vercel部署指南

## 📋 项目说明

这是AudioVisual项目的Web版本，已从Electron桌面应用改造为纯前端网页应用，可直接部署到Vercel。

### ✨ 主要改动

1. **移除Electron依赖** - 改为纯HTML/CSS/JavaScript
2. **静态网页化** - 所有功能在浏览器中运行
3. **响应式设计** - 支持移动端和桌面端
4. **Vercel优化** - 添加了必要的配置文件

## 🚀 部署到Vercel

### 方法1：通过GitHub部署（推荐）

1. **创建GitHub仓库**
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/你的用户名/audiovisual-web.git
   git push -u origin main
   ```

2. **连接到Vercel**
   - 访问 [vercel.com](https://vercel.com)
   - 点击 "New Project"
   - 导入你的GitHub仓库
   - 点击 "Deploy"

3. **完成！**
   - Vercel会自动检测配置并部署
   - 部署完成后会获得一个`.vercel.app`域名

### 方法2：使用Vercel CLI

1. **安装Vercel CLI**
   ```bash
   npm install -g vercel
   ```

2. **登录Vercel**
   ```bash
   vercel login
   ```

3. **部署项目**
   ```bash
   vercel
   ```

4. **生产环境部署**
   ```bash
   vercel --prod
   ```

## 📁 项目结构

```
audiovisual-web/
├── index.html          # 主页面（包含所有代码）
├── vercel.json         # Vercel配置文件
└── README.md           # 本文件
```

## 🎯 功能特性

- ✅ 支持腾讯视频、爱奇艺、优酷、B站、芒果TV等主流平台
- ✅ 内置8个高质量解析接口
- ✅ 现代化响应式UI设计
- ✅ 移动端友好
- ✅ 无需后端服务器
- ✅ 完全免费部署

## 🛠️ 本地开发

由于是纯静态HTML文件，可以直接用浏览器打开：

```bash
# 方法1：直接打开
open index.html

# 方法2：使用Python简单服务器
python -m http.server 8000

# 方法3：使用Node.js服务器
npx serve
```

## ⚙️ 配置说明

### vercel.json 配置

- `builds`: 定义构建配置，使用静态文件构建器
- `routes`: 配置路由规则，所有请求指向index.html
- `headers`: 设置安全响应头

### 自定义解析接口

在`index.html`中找到`parsers`数组，可以添加或修改解析接口：

```javascript
const parsers = [
    { id: 1, name: '接口1', url: 'https://jx.xmflv.com/?url=' },
    { id: 2, name: '接口2', url: 'https://www.8090kzy.com/jiexi/?url=' },
    // 添加更多接口...
];
```

## 🔧 自定义域名

1. 在Vercel项目设置中点击 "Domains"
2. 添加你的域名
3. 按照提示配置DNS记录
4. 等待DNS生效（通常几分钟到几小时）

## ⚠️ 注意事项

1. **免责声明**
   - 本项目仅供学习交流使用
   - 严禁用于任何商业用途
   - 使用本工具产生的任何法律责任由使用者自行承担

2. **CORS问题**
   - 某些视频平台可能有CORS限制
   - 解析接口的可用性取决于第三方服务

3. **性能优化**
   - 所有资源已内联，无外部依赖
   - 使用CDN加速（由Vercel提供）
   - 响应式设计确保各端体验

## 📝 更新日志

### v2.0.0 (Web版)
- 🔄 完全重写为Web应用
- ✨ 现代化UI设计
- 📱 响应式布局
- 🚀 Vercel部署支持
- 🎨 渐变色主题

## 🤝 贡献

欢迎提交Issue和Pull Request！

## 📄 许可证

本项目采用原项目的许可证

## 🔗 相关链接

- [原项目地址](https://github.com/z77177/AudioVisual)
- [Vercel文档](https://vercel.com/docs)
- [HTML5文档](https://developer.mozilla.org/zh-CN/)

---

Made with ❤️ | Deployed on Vercel