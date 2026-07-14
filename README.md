# hpackgen  
**自动生成 HMCL 自动更新整合包配置的整合包构建工具**

hpackgen 是一个面向服务器管理员与整合包作者的自动化构建工具，用于生成 HMCL 自动更新整合包所需的全部配置文件。它能够自动扫描整合包内容、计算文件哈希、生成 manifest.json，并输出符合 HMCL 自动更新规范的整合包更新结构。

通过 hpackgen，你可以在每次更新模组、资源包或配置文件后，一键生成更新包并部署到你的更新服务器，让客户端 HMCL 自动检测并下载最新版本。

---

## ✦ 功能特点
- 自动生成 **manifest.json**（HMCL 自动更新整合包配置）  
- 自动扫描整合包目录并生成 **files[] 文件列表与哈希**  
- 自动写入 **整合包信息（name / author / version / description）**  
- 自动生成 **addons[]（game / forge / neoforge 等版本信息）**  
- 支持自定义 **fileApi**（整合包更新服务器地址）  
- 适合整合包频繁更新的服务器环境  

---

## ✦ 适用场景
- 需要频繁更新模组或配置的服务器  
- 需要自动分发整合包更新的 HMCL 用户  
- 想要减少手工编辑 manifest.json 的整合包作者  
- 想要构建自动化整合包发布流水线的开发者  

---

## ✦ 输出示例（由 hpackgen 自动生成）
```json
{
  "name": "1szt",
  "author": "1szt",
  "version": "1szt",
  "description": "# 欢迎来到 1szt 服务器\n\n感谢你选择加入我们的世界。\n交流与反馈请前往 QQ 群：565941634\n",
  "fileApi": "https://mc.1szt.com",
  "files": [
    {
      "path": "icon.png",
      "hash": "59ed14aa8d6276fc1ff3f40d3c681b828ec9a51a"
    }
  ],
  "addons": [
    {
      "id": "game",
      "version": "1.21.1"
    },
    {
      "id": "neoforge",
      "version": "21.1.236"
    }
  ]
}
```
