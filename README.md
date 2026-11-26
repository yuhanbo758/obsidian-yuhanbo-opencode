# yuhanbo-opencode

## Overview

Use OpenCode in the Obsidian desktop sidebar to chat with vault notes, search, rewrite selections, and save conversations as Markdown. The free edition includes these features. An optional activation code unlocks scheduled tasks, bulk note updates, and SMTP notifications.

## Installation

1. Install and configure OpenCode on your desktop.
2. Download `main.js`, `manifest.json`, and `styles.css` from the same GitHub Release.
3. Place those files in `.obsidian/plugins/yuhanbo-opencode/` inside your vault. Reload Obsidian and enable **yuhanbo-opencode** under **Settings → Community plugins**.

## Usage

Click the notebook assistant ribbon icon. Type `@` alone, choose a note, and enter a question in the chat. Use **Save** to keep the conversation as Markdown. To edit a note, select text and choose the plugin's insert or replace command from the Command Palette. For automation, open the plugin settings, select a Markdown prompt and output folder, then use **Run now** to verify the result before scheduling it.

## Privacy

The plugin connects to a local OpenCode service using HTTP and SSE. The selected model provider can receive the prompts, attachments, and note content you choose to use. The configured SMTP service receives task notices only when email is enabled. The plugin can access explicitly configured Skills folders outside the vault and can invoke the installed OpenCode or Obsidian CLI. Activation is verified offline, and there is no telemetry.

在 Obsidian 桌面端使用 OpenCode 查找、引用和改写笔记，也可以把重复工作保存成定时任务。插件需要用户自行安装并配置 [OpenCode](https://opencode.ai/)。

## 安装

从 [GitHub Releases](https://github.com/yuhanbo758/obsidian-yuhanbo-opencode/releases) 下载同一版本的 `main.js`、`manifest.json` 和 `styles.css`，放入笔记库的 `.obsidian/plugins/yuhanbo-opencode/`。重载 Obsidian 后在「设置 → 第三方插件」启用 **yuhanbo-opencode**。点击左侧「笔记助理」图标打开面板。

默认连接 `http://localhost:8091`。端口已占用且无法连接时，请核对服务或换用空闲端口。自动启动调用用户已安装的 OpenCode。模型和提供商使用 OpenCode 的配置，提供商可能另行收费。

从旧版手动安装迁移时，备份原安装目录，停用旧版，再安装新 ID。旧版设置可按需从原目录的 data.json 在本机复制，已有 Obsidian 快捷键需要按新插件 ID 重新绑定。

## 免费功能与自动化授权

| 免费使用 | 需要自动化激活码 |
| --- | --- |
| 聊天、模型切换、文件引用、图片、Markdown 聊天记录 | 创建、编辑并运行每日或一次性定时任务，也可立即执行 |
| Markdown 模板、本地 Skills、全文搜索、编辑器插入与替换 | 按 WikiLink、Dataview 或 DataviewJS 查询结果批量追加或覆盖笔记 |
| 查看已有任务及笔记产物 | SMTP 任务邮件及测试邮件 |

在「设置 → yuhanbo-opencode → 自动化授权」粘贴由维护者签发的激活码并点击「激活」。插件在本地用 Ed25519 公钥验签，无需账户或授权服务器。激活码保存在当前笔记库的插件设置中。移除激活会暂停定时器并保留任务和产物。当前签发格式没有到期时间、设备绑定或在线撤销。

定时任务要求 Obsidian 和插件保持运行。已错过的单次任务可手动重新执行。自动处理权限默认关闭。启用后，插件可以为后台任务选择 OpenCode 的允许权限。建议先用示例笔记核对目标文件和写入模式。

## 隐私、网络与文件访问

- 插件通过本机 HTTP 和 SSE 与 OpenCode 通信。聊天提示词、引用和任务内容会交给 OpenCode，OpenCode 可能将这些数据发给配置的模型提供商。
- 插件按照设置读取模板、Skills 和附件。库外 Skills 路径会访问笔记库外的文件。使用 Obsidian CLI 或 OpenCode 工具时，应查看对应程序的权限。
- 启用邮件后，插件向配置的 SMTP 服务发送任务通知或测试邮件。插件将 SMTP 配置和激活码保存在 `data.json` 中，请按凭据文件保护。
- 插件没有客户端遥测，也不会自行安装依赖或更新。社区目录收录后由 Obsidian 提供 GitHub Release 更新。

## 源码与许可证

公开仓库提供可读的运行产物和 Release。源码由独立私有仓库管理，可关联 Obsidian Community Directory GitHub App 供审核及复现构建。发行产物使用 [MIT 许可证](LICENSE)。

<!-- sanrenjz-promotion:start -->

## 👨‍💻 作者信息

**余汉波** - 编程爱好者-量化交易和效率工具开发

- **GitHub**: [@yuhanbo758](https://github.com/yuhanbo758)

- **Email**: yuhanbo@sanrenjz.com

- **Website**: [三人聚智](https://www.sanrenjz.com)

## 🌐 相关链接

- 🏠 [项目主页](https://www.sanrenjz.com)

- 📚 [在线文档](https://docs.sanrenjz.com)（财经、代码和库文档等）

- 🛒 [插件商店](https://shop.sanrenjz.com)（所有程序，包括开源和不开源）


## 联系我们

[联系我们 - 三人聚智-余汉波](https://www.sanrenjz.com/contact_us/)

证券开户（+V：yuhanbo758）：[证券开户免5万0.854，无门槛开量化QMT，送框架策略，支持VIP快速通道，也可开Ptrade | 余汉波 文档](https://docs.sanrenjz.com/article/%E8%AF%81%E5%88%B8%E5%BC%80%E6%88%B7%E5%85%8D5%20%E4%B8%870.854%EF%BC%8C%E6%97%A0%E9%97%A8%E6%A7%9B%E5%BC%80%E9%87%8F%E5%8C%96QMT%EF%BC%8C%E9%80%81%E6%A1%86%E6%9E%B6%E7%AD%96%E7%95%A5%EF%BC%8C%E6%94%AF%E6%8C%81VIP%E5%BF%AB%E9%80%9F%E9%80%9A%E9%81%93%EF%BC%8C%E4%B9%9F%E5%8F%AF%E5%BC%80Ptrade)

三人聚智下载：[sanrenjz - 三人聚智](https://www.sanrenjz.com/sanrenjz/)

codebot 下载：[sanrenjz-codebot - 三人聚智-余汉波](https://www.sanrenjz.com/sanrenjz-codebot/)

![三码合一](https://gdsx.sanrenjz.com/image/sanrenjz_yuhanbolh_yuhanbo758.png?imageSlim&t=1ab9b82c-e220-8022-beff-e265a194292a)

![余汉波打赏码](https://gdsx.sanrenjz.com/image/%E6%89%93%E8%B5%8F%E7%A0%81%E5%90%88%E4%B8%80.png?imageSlim)

## 🙏 致谢

感谢所有为本项目贡献代码和想法的开发者们！

---
**⭐ 如果这个项目对您有帮助，请给它一个 Star！**

<!-- sanrenjz-promotion:end -->
