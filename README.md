# Twitter/X 屏蔽互fo/互粉/互关推文 (Mutual Follow Blocker)

[![GitHub stars](https://img.shields.io/github/stars/Asakushen/Twitter_Mutual_Follow_Blocker?style=social)](https://github.com/Asakushen/Twitter_Mutual_Follow_Blocker)
[![GreasyFork](https://img.shields.io/badge/GreasyFork-Install_Script-red.svg)](https://greasyfork.org/zh-CN/scripts/557093)
[![License](https://img.shields.io/github/license/Asakushen/Twitter_Mutual_Follow_Blocker)](LICENSE)
![Version](https://img.shields.io/badge/Version-1.0-blue.svg)

> **净化推特时间线，拒绝无效社交噪音。**

一个轻量级、高性能的 Tampermonkey (油猴) 脚本，专为 Twitter (X.com) 设计。它可以自动识别并**折叠**那些为了刷数据而存在的“互fo”、“互粉”、“互关”账号的推文，还你一个清爽的浏览体验。

---

## 📖 简介 (Introduction)

浏览推特时，你是否经常被大量的“互fo”、“诚信互关”、“回fo”推文刷屏？这些内容往往没有实际价值，严重影响信息获取效率。

本脚本**不会简单粗暴地删除**这些推文（因为这会导致推特虚拟列表渲染出错，出现页面闪烁或内容错位），而是采用**折叠**的方式，将其替换为一个不显眼的提示条。

## ✨ 核心功能 (Features)

* **🛡️ 智能正则匹配**：内置高效正则表达式，精准识别用户名中的“互fo”、“互粉”、“互关”、“互赞”等关键词。
* **📂 非破坏性折叠**：将目标推文隐藏并替换为提示条，点击即可临时展开查看，避免误杀。
* **⚡ 极低资源占用**：使用 `MutationObserver` 监听 DOM 变化，完美支持推特的无限滚动加载，无感运行。
* **🎨 原生 UI 适配**：提示条样式自动适配推特亮色/暗色/黑夜模式，视觉体验统一。
* **🔒 安全零风险**：纯前端脚本，仅修改本地显示逻辑，**不调用任何 Twitter API**，绝无封号风险。

## 🚀 安装指南 (Installation)

### 1. 安装脚本管理器
首先，你需要为浏览器安装 **Tampermonkey** (油猴) 插件：
* [Chrome / Edge / Brave](https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo)
* [Firefox](https://addons.mozilla.org/zh-CN/firefox/addon/tampermonkey/)

### 2. 安装脚本
你可以选择以下任意一种方式安装：

* **方式 A (推荐 - 自动更新)**：
    [👉 **前往 GreasyFork 安装**](https://update.greasyfork.org/scripts/557093/TwitterX%20%E5%B1%8F%E8%94%BD%E4%BA%92fo%E4%BA%92%E7%B2%89%E4%BA%92%E5%85%B3%E6%8E%A8%E6%96%87.user.js)
    *(建议使用此方式，以便后续自动接收新功能推送)*

* **方式 B (手动 - 开发者)**：
    点击仓库中的 `Twitter_Mutual_Follow_Blocker.user.js` 文件，点击 "Raw" 按钮即可触发安装。

### 3. 生效
安装完成后，刷新 Twitter/X 页面即可生效。

## ⚙️ 个性化配置 (Configuration)

如果你想自定义屏蔽的关键词（例如屏蔽“币圈”或特定的营销词），可以编辑脚本代码中的 `BLOCK_KEYWORDS` 数组。

(这里填三个反引号)javascript
// 打开脚本编辑器，找到约第 18 行：
const BLOCK_KEYWORDS = [
    /互(fo|粉|关|赞|推|回)/i,  // 默认规则
    /fo回/i,
    /诚信互/i,
    /你的新关键词/i             // 在这里添加，支持正则
];
(这里填三个反引号)

## 📸 效果截图 (Preview)

脚本运行后，原本占据大版面的互粉推文将变为如下样式：

> **[ 🟦 已折叠一条来自 "xxx(互fo）" 的推文 (包含互粉关键词) - 点击查看 ]**

*点击该横条，内容将临时展开。*

## 🛠️ 开发与贡献 (Contributing)

欢迎提交 [Issue](https://github.com/Asakushen/Twitter_Mutual_Follow_Blocker/issues) 反馈 Bug 或建议。如果你有更好的正则匹配规则，欢迎提交 Pull Request！

1.  Fork 本仓库
2.  创建你的 Feature 分支 (`git checkout -b feature/AmazingFeature`)
3.  提交修改 (`git commit -m 'Add some AmazingFeature'`)
4.  推送到分支 (`git push origin feature/AmazingFeature`)
5.  提交 Pull Request

## 🌟 支持 (Support)

如果这个脚本让你的推特时间线变干净了，请**给这个仓库点一个 Star ⭐**！
这是对我最大的鼓励！

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=Asakushen/Twitter_Mutual_Follow_Blocker&type=date&legend=top-left)](https://www.star-history.com/#Asakushen/Twitter_Mutual_Follow_Blocker&type=date&legend=top-left)

## 📄 许可证 (License)

本项目基于 [MIT License](LICENSE) 分发。
