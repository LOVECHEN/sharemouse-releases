# ShareMouse 发布镜像

[English](README.md)

自动镜像 [ShareMouse](https://www.sharemouse.com/) 官方发布。

## 工作原理

- 每天 08:00 UTC 通过 GitHub Actions **自动检测**，也支持手动触发
- 抓取官方下载页面和更新日志，获取最新的 Windows 和 macOS 版本号
- 下载安装包和便携版压缩包，计算 SHA-256 校验和
- 发布 GitHub Release，附带各平台的更新日志和文件校验信息
- Windows 和 macOS 版本号**独立追踪**——若两个平台达到相同版本号，资源会合并到同一个 Release 中

## 每个 Release 包含的文件

| 平台 | 文件 |
|------|------|
| 🪟 Windows | `ShareMouseSetup.exe`、`ShareMouse_USB.zip` |
| 🍎 macOS | `ShareMouseSetup.dmg`、`ShareMouseMac.zip` |

## 相关链接

- 📥 [官方下载页](https://www.sharemouse.com/download/)
- 📋 [Windows 更新日志](https://www.sharemouse.com/download/changelog/)
- 📋 [macOS 更新日志](https://www.sharemouse.com/download/changelog-mac/)
