Note composer lets you merge two notes or extract part of a note into a new note.

## Merge notes

Merging notes adds a note to another and removes the first one. Note composer updates all links to reference the merged note.

When you select the note to merge into, you can choose between the following methods:

- `Enter`: Adds the source note at the _end_ to the destination note.
- `Shift+Enter`: Adds the source note at the _start_ of the destination note.
- `Ctrl+Enter` (or `Cmd+Enter` on macOS): Creates a new note with the content of the source note.

To merge the active note with another note in your vault:

**File explorer**

1. In the File explorer, right-click the note you want to merge.
2. Click **Merge entire file with...**.
3. Select the note you want to merge into.
4. Click **Merge** to confirm.

**Command palette**

1. Open the [[Command palette]].
2. Select **Note composer: Merge current file with another file...**.
3. Select the note you want to merge into.
4. Click **Merge** to confirm.

> [!tip]
> By default, Note composer asks you to confirm when merging notes. If you disable the confirmation, and you merge a note by mistake, you can still recover it with the [[File recovery]] plugin.

## Extract note

When you select the note to extract the selection into, you can choose between the following methods:

- `Enter`: Adds the selected text at the _end_ to the destination note.
- `Shift+Enter`: Adds the selected text at the _start_ of the destination note.
- `Ctrl+Enter` (or `Cmd+Enter` on macOS): Creates a new note with the selected text.

To extract text into a new note:

**Editor**

1. While in the **Editing view**, select the text you want to extract.
2. Right-click the selected text.
3. Click **Extract current selection...**.
4. Select the note you want to extract into.

**Command palette**

1. While in the **Editing view**, select the text you want to extract.
2. Open the [[Command palette]].
3. Select **Note composer: Extract current selection...**.
4. Select the note you want to extract into.

> [!tip]
> By default, Note composer replaces the extracted text with a link to the destination note. Under settings, you can also change to instead [[Embed files|embed]] the destination note, or to leave nothing behind.

## Template file

By configuring a template, you can customize the content before you add it to the new note. To use a template, enter a **Template file location** in the plugin settings.

The template can contain the following variables:

| Variable          | Description                                                                                                                                              |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `{{content}}`     | The content to merge, or the extracted text selection. If you don't include this variable, Note composer adds the content at the bottom of the template. |
| `{{fromTitle}}`   | Name of the source note.                                                                                                                                 |
| `{{newTitle}}`    | Name of the destination note. For example, to add the file name as a heading at the top of the file.                                                     |
| `{{date:FORMAT}}` | Creation date of the new note. For example, `{{date:YYYY-MM-DD}}`.                                                                                       |


---

中文翻译：
笔记合并功能让你可以将两个笔记合并，或者从一个笔记中提取部分内容创建新笔记。

## 合并笔记

合并笔记会将一个笔记添加到另一个笔记中，并删除第一个笔记。笔记合并器会更新所有链接以引用合并后的笔记。

当选择要合并的目标笔记时，你可以选择以下方法之一：

- `Enter`：将源笔记添加到目标笔记的 _末尾_。
- `Shift+Enter`：将源笔记添加到目标笔记的 _开头_。
- `Ctrl+Enter`（或 macOS 上的 `Cmd+Enter`）：创建一个包含源笔记内容的新笔记。

要将活动笔记与仓库中的另一个笔记合并：

**文件浏览器**

1. 在文件浏览器中，右键点击要合并的笔记。
2. 点击 **与另一个文件合并**。
3. 选择要合并到的笔记。
4. 点击 **合并** 确认。

**命令面板**

1. 打开[[Command palette|命令面板]]。
2. 选择 **Note composer: 合并当前文件与另一个文件...**。
3. 选择要合并到的笔记。
4. 点击 **合并** 确认。

> [!提示]
> 默认情况下，笔记合并器在合并笔记时会要求确认。如果你禁用了确认功能，并且不小心合并了一个笔记，你仍可以使用[[文件恢复]]插件将其恢复。

## 提取笔记

当选择要提取内容的笔记时，你可以选择以下方法之一：

- `Enter`：将所选文本添加到目标笔记的 _末尾_。
- `Shift+Enter`：将所选文本添加到目标笔记的 _开头_。
- `Ctrl+Enter`（或 macOS 上的 `Cmd+Enter`）：创建一个包含所选文本的新笔记。

要将文本提取到新笔记中：

**编辑器**

1. 在**编辑视图**中，选择要提取的文本。
2. 右键点击所选文本。
3. 点击 **提取当前选择...**。
4. 选择要提取到的笔记。

**命令面板**

1. 在**编辑视图**中，选择要提取的文本。
2. 打开[[Command palette|命令面板]]。
3. 选择 **Note composer: 提取当前选择...**。
4. 选择要提取到的笔记。

> [!提示]
> 默认情况下，笔记合并器会用目标笔记的链接替换提取的文本。在设置中，你还可以选择改为[[Embed files|嵌入]]目标笔记，或者不留任何痕迹。

## 模板文件

通过配置模板，你可以在将内容添加到新笔记前自定义内容。要使用模板，请在插件设置中输入**模板文件位置**。

模板可以包含以下变量：

| 变量              | 描述                                                                                                                                                   |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `{{content}}`     | 要合并的内容，或提取的文本选择。如果不包含此变量，笔记合并器会将内容添加到模板底部。                                                                  |
| `{{fromTitle}}`   | 源笔记的名称。                                                                                                                                          |
| `{{newTitle}}`    | 目标笔记的名称。例如，将文件名作为文件顶部的标题添加。                                                                                                 |
| `{{date:FORMAT}}` | 新笔记的创建日期。例如，`{{date:YYYY-MM-DD}}`。                                                                                                       |