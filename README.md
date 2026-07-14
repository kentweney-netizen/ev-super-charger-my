# EV Super Charger MY

**马来西亚电动汽车超级充电地图（轻量版 PWA）**

一站式发现附近充电站，自动定位，并一键跳转到对应运营商 App（ChargeSini、JomCharge、Gentari、ChargeEV、Shell 等）。

> 解决目前马来西亚充电 App 太多、每次换地方都要重新找 App 的痛点。

---

## 功能特点

- 自动获取当前位置
- 地图 + 列表双视图
- 按距离排序
- 支持筛选（AC/DC、运营商）
- 一键打开对应充电运营商 App（Deep Link + 应用商店降级）
- 一键导航（Google Maps）
- 支持「添加到主屏幕」（PWA）
- 基础离线缓存

## 技术栈

- 纯前端（HTML + CSS + JavaScript）
- Leaflet.js + OpenStreetMap
- Progressive Web App（Manifest + Service Worker）
- 后续可轻松接入 Supabase 作为后端

## 在线体验

（部署后把链接放这里）

## 本地运行

1. 下载或克隆本仓库
2. 用任意静态服务器打开（推荐）：

```bash
# 方法1：使用 VS Code 的 Live Server 插件
# 方法2：Python
python -m http.server 8080

# 方法3：Node.js
npx serve .
```

3. 用手机浏览器访问电脑的 IP 地址，或直接用手机打开 `index.html`

## 部署到免费托管（推荐）

### 方法一：Cloudflare Pages（最推荐）

1. 把代码推送到 GitHub
2. 登录 [Cloudflare Pages](https://pages.cloudflare.com)
3. 连接 GitHub 仓库
4. 构建设置保持默认（因为是纯静态）
5. 部署完成后获得 `https://xxx.pages.dev` 链接

### 方法二：Vercel

1. 登录 [vercel.com](https://vercel.com)
2. Import GitHub 仓库
3. 直接 Deploy

### 方法三：GitHub Pages

1. 仓库 Settings → Pages
2. Source 选择 `main` 分支的 `/ (root)`
3. 保存后等待几分钟即可访问

## 项目结构

```
ev-super-charger/
├── index.html          # 主页面
├── manifest.json       # PWA 配置
├── sw.js               # Service Worker
├── icons/              # 应用图标
│   ├── icon-192.png
│   ├── icon-512.png
│   └── apple-touch-icon.png
└── README.md
```

## 后续计划

- [ ] 接入真实充电站数据（Supabase）
- [ ] 中英双语切换
- [ ] 用户上报充电站状态
- [ ] 打包成 Android APK（Capacitor）
- [ ] 上架 Google Play / App Store

## 贡献

欢迎提 Issue 和 Pull Request。

## License

MIT
