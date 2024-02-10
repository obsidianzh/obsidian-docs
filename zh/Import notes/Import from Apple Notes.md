---
permalink: import/apple-notes
---
Obsidian allows you to easily migrate your notes from Apple Notes using the [[Importer|Importer plugin]]. Currently, it only supports importing from Apple Notes on your macOS desktop. 


## Import Apple Notes data into Obsidian

You will need the official Obsidian [[Importer]] plugin, which you can [install here](obsidian://show-plugin?id=obsidian-importer).

1. Open **Settings**.
2. Go to **Community Plugins** and [install Importer](obsidian://show-plugin?id=obsidian-importer).
3. Enable the Importer plugin.
4. Open the **Importer** plugin using the command palette or ribbon icon.
5. Under **File format** choose **Apple Notes**.
6. Click **Import**.
7. Click **Open** on the popup that appears titled `Select the "group.com.apple.notes" folder to allow Obsidian to read Apple Notes data`.
8. Wait until import is complete. 
9. You're done!

## Supported content

The Obsidian Importer plugin supports virtually all Apple Notes content types. This includes tables, images, drawings, scans, PDFs, and links introduced in iOS 17.

> [!Warning]
> Password-protected notes are encrypted by Apple, so must be unlocked before importing them. Any locked notes will be skipped.

### Scans

Apple stores scans in a variety of formats depending on how they were created. To preseve the original data, this means they'll be exported differently.

* Scans created or viewed on older versions of macOS or iOS will be exported as a series of uncropped images.
* Scans created or viewed on newer versions of macOS or iOS will usually be exported as cropped images.
* Scans that have been edited using the features introduced in iOS 17 will usually be exported as PDFs.

## Alternate export methods

Apple does not provide a native option to export your notes. However several third-party tools exist such as [Exporter](https://apps.apple.com/us/app/exporter/id1099120373) by Chintan Ghate. Please be aware that most tools are limited in what data they will export from Apple Notes and might not provide the most compatible output data. These tools work best if your Apple Notes are primarily text-only, and have few attachments or special features such as drawings and scans.

Depending on the tool you used, the export may be in Markdown format or HTML format. Follow instructions based on the file format you exported to: 

- [[Import HTML files]]
- [[Import Markdown files]]


---

中文翻译：
---
permalink: import/apple-notes
---
Obsidian允许你使用[[Importer|Importer插件]]轻松迁移你的Apple Notes。目前，该插件仅支持在 macOS 桌面端从 Apple Notes 迁移。

## 将 Apple Notes 数据导入 Obsidian

你需要安装官方的Obsidian [[Importer]]插件，你可以[在这里安装](obsidian://show-plugin?id=obsidian-importer)。

1. 打开 **设置**。
2. 进入 **社区插件** 并[安装 Importer](obsidian://show-plugin?id=obsidian-importer)。
3. 启用 Importer 插件。
4. 使用命令面板或工具栏图标打开 **Importer** 插件。
5. 在 **文件格式** 下选择 **Apple Notes**。
6. 点击 **导入**。
7. 在弹出的标题为 `选择 "group.com.apple.notes" 文件夹以允许 Obsidian 读取 Apple Notes 数据` 的窗口中点击 **打开**。
8. 等待导入完成。
9. 完成！

## 支持的内容

Obsidian Importer 插件几乎支持所有 Apple Notes 的内容类型。这包括表格、图片、绘画、扫描、PDF 以及 iOS 17 中引入的链接。

> [!警告]
> 受密码保护的笔记由 Apple 加密，因此在导入之前必须解锁它们。任何受锁定的笔记将被跳过。

### 扫描

根据创建方式的不同，Apple 以各种格式存储扫描。为了保留原始数据，这意味着它们将以不同的方式导出。

* 在旧版本的 macOS 或 iOS 上创建或查看的扫描将被导出为一系列未裁剪的图像。
* 在新版本的 macOS 或 iOS 上创建或查看的扫描通常将被导出为裁剪后的图像。
* 使用 iOS 17 中引入的功能编辑过的扫描通常将被导出为 PDF。

## 备选的导出方法

Apple 没有提供原生选项来导出你的笔记。但是存在一些第三方工具，例如 Chintan Ghate 开发的 [Exporter](https://apps.apple.com/us/app/exporter/id1099120373)。请注意，大多数工具在从 Apple Notes 导出数据时存在限制，并且可能无法提供最兼容的输出数据。如果你的 Apple Notes 主要是纯文本，并且附件或特殊功能如绘画和扫描较少，这些工具效果最好。

根据你使用的工具，导出可能是 Markdown 格式或 HTML 格式。根据导出的文件格式，按照相应的说明进行操作：

- [[导入 HTML 文件]]
- [[导入 Markdown 文件]]