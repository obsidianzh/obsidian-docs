Daily notes opens a note based on today's date, or creates it if it doesn't exist. Use daily notes to create journals, to-do lists, or daily logs for things you discovered during the day.

To open today's daily note, either:

- Click **Open today's daily note** (calendar with checkmark icon) in the [[Ribbon|ribbon]].
- Run **Open today's daily note** from the [[Command palette]].
- [[Hotkeys#Setting hotkeys|Use a hotkey]] for the **Open today's daily note** command.

By default, Obsidian creates a new empty note named after today's date in the YYYY-MM-DD format.

> [!tip] If you prefer to have your daily notes in a separate folder, you can set the <u>New file location</u> under plugin options to change where Obsidian creates new daily notes.

> [!example]- Automatic subfolders
> You can automatically organize your daily notes into folders using the **Date format** feature.
> 
> For instance, if you set the date format as `YYYY/MMMM/YYYY-MMM-DD`, your notes will be created as `2023/January/2023-Jan-01`. 
> 
> You can explore more formatting options on the [momentJS](https://momentjs.com/docs/#/displaying/format/) documentation site.

## Create a daily note from template

If your daily notes have the same structure, you can use a [[Templates|template]] to add pre-defined content to your daily notes when you create them.

1. Create a new note named "Daily template" with the following text (or whatever makes sense to you!):

   ```md
   # {{date:YYYY-MM-DD}}

   ## Tasks

   - [ ]
   ```

2. Open **Settings**.
3. In the sidebar, click **Daily notes** under **Plugin options**.
4. In the text box next to **Template file location**, select the "Daily template" note.

Obsidian uses the template the next time you create a new daily note.

## Daily notes and properties

When the Daily notes plugin is activated and a date property is present within any note, Obsidian will automatically attempt to generate a link to the daily note for that specific day. For instance, if a note titled `example.md` includes a date property like `2023-01-01`, this date will transform into a clickable link in the [[Edit and preview Markdown#Live Preview|live preview]] section.

![[daily-notes-and-date-properties.png#interface|300]]
^daily-notes-date


---

中文翻译：
每日笔记会根据今天的日期打开一个笔记，如果不存在则会创建一个新的。可以使用每日笔记创建日记、待办事项列表，或者记录当天发现的事情。

要打开今天的每日笔记，可以：

- 点击[[Ribbon|工具栏]]中的**打开今日每日笔记**（带有日历和勾选图标）。
- 从[[命令面板]]中运行**打开今日每日笔记**。
- [[快捷键#设置快捷键|使用快捷键]]执行**打开今日每日笔记**命令。

默认情况下，Obsidian会按照YYYY-MM-DD格式创建一个以当天日期命名的空笔记。

> [!提示] 如果你希望将每日笔记保存在单独的文件夹中，可以在插件选项下设置<u>新文件位置</u>来更改 Obsidian 创建新每日笔记的位置。

> [!示例]- 自动子文件夹
> 你可以使用**日期格式**功能自动将每日笔记整理到文件夹中。
> 
> 例如，如果将日期格式设置为`YYYY/MMMM/YYYY-MMM-DD`，你的笔记将被创建为`2023/January/2023-Jan-01`。
> 
> 你可以在[momentJS](https://momentjs.com/docs/#/displaying/format/)文档网站上探索更多格式选项。

## 使用模板创建每日笔记

如果你的每日笔记具有相同的结构，可以使用[[模板|template]]在创建笔记时向每日笔记添加预定义内容。

1. 创建一个名为“每日模板”的新笔记，并输入以下文本（或任何你觉得合适的内容）：

   ```md
   # {{date:YYYY-MM-DD}}

   ## 任务

   - [ ]
   ```

2. 打开**设置**。
3. 在侧边栏中，点击**插件选项**下的**每日笔记**。
4. 在**模板文件位置**旁边的文本框中，选择“每日模板”笔记。

下次创建新的每日笔记时，Obsidian会使用该模板。

## 每日笔记和属性

当启用每日笔记插件并在任何笔记中存在日期属性时，Obsidian会自动尝试为该特定日期生成一个到每日笔记的链接。例如，如果一个名为`example.md`的笔记包含日期属性`2023-01-01`，这个日期将会在[[编辑和预览 Markdown#实时预览|实时预览]]部分转换为可点击的链接。

![[daily-notes-and-date-properties.png#interface|300]]
^每日笔记日期