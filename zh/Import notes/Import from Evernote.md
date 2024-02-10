---
permalink: import/evernote
---
Obsidian allows you to easily migrate your notes from Evernote using the [[Importer|Importer plugin]].

## Export your data from Evernote

Obsidian uses Evernote's export format `.enex` files.

You can find Evernote's instructions for exporting your data [on Evenote's website](https://help.evernote.com/hc/en-us/articles/209005557-Export-notes-and-notebooks-as-ENEX-or-HTML). This method allows you to export entire notebooks in the desktop client.

1. Go to the Notebooks screen.
2. Click on **More actions** (`•••` icon) and choose **Export Notebook...**
3. Select **ENEX** as the file format.
3. Choose a location for your exported `.enex` file.

## Import your Evernote data into Obsidian

You will need the official Obsidian [[Importer]] plugin, which you can [install here](obsidian://show-plugin?id=obsidian-importer).

1. Open **Settings**.
2. Go to **Community Plugins** and [install Importer](obsidian://show-plugin?id=obsidian-importer).
3. Enable the Importer plugin.
4. Open the **Importer** plugin using the command palette or ribbon icon.
5. Under **File format** choose **Evernote (.enex)**.
6. Select the location of your Evernote backup file.
7. Click **Import** and wait until import is complete.
8. You're done!

## Advanced import options

### Maintain tag hierarchy

Evernote export does not keep the tag hierarchy. To keep your tag hierarchy, you can "flatten" tags separated by "/". For example, assuming that you have the following tag structure: 

```
ParentTag
    ChildTag
```

What you need to do to keep tags related in Obsidian is:

1. Right-click on the ChildTag.
2. Select "Rename."
3. Rename it as `ParentTag/ChildTag`.

### Handling notebook stacks

Since the export process is limited to single notebooks, the default export file lacks information about notebook stacks. However, the importer can recognize patterns in the enex file name to recreate notebook stacks as folders.

Assuming that you have a notebook called ```NotebookA``` in a stack called ```Stack1```, you can recreate a notebook stack by renaming the enex file to ```Stack1@@@NotebookA```.

This results in the converted notes being generated within the Stack1/NotebookA folder.

### More options

For more advanced import options from Evernote you can also try [importing via Yarle](https://github.com/akosbalasko/yarle).


---

中文翻译：
---
permalink: import/evernote
---
使用[[Importer|Importer插件]]，Obsidian可以帮助你轻松将Evernote中的笔记迁移至Obsidian。

## 从Evernote导出数据

Obsidian使用Evernote的导出格式`.enex`文件。

你可以在[Evernote官网](https://help.evernote.com/hc/en-us/articles/209005557-Export-notes-and-notebooks-as-ENEX-or-HTML)找到Evernote导出数据的说明。这种方法允许你在桌面客户端中导出整个笔记本。

1. 进入笔记本界面。
2. 点击**更多操作**（`•••`图标），选择**导出笔记本...**。
3. 选择**ENEX**作为文件格式。
4. 选择导出`.enex`文件的位置。

## 将Evernote数据导入Obsidian

你需要使用官方的Obsidian[[Importer]]插件，你可以在这里[安装它](obsidian://show-plugin?id=obsidian-importer)。

1. 打开**设置**。
2. 进入**社区插件**，[安装Importer](obsidian://show-plugin?id=obsidian-importer)。
3. 启用Importer插件。
4. 使用命令面板或工具栏图标打开**Importer**插件。
5. 在**文件格式**下选择**Evernote (.enex)**。
6. 选择你的Evernote备份文件位置。
7. 点击**导入**，等待导入完成。
8. 完成！

## 高级导入选项

### 保留标签层次结构

Evernote导出文件不会保留标签的层次结构。为了保留标签层次结构，在标签之间用“/”分隔。例如，假设你有以下标签结构：

```
父标签
    子标签
```

为了在Obsidian中保留标签关系，你需要：

1. 右键点击子标签。
2. 选择“重命名”。
3. 将其重命名为`父标签/子标签`。

### 处理笔记本堆叠

由于导出过程仅限于单个笔记本，导出文件缺乏有关笔记本堆叠的信息。不过，Importer可以识别enex文件名中的模式，以重新创建笔记本堆叠作为文件夹。

假设你有一个名为```笔记本A```的笔记本，它位于名为```堆叠1```的堆叠中，你可以通过将enex文件重命名为```堆叠1@@@笔记本A```来重新创建笔记本堆叠。

这样转换后的笔记会生成在Stack1/NotebookA文件夹内。

### 更多选项

如果你想要更多来自Evernote的高级导入选项，你也可以尝试[通过Yarle导入](https://github.com/akosbalasko/yarle)。