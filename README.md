# OJO Pet Founder Test

一个面向 OJO Pet Buildathon 的单页病毒传播小游戏：用户上传宠物照片、回答 4 道轻量问题，即可获得宠物 Founder 人格、创业产品 Demo 和带回流二维码的分享海报。

## 在线体验

https://ojo-pet-founder-test.prudenceyang167.chatgpt.site

## 核心体验

- 宠物照片上传，自动压缩至最长边 1600px，减少大图卡顿
- 4 道点按式场景题，约 20 秒完成
- 4 种 Founder 人格和对应的 OJO 产品概念
- 结果页内置可互动的迷你产品 Demo
- 一键生成 1080 × 1440 PNG 分享海报
- 页面二维码和海报二维码均指向当前测试地址
- 结果页提供跳转 OJO 官网的 Build CTA，并通过 UTM 标记活动来源
- 支持跳过照片、重复测试和移动端布局
- 无后端、无账户、无数据上传；照片只在浏览器本地处理

## 本地运行

项目是纯静态页面，无需安装依赖：

```bash
python3 -m http.server 4173 --directory dist
```

然后访问 `http://127.0.0.1:4173/`。

## 项目结构

```text
dist/
├── index.html
├── assets/
│   └── pet-founder-hero.png
└── vendor/
    └── qrcode-generator.min.js
```

`dist/vendor/qrcode-generator.min.js` 固定使用 `qrcode-generator@1.4.4`，随项目本地加载，避免活动现场依赖外部 CDN。该依赖使用 MIT License。

## 测试

回归测试结果见 [QA_REPORT.md](QA_REPORT.md)。

