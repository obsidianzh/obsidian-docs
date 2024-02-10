---
permalink: import/notion
---
Obsidian allows you to easily migrate your notes from Notion using the [[Importer|Importer plugin]].

## Export your data from Notion

Obsidian uses Notion's HTML export format. You can find Notions's instructions on how to export your entire workspace [on Notion's website](https://www.notion.so/help/export-your-content). Note that you must be a workspace admin to see this option.

1. Go to **Settings & members** at the top of your left-hand sidebar.
2. Select **Settings** in the sidebar of that window.
3. Scroll down and select the **Export all workspace content** button.
4. Under **Export format** select **HTML**.
5. Enable **Include subpages**
6. Enable **Create folders for subpages**
7. You will receive a `.zip` file via email or directly in the browser.

![[notion-export.png#interface]]

## Import your Notion data into Obsidian

You will need the official Obsidian [[Importer]] plugin, which you can [install here](obsidian://show-plugin?id=obsidian-importer).

1. Open **Settings**.
2. Go to **Community Plugins** and [install Importer](obsidian://show-plugin?id=obsidian-importer).
3. Enable the Importer plugin.
4. Open the **Importer** plugin using the command palette or ribbon icon.
5. Under **File format** select **Notion (.zip)**
6. Choose the `.zip` file with Notion files you want to import. *It's recommended to import all your Notion at once so internal links can be reconciled correctly.*
7. _Optionally_, select a folder for the import Your Notion pages and databases will be nested inside this folder.
8. Enable **Save parent pages in subfolders** to keep the Notion structure. *Note that in Notion you can write content in Folders, this is not possible in Obsidian and these pages will be added as a subpage under the folder.*
9. Select **Import** and wait until import is complete
10. You're done!

## Troubleshooting

If you run into issues while importing from Notion:

- Make sure you use **HTML** as the export format in Notion, **not Markdown**.
- If Obsidian appears to freeze during import, disable community plugins and try again.

Run into something else? Search [the Importer repository](https://github.com/obsidianmd/obsidian-importer/issues) to see if others have experienced it.


---

中文翻译：
---
permalink: import/notion
---
使用[[Importer|Importer插件]]，Obsidian允许你轻松将笔记从 Notion 迁移过来。

## 从 Notion 导出数据

Obsidian 使用 Notion 的 HTML 导出格式。你可以在[Notion官网](https://www.notion.so/help/export-your-content)找到导出整个工作区的指南。请注意，你必须是工作区管理员才能看到此选项。

1. 在左侧侧边栏顶部转到**设置与成员**。
2. 在该窗口的侧边栏中选择**设置**。
3. 向下滚动并选择**导出所有工作区内容**按钮。
4. 在**导出格式**下选择**HTML**。
5. 启用**包括子页面**。
6. 启用**为子页面创建文件夹**。
7. 你将通过电子邮件或直接在浏览器中收到一个`.zip`文件。

![[notion-export.png#interface]]

## 将 Notion 数据导入 Obsidian

你需要使用官方的[[Importer]]插件，你可以在[这里安装](obsidian://show-plugin?id=obsidian-importer)。

1. 打开**设置**。
2. 转到**社区插件**并[安装 Importer](obsidian://show-plugin?id=obsidian-importer)。
3. 启用 Importer 插件。
4. 使用命令面板或工具栏图标打开**Importer**插件。
5. 在**文件格式**下选择**Notion（.zip）**。
6. 选择要导入的装有 Notion 文件的`.zip`文件。*建议一次性导入所有 Notion 内容，以便内部链接可以正确对应。*
7. _可选地_，选择一个文件夹进行导入，你的 Notion 页面和数据库将被嵌套在这个文件夹内。
8. 启用**将父页面保存在子文件夹中**以保留 Notion 结构。*请注意，在 Notion 中可以在文件夹中编写内容，而在 Obsidian 中不支持，这些页面将被添加为文件夹下的子页面。*
9. 选择**导入**并等待导入完成。
10. 完成！

## 故障排除

如果在从 Notion 导入时遇到问题：

- 确保在 Notion 中使用**HTML**作为导出格式，而不是 Markdown。
- 如果在导入过程中 Obsidian 出现卡顿，请禁用社区插件后重试。

遇到其他问题？搜索[Importer存储库](https://github.com/obsidianmd/obsidian-importer/issues)看看其他人是否遇到过相同问题。