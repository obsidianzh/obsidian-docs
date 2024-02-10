The Search plugin helps you find files in your vault.

By default, you can find Search in the left sidebar (magnifying glass icon). You can also open Search by pressing `Ctrl+Shift+F` (or `Cmd+Shift+F` on macOS).

- **Search selected text**: If you select text in the editor and open Search with the keyboard shortcut, Search shows you the search results for the selected text.
- **Search recent search terms**: Open Search with an empty search term to list recent search terms. Click any of them to use the search term again.

## Search terms

A search term is the word or phrase that you enter in the search field. Learning how to write search terms effectively can help you quickly find what you're looking for, even in large vaults. Obsidian only searches the contents of notes and canvases.

> [!tip] Searching paths and filenames
> By default, you can only search the paths and filenames of notes and canvases. To search for a path or filename of any file in the vault, use the `path` or `file` operator.

Each word in the search term is matched independently within each file. To search for an exact phrase, surround it with quotes, for example `"star wars"`. To search for quoted text within an exact phrase, you can _escape_ the quotes by adding a backslash (`\`) in front of the quote, for example `"they said \"hello\" to each other"`.

You can control whether to return files that contain _all_ the words in your search term, or _any_ of the words:

- `meeting work` returns files that contain both `meeting` and `work`.
- `meeting OR work` returns files that contain either `meeting` or `work`.

You can even combine the two in the same search term.

- `meeting work OR meetup personal` returns files for work meetings and personal meetups.

You can use parentheses to control the priority of each expression.

- `meeting (work OR meetup) personal` returns files that contain `meeting`, `personal`, and either `work` or `meetup`.

To exclude, or negate, a word from the search results, add a hyphen (`-`) in front of it:

- `meeting -work` returns files that contain `meeting` but not `work`.

You can exclude multiple expressions:

- `meeting -work -meetup` returns files that contain `meeting` but not `work` or `meetup`.

You can exclude a combination of expressions using parentheses:

- `meeting -(work meetup)` returns files that contain `meeting` but not _both_ `work` and `meetup`.

> [!tip] Explain search term
> If you need to troubleshoot a complex search term, you can click **Explain search term** in Search for an explanation of your search term.

## Search operators

Search operators enable more fine-grained search queries to filter your results even more.

Some operators even allow you to add a nested search term within parentheses, for example: `task:(call OR email)`.

| Search operator | Description                                                                                                                                                                                                          |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `file:`         | Find text in filename. Matches any file in the vault.<p/>Example: `file:.jpg` or `file:202209`.                                                                                                                                                     |
| `path:`         | Find text in file path. Matches any file in the vault.<p/>Example: `path:"Daily notes/2022-07"`.                                                                                                                                                    |
| `content:`      | Find text in file content.<p/>Example: `content:"happy cat"`.                                                                                                                                                        |
| `match-case:`   | Case-sensitive match.<p/>Example: `match-case:HappyCat`.                                                                                                                                                             |
| `ignore-case:`  | Case-insensitive match.<p/>Example: `ignore-case:ikea`.                                                                                                                                                              |
| `tag:`          | Find tag in file.<p/>Example: `tag:#work`.<p/>**Note**: Since `tag:` ignores matches in code blocks and in non-Markdown content, it's often faster and more accurate than a normal full-text search for `#work`.     |
| `line:`         | Find matches on the same line.<p/>Example: `line:(mix flour)`.                                                                                                                                                       |
| `block:`        | Find matches in the same block.<p/>Example: `block:(dog cat)`.<p/>**Note**: Since `block:` requires Search to parse the Markdown content in every file, it can cause your search term to take longer time to finish. |
| `section:`      | Find matches in the same section (text between two headings).<p/>Example: `section:(dog cat)`.                                                                                                                         |
| `task:`         | Find matches in a [[Basic formatting syntax#Task lists\|task]] on a block-by-block basis.<p/>Example: `task:call`.                                                                                                          |
| `task-todo:`    | Find matches in an *uncompleted* [[Basic formatting syntax#Task lists\|task]] on a block-by-block basis.<p/>Example: `task-todo:call`.                                                                                      |
| `task-done:`    | Find matches in a *completed* [[Basic formatting syntax#Task lists\|task]] on a block-by-block basis.<p/>Example: `task-done:call`.                                                                                         |

## Search properties

You can use data stored in [[Properties]] in your search terms.

Use brackets around a property name `[property]` to return files with that property:

- `[aliases]` returns files that contain the `aliases` property
  
Use brackets and a colon `[property:value]` to return files with that property and value:

- `[aliases:Name]` returns files where the `aliases` property value is `Name`

Both property and value allow sub-queries, such as parentheses for grouping, the `OR` operator, double-quotes for exact matching, and regex.

- Example: `[status:Draft OR Published]` to find returns files where the `status` property value is `Draft` or `Published`

## Change case sensitivity

By default, search terms are not case sensitive. If you want to search for the exact case of your search term, click **Match case** ("Aa" icon) inside the search bar.

This setting can be toggled. If **Match case** icon is highlighted, that means you’re currently doing a case sensitive search.

## Change result sort order

1. Enter a [[#Search terms|search term]].
2. Under the search field, click on the dropdown on the right.
3. Select the sort order you want. Default is "File name (A to Z)".

The following options are available:

- File name (A to Z)
- File name (Z to A)
- Modified time (new to old)
- Modified time (old to new)
- Created time (new to old)
- Created time (old to new)

## Copy search results

1. Enter a [[#Search terms|search term]].
2. Under the search field, select the three dots icon next to the number of results.
3. Select **Copy search results**.

## Use regular expressions

A regular expression is a set of characters that describe a text pattern. To use regular expressions in your search term, surround the expression with forward slashes (`/`).

- `/\d{4}-\d{2}-\d{2}/` matches an ISO 8601 date, such as 2022-01-01.

You can even combine regular expressions with search operators:

- `path:/\d{4}-\d{2}-\d{2}/` returns files with a date in the file path.

For more information on how to write regular expressions, refer to [Regular expressions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions)

> [!note]
> Regular expressions come in different flavors that may look different from each other. Obsidian uses JavaScript-flavored regular expressions.

## Configure search settings

To configure Search, click on **Search settings** (three rows of switches icon) on the right side of the search bar to see the toggles.

| Setting                 | Description                                                                 |
|-------------------------|-----------------------------------------------------------------------------|
| **Explain search term** | Breaks down the search terms and explains it in plain text.                 |
| **Collapse results**    | Toggles whether to show the search context.                                 |
| **Show more context**   | Expands the search result to show more text around the match.               |

## Embed search results in a note

To embed search results in a note, add a `query` code block:

<pre><code>```query
embed OR search
```</code></pre>

For example:

> [!note]
> [[Introduction to Obsidian Publish|Obsidian Publish]] doesn't support embedded search results. To see the example, open Obsidian Help locally inside Obsidian.

```query
embed OR search
```


---

中文翻译：
搜索插件帮助你在仓库中查找文件。

默认情况下，你可以在左侧边栏（放大镜图标）找到搜索。你也可以通过按下 `Ctrl+Shift+F`（或 macOS 上的 `Cmd+Shift+F`）来打开搜索。

- **搜索所选文本**：如果你在编辑器中选择文本并使用键盘快捷键打开搜索，搜索会显示所选文本的搜索结果。
- **搜索最近的搜索词**：使用空搜索词打开搜索以列出最近的搜索词。点击其中任何一个以再次使用该搜索词。

## 搜索词

搜索词是你在搜索字段中输入的单词或短语。学会如何有效编写搜索词可以帮助你快速找到你需要的内容，即使在大型仓库中也能如此。Obsidian只搜索笔记和画布的内容。

> [!提示] 搜索路径和文件名
> 默认情况下，你只能搜索笔记和画布的路径和文件名。要搜索仓库中任何文件的路径或文件名，请使用 `path` 或 `file` 运算符。

搜索词中的每个单词在每个文件中独立匹配。要搜索精确短语，请用引号括起来，例如 `"星球大战"`。要在精确短语内搜索带引号的文本，可以通过在引号前添加反斜杠（`\`）来 _转义_ 引号，例如 `"他们说\"你好\""`。

你可以控制是否返回包含搜索词中所有单词或任意单词的文件：

- `会议 工作` 返回包含 `会议` 和 `工作` 的文件。
- `会议 OR 工作` 返回包含 `会议` 或 `工作` 的文件。

你甚至可以将两者结合在同一个搜索词中。

- `会议 工作 OR 聚会 个人` 返回工作会议和个人聚会的文件。

你可以使用括号来控制每个表达式的优先级。

- `会议 (工作 OR 聚会) 个人` 返回包含 `会议`、`个人` 和 `工作` 或 `聚会` 的文件。

要从搜索结果中排除或否定一个单词，可以在单词前加上连字符（`-`）：

- `会议 -工作` 返回包含 `会议` 但不包含 `工作` 的文件。

你可以排除多个表达式：

- `会议 -工作 -聚会` 返回包含 `会议` 但不包含 `工作` 或 `聚会` 的文件。

你可以使用括号排除表达式的组合：

- `会议 -(工作 聚会)` 返回包含 `会议` 但不包含 _同时_ 包含 `工作` 和 `聚会` 的文件。

> [!提示] 解释搜索词
> 如果你需要解决复杂搜索词的问题，可以点击搜索中的 **解释搜索词** 以获取搜索词的解释。

## 搜索运算符

搜索运算符使得能够更精细地搜索查询以进一步筛选结果。

一些运算符甚至允许在括号内添加嵌套搜索词，例如：`task:(电话 OR 邮件)`。

| 搜索运算符  | 描述                                                                                                                                                 |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `file:`     | 在文件名中查找文本。匹配仓库中的任何文件。<p/>示例：`file:.jpg` 或 `file:202209`。                                                                                     |
| `path:`     | 在文件路径中查找文本。匹配仓库中的任何文件。<p/>示例：`path:"日常笔记/2022-07"`。                                                                                          |
| `content:`  | 在文件内容中查找文本。<p/>示例：`content:"快乐的猫"`。                                                                                                      |
| `match-case:` | 区分大小写的匹配。<p/>示例：`match-case:快乐的猫`。                                                                                                    |
| `ignore-case:` | 不区分大小写的匹配。<p/>示例：`ignore-case:宜家`。                                                                                                     |
| `tag:`      | 在文件中查找标签。<p/>示例：`tag:#工作`。<p/>**注意**：由于 `tag:` 忽略代码块和非 Markdown 内容中的匹配，因此它通常比普通全文搜索的速度更快且更准确。             |
| `line:`     | 在同一行上查找匹配项。<p/>示例：`line:(混合面粉)`。                                                                                                      |
| `block:`    | 在同一块中查找匹配项。<p/>示例：`block:(狗 猫)`。<p/>**注意**：由于 `block:` 需要搜索解析每个文件中的 Markdown 内容，这可能导致你的搜索词需要更长的时间来完成。           |
| `section:`  | 在同一节（两个标题之间的文本）中查找匹配项。<p/>示例：`section:(狗 猫)`。                                                                                         |
| `task:`     | 在块级基础上查找[[基本格式语法#任务列表\|任务]]中的匹配项。<p/>示例：`task:电话`。                                                                                      |
| `task-todo:` | 在块级基础上查找*未完成*的[[基本格式语法#任务列表\|任务]]中的匹配项。<p/>示例：`task-todo:电话`。                                                                      |
| `task-done:` | 在块级基础上查找*已完成*的[[基本格式语法#任务列表\|任务]]中的匹配项。<p/>示例：`task-done:电话`。                                                                     |

## 搜索属性

你可以在搜索词中使用存储在[[Properties]]中的数据。

用方括号括起属性名称 `[属性]` 以返回具有该属性的文件：

- `[别名]` 返回包含 `别名` 属性的文件

用方括号和冒号 `[属性:值]` 来返回具有该属性和值的文件：

- `[别名:名称]` 返回 `别名` 属性值为 `名称` 的文件

属性和值都允许子查询，例如使用括号进行分组，`OR` 运算符，双引号进行精确匹配，以及正则表达式。

- 示例：`[状态:草稿 OR 已发布]` 以返回 `状态` 属性值为 `草稿` 或 `已发布` 的文件

## 更改大小写敏感度

默认情况下，搜索词不区分大小写。如果要搜索与搜索词的确切大小写匹配项，点击搜索栏内的 **匹配大小写**（"Aa" 图标）。

此设置可以切换。如果 **匹配大小写** 图标被突出显示，那意味着你当前正在进行大小写敏感的搜索。

## 更改结果排序顺序

1. 输入[[#搜索词|搜索词]]。
2. 在搜索字段下，点击右侧的下拉菜单。
3. 选择你想要的排序顺序。默认为"文件名（A 到 Z）"。

以下选项可用：

- 文件名（A 到 Z）
- 文件名（Z 到 A）
- 修改时间（新到旧）
- 修改时间（旧到新）
- 创建时间（新到旧）
- 创建时间（旧到新）

## 复制搜索结果

1. 输入[[#搜索词|搜索词]]。
2. 在搜索字段下，选择结果数量旁边的三个点图标。
3. 选择 **复制搜索结果**。

## 使用正则表达式

正则表达式是描述文本模式的一组字符。要在搜索词中使用正则表达式，请用斜杠（`/`）括起表达式。

- `/\\d{4}-\\d{2}-\\d{2}/` 匹配 ISO 8601 日期，例如 2022-01-01。

你甚至可以将正则表达式与搜索运算符结合使用：

- `path:/\\d{4}-\\d{2}-\\d{2}/` 返回文件路径中带有日期的文件。

有关如何编写正则表达式的更多信息，请参阅[正则表达式](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions)。

> [!注意]
> 正则表达式有不同的风格，可能看起来不同。Obsidian 使用 JavaScript 风格的正则表达式。

## 配置搜索设置

要配置搜索，点击搜索栏右侧的 **搜索设置**（三排开关图标）以查看切换按钮。

| 设置                     | 描述                                                                 |
|-------------------------|---------------------------------------------------------------------|
| **解释搜索词**           | 分解搜索词并用简单文本解释。                                             |
| **折叠结果**             | 切换是否显示搜索上下文。                                                  |
| **显示更多上下文**       | 展开搜索结果以显示匹配周围更多文本。                                        |

## 在笔记中嵌入搜索结果

要在笔记中嵌入搜索结果，添加一个 `query` 代码块：

<pre><code>```query
嵌入 OR 搜索
```</code></pre>

例如：

> [!提示]
> [[了解 Obsidian Publish|Obsidian Publish]] 不支持嵌入式搜索结果。要查看示例，请在 Obsidian 中本地打开 Obsidian 帮助。

```query
嵌入 OR 搜索
```