Format converter lets you convert Markdown from other applications to Obsidian format.

> [!warning]
> Format converter converts your entire vault based on your settings. Back up your notes before you perform the conversion.

To convert all notes in your vault:

1. In the ribbon, click **Open format converter** (ones and zeros icon).
2. Enable the formats you want to convert.
3. Click **Start conversion**.

For more information, refer to [[Basic formatting syntax]].

## Supported formats

| Application   | From                  | To                                                              |
|---------------|-----------------------|-----------------------------------------------------------------|
| Roam Research | `#tag` and `#[[tag]]` | `[[tag]]`                                                       |
| Roam Research | `^^highlight^^`       | `==highlight==`                                                 |
| Roam Research | `{{[[TODO]]}}`        | `[ ]`                                                           |
| Bear          | `::highlight::`       | `==highlight==`                                                 |
| Zettelkasten  | `[[UID]]`             | `[[UID File Name]]` (full link)                                 |
| Zettelkasten  | `[[UID]]`             | <code>\[\[UID File Name&#124;File Name\]\]</code> (pretty link) |



---

中文翻译：
格式转换器可以将其他应用程序中的 Markdown 转换为 Obsidian 格式。

> [!警告]
> 格式转换器会根据您的设置转换整个仓库。在执行转换操作前，请备份您的笔记。

要转换仓库中的所有笔记：

1. 在工具栏中，点击**打开格式转换器**（一串数字和零的图标）。
2. 启用您想要转换的格式。
3. 点击**开始转换**。

如需更多信息，请参考[[基本格式语法]]。

## 支持的格式

| 应用程序       | 转换前                | 转换后                                                          |
|---------------|-----------------------|-----------------------------------------------------------------|
| Roam Research | `#标签` 和 `#[[标签]]` | `[[标签]]`                                                       |
| Roam Research | `^^高亮^^`             | `==高亮==`                                                      |
| Roam Research | `{{[[待办]]}}`         | `[ ]`                                                           |
| Bear          | `::高亮::`             | `==高亮==`                                                      |
| Zettelkasten  | `[[UID]]`             | `[[UID 文件名]]`（完整链接）                                    |
| Zettelkasten  | `[[UID]]`             | <code>\[\[UID 文件名&#124;文件名\]\]</code>（漂亮链接）           |