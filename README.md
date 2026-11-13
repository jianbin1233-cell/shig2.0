# 拾光 · Notes 2.0

液态玻璃风格的 Android 便签应用工程。

## 当前实现
- 液态玻璃风格首页、便签编辑器、悬浮底栏、深浅主题/系统主题
- 便签新增、编辑、置顶、收藏、分类、搜索
- 图片附件（以本地数据形式保存）
- 归档、回收站恢复、隐藏便签管理
- PDF 导出、PNG 长图生成、系统文字分享、复制
- JSON 数据备份与恢复
- 本地通知提醒（需授予通知权限）
- 生物识别验证接口示例

## 重要说明
本工程是 Capacitor Android 工程源文件，GitHub Actions 会生成 debug APK。
首次构建必须上传整个项目内容，包括隐藏目录 `.github/workflows`。

生物识别目前提供验证调用，但尚未实现应用冷启动/切后台后的完整强制锁屏流程；“隐藏便签”目前是界面隐藏，不是加密存储。PDF 中文字体嵌入、图片自动排版及多页图片支持仍需进一步完善和真机验收。请勿将当前版本用于存放高度敏感资料。

## 构建
```bash
npm install
npx cap add android
npx cap sync android
cd android
./gradlew assembleDebug
```

或推送到 GitHub，在 Actions 中运行 `Build Android APK`，下载 artifact `shiguang-v2-debug-apk`。
