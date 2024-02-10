---
permalink: import/google-keep
---
Obsidian allows you to easily migrate your notes from Google Keep using the [[Importer|Importer plugin]].

## Export your data from Google Keep

1. Go to [Google Takeout](https://takeout.google.com/settings/takeout) and log into your Google account.
2. Click **Deselect all** in the top right corner.
3. Scroll down and select **Keep** from the list. 
4. Scroll down to the bottom of the page and click **Next step**.
5. On the next screen, click the **Create export** button.
6. Download the `.zip` file once it is available.

## Import your Google Keep data into Obsidian

You will need the official Obsidian [[Importer]] plugin, which you can [install here](obsidian://show-plugin?id=obsidian-importer).

1. Open **Settings**.
2. Go to **Community Plugins** and [install Importer](obsidian://show-plugin?id=obsidian-importer).
3. Enable the Importer plugin.
4. Open the **Importer** plugin using the command palette or ribbon icon.
5. Under **File format** choose **Google Keep (.zip).**
6. Select the location of your `.zip` file.
7. Click **Import** and wait until import is complete.
8. You're done!

### Supported features

- All checklists will import as top-level items because Google Keep doesn't export indentation information.
- Reminders and user assignments on notes will not be imported because these features are not supported by Obsidian.
- All other information should import as a combination of content and tags.

---

中文翻译：
---
permalink: import/google-keep
---
通过[[Importer|Importer插件]]，Obsidian让您可以轻松地从Google Keep迁移您的笔记。

## 从Google Keep导出数据

1. 进入[Google Takeout](https://takeout.google.com/settings/takeout)并登录您的Google账号。
2. 点击右上角的**取消全选**。
3. 滚动页面并从列表中选择**Keep**。
4. 滚动到页面底部，点击**下一步**。
5. 在下一个页面，点击**创建导出**按钮。
6. 一旦文件可用，下载`.zip`文件。

## 将Google Keep数据导入Obsidian

您需要安装官方的Obsidian[[Importer]]插件，您可以[在此处安装](obsidian://show-plugin?id=obsidian-importer)。

1. 打开**设置**。
2. 进入**社区插件**并[安装Importer](obsidian://show-plugin?id=obsidian-importer)。
3. 启用Importer插件。
4. 使用命令面板或工具栏图标打开**Importer**插件。
5. 在**文件格式**下选择**Google Keep (.zip).**
6. 选择您的`.zip`文件位置。
7. 点击**导入**并等待导入完成。
8. 完成！

### 支持的功能

- 所有的清单将作为顶层项目导入，因为Google Keep不导出缩进信息。
- 由于Obsidian不支持这些功能，提醒和用户分配的笔记将不会被导入。
- 所有其他信息应作为内容和标签的组合导入。