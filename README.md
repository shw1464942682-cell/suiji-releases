# 随记安装包与更新

此仓库仅发布随记 Android APK、更新说明和更新清单，不包含用户账本、个人信息或签名私钥。

[下载最新安装包](https://github.com/shw1464942682-cell/suiji-releases/releases/latest)

手机安装1.8.0或更高版本后，在「设置 → 检查应用更新」下载。默认打开应用时每天最多检查一次，下载和安装均由使用者确认。旧版需先手动覆盖安装一次1.8.0，不要卸载或清除数据。

## 发布者以后怎样更新

1. 打开 Releases → Draft a new release，填写新版本标签（例如 v1.8.1）及更新说明。
2. 上传同包名、同原签名、versionCode更高的新APK。每个Release只上传一个APK。
3. 发布Release，保持普通正式版本，不标为Pre-release，并设为Latest。
4. 等Actions中Generate app update manifest显示绿色；工作流会自动验证APK并生成update.json，无需手填哈希，也不用向各手机传APK。

固定更新地址：
https://github.com/shw1464942682-cell/suiji-releases/releases/latest/download/update.json

注意：若先发布空Release再补传APK，工作流会失败；请在Actions中手动运行并填写该Release标签。新版本请新建Release，不要直接替换已发布APK。GitHub在部分网络中可能无法访问，用户可稍后重试。

## 当前兼容验证范围

1.8.0尝试调整无障碍服务入口以验证微信页面节点可读性；不能据此认定OPPO微信发红包、转账已经修复。覆盖升级保留原账本；不要卸载或清数据。升级后页面识别可能需要重新开启一次。
