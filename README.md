# 记·账 - 智能记账 App

适配 Android 16 的记账应用，支持分类管理、报表分析、资产管理、数据导出。

## 功能

- 📝 支出/收入记录，大类 + 子分类 + 自定义
- 📊 月度/年度报表，饼图分类占比
- 💰 资产汇总（支付宝/微信/银行卡等）
- 🎨 主题切换（自动/白色/黑色）
- 📤 CSV / JSON 导出
- 📥 JSON 数据导入/备份

## 本地预览

```bash
# 浏览器直接打开
open index.html
# 或
npx serve www
```

## 构建 APK

### 方式一：GitHub Actions（推荐）

1. 创建 GitHub 仓库
2. 上传此项目所有文件
3. Push 到 main 分支
4. GitHub Actions 自动构建 APK
5. 在 Actions → Artifacts 下载 `app-debug`

### 方式二：本地构建

```bash
# 前置要求：Node.js 18+、Java 17、Android SDK

npm install
npx cap sync android
cd android
./gradlew assembleDebug
# APK 位置：android/app/build/outputs/apk/debug/app-debug.apk
```

## 项目结构

```
├── index.html              # 主应用（单文件 Web App）
├── www/index.html          # Capacitor web 资源
├── android/                # Android 原生项目
├── capacitor.config.json   # Capacitor 配置
├── package.json
└── .github/workflows/      # GitHub Actions 自动构建
```
