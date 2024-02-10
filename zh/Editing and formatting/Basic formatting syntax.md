---
aliases:
  - How to/Format your notes
  - Markdown
---

Learn how to apply basic formatting to your notes, using [Markdown](https://daringfireball.net/projects/markdown/). For more advanced formatting syntax, refer to [[Advanced formatting syntax]].

## Paragraphs

To create paragraphs, use a blank line to separate one or more lines of text.

```
This is a paragraph.

This is another paragraph.
```

> [!note]- Multiple blank spaces
> Multiple adjacent blank spaces in and between paragraphs collapse to a single space when displaying a note in [[Edit and preview Markdown#Editor views|Reading view]] and on [[Introduction to Obsidian Publish|Obsidian Publish]] sites.
> 
> ```md
> Multiple          adjacent          spaces
> 
> 
> 
> and multiple newlines between paragraphs.
> ```
> 
> > Multiple          adjacent          spaces
> > 
> > 
> > 
> > and multiple newlines between paragraphs.
> 
> If you want to add multiple spaces, you can add `&nbsp;` (blank space) and `<br>` (newline) to your note.

## Headings

To create a heading, add up to six `#` symbols before your heading text. The number of `#` symbols determines the size of the heading.

```md
# This is a heading 1
## This is a heading 2
### This is a heading 3
#### This is a heading 4
##### This is a heading 5
###### This is a heading 6
```

%% These headings use HTML to avoid cluttering the Outline/Table of contents %%
<h1>This is a heading 1</h1>
<h2>This is a heading 2</h2>
<h3>This is a heading 3</h3>
<h4>This is a heading 4</h4>
<h5>This is a heading 5</h5>
<h6>This is a heading 6</h6>

## Bold, italics, highlights

Text formatting can also be applied using [[Editing shortcuts]].

| Style | Syntax | Example | Output |
|-|-|-|-|
| Bold | `** **` or `__ __` | `**Bold text**` | **Bold text** |
| Italic | `* *` or `_ _`  | `*Italic text*` | *Italic text* |
| Strikethrough | `~~ ~~` |  `~~Striked out text~~` | ~~Striked out text~~ |
| Highlight | `== ==` |  `==Highlighted text==` | ==Highlighted text== |
| Bold and nested italic | `** **` and `_ _`  | `**Bold text and _nested italic_ text**` | **Bold text and _nested italic_ text** |
| Bold and italic | `*** ***` or `___ ___` |  `***Bold and italic text***` | ***Bold and italic text*** |

## Internal links

Obsidian supports two formats for [[internal links]] between notes:

- Wikilink: `[[Three laws of motion]]`
- Markdown: `[Three laws of motion](Three%20laws%20of%20motion.md)`

## External links

If you want to link to an external URL, you can create an inline link by surrounding the link text in brackets (`[ ]`), and then the URL in parentheses (`( )`).

```md
[Obsidian Help](https://help.obsidian.md)
```

[Obsidian Help](https://help.obsidian.md)

You can also create external links to files in other vaults, by linking to an [[Obsidian URI|Obsidian URI]].

```md
[Note](obsidian://open?vault=MainVault&file=Note.md)
```

### Escape blank spaces in links

If your URL contains blank spaces, you must escape them by replacing them with `%20`.

```md
[My Note](obsidian://open?vault=MainVault&file=My%20Note.md)
```

You can also escape the URL by wrapping it with angled brackets (`< >`).

```md
[My Note](<obsidian://open?vault=MainVault&file=My Note.md>)
```

## External images

You can add images with external URLs, by adding a `!` symbol before an [[#External links|external link]].

```md
![Engelbart](https://history-computer.com/ModernComputer/Basis/images/Engelbart.jpg)
```

![Engelbart](https://history-computer.com/ModernComputer/Basis/images/Engelbart.jpg)

You can change the image dimensions, by adding `|640x480` to the link destination, where 640 is the width and 480 is the height.

```md
![Engelbart|100x145](https://history-computer.com/ModernComputer/Basis/images/Engelbart.jpg)
```

If you only specify the width, the image scales according to its original aspect ratio. For example:

```md
![Engelbart|100](https://history-computer.com/ModernComputer/Basis/images/Engelbart.jpg)
```

> [!tip]
> If you want to add an image from inside your vault, you can also [[Embed files#Embed an image in a note|embed an image in a note]].

## Quotes

You can quote text by adding a `>` symbols before the text.

```md
> Human beings face ever more complex and urgent problems, and their effectiveness in dealing with these problems is a matter that is critical to the stability and continued progress of society.

\- Doug Engelbart, 1961
```

> Human beings face ever more complex and urgent problems, and their effectiveness in dealing with these problems is a matter that is critical to the stability and continued progress of society.

\- Doug Engelbart, 1961

> [!tip]
> You can turn your quote into a [[Callouts|callout]] by adding `[!info]` as the first line in a quote.

## Lists

You can create an unordered list by adding a `-`, `*`, or `+` before the text.

```md
- First list item
- Second list item
- Third list item
```

- First list item
- Second list item
- Third list item

To create an ordered list, start each line with a number followed by a `.` symbol.

```md
1. First list item
2. Second list item
3. Third list item
```

1. First list item
2. Second list item
3. Third list item

### Task lists

To create a task list, start each list item with a hyphen and space followed by `[ ]`.

```md
- [x] This is a completed task.
- [ ] This is an incomplete task.
```

- [x] This is a completed task.
- [ ] This is an incomplete task.

You can toggle a task in Reading view by selecting the checkbox.

> [!tip]
> You can use any character inside the brackets to mark it as complete.
>
> ```md
> - [x] Milk
> - [?] Eggs
> - [-] Eggs
> ```
>
> - [x] Milk
> - [?] Eggs
> - [-] Eggs

### Nesting lists

All list types can be nested in Obsidian.

To create a nested list, indent one or more list items:

```md
1. First list item
   1. Ordered nested list item
2. Second list item
   - Unordered nested list item
```

1. First list item
   1. Ordered nested list item
2. Second list item
   - Unordered nested list item

Similarly, you can create a nested task list by indenting one or more list items:

```md
- [ ] Task item 1
	- [ ] Subtask 1
- [ ] Task item 2
	- [ ] Subtask 1
```

- [ ] Task item 1
	- [ ] Subtask 1
- [ ] Task item 2
	- [ ] Subtask 1

Use `Tab` or `Shift+Tab` to indent or unindent one or more selected list items for easy organization.
## Horizontal rule

You can use three or more stars `***`, hyphens `---`, or underscore `___` on its own line to add a horizontal bar. You can also separate symbols using spaces.

```md
***
****
* * *
---
----
- - -
___
____
_ _ _
```

***

## Code

You can format code both inline within a sentence, or in its own block.

### Inline code

You can format code within a sentence using single backticks.

```md
Text inside `backticks` on a line will be formatted like code.
```

Text inside `backticks` on a line will be formatted like code.

If you want to put backticks in an inline code block, surround it with double backticks like so: inline ``code with a backtick ` inside``.

### Code blocks

To format a block of code, surround the code with triple backticks.

~~~
```
cd ~/Desktop
```
~~~

```md
cd ~/Desktop
```

You can also create a code block by indenting the text using `Tab` or 4 blank spaces.

```md
    cd ~/Desktop
```

You can add syntax highlighting to a code block, by adding a language code after the first set of backticks.

~~~md
```js
function fancyAlert(arg) {
  if(arg) {
    $.facebox({div:'#foo'})
  }
}
```
~~~

```js
function fancyAlert(arg) {
  if(arg) {
    $.facebox({div:'#foo'})
  }
}
```

Obsidian uses Prism for syntax highlighting. For more information, refer to [Supported languages](https://prismjs.com/#supported-languages).

> [!note]
> [[Edit and preview Markdown#Source mode|Source mode]] and [[Edit and preview Markdown#Live Preview|Live Preview]] do not support PrismJS, and may render syntax highlighting differently.

## Footnotes

You can add footnotes[^footnote] to your notes using the following syntax:

[^footnote]: This is a footnote.

```md
This is a simple footnote[^1].

[^1]: This is the referenced text.
[^2]: Add 2 spaces at the start of each new line.
  This lets you write footnotes that span multiple lines.
[^note]: Named footnotes still appear as numbers, but can make it easier to identify and link references.
```

You can also inline footnotes in a sentence. Note that the caret goes outside the brackets.

```md
You can also use inline footnotes. ^[This is an inline footnote.]
```

> [!note]
> Inline footnotes only work in reading view, not in Live Preview.

## Comments

You can add comments by wrapping text with `%%`. Comments are only visible in Editing view.

```md
This is an %%inline%% comment.

%%
This is a block comment.

Block comments can span multiple lines.
%%
```

## Learn more

To learn more advanced formatting syntax, such as tables, diagrams, and math expressions, refer to [[Advanced formatting syntax]].

To learn more about how Obsidian parses Markdown, refer to [[Obsidian Flavored Markdown]].


---

中文翻译：
---
aliases:
  - 如何/格式化你的笔记
  - Markdown
---

学习如何使用[Markdown](https://daringfireball.net/projects/markdown/)对你的笔记进行基本格式化。如需了解更高级的格式化语法，请参阅[[高级格式化语法]]。

## 段落

要创建段落，请使用空行来分隔一个或多个文本行。

```
这是一个段落。

这是另一个段落。
```

> [!注意]- 多个空格
> 在段落和段落之间的多个相邻空格在[[编辑和预览 Markdown#编辑器视图|阅读视图]]中显示笔记时会合并为一个空格，在[[介绍 Obsidian Publish|Obsidian Publish]]站点上也是如此。
> 
> ```md
> 多个          相邻          空格
> 
> 
> 
> 和多个段落之间的换行。
> ```
> 
> > 多个          相邻          空格
> > 
> > 
> > 
> > 和多个段落之间的换行。
> 
> 如果想要添加多个空格，你可以在笔记中添加 `&nbsp;`（空格）和 `<br>`（换行）。

## 标题

要创建标题，在标题文本之前添加多达六个 `#` 符号。`#` 符号的数量决定了标题的大小。

```md
# 这是标题 1
## 这是标题 2
### 这是标题 3
#### 这是标题 4
##### 这是标题 5
###### 这是标题 6
```

%% 为了避免混乱，这些标题使用 HTML 编写，不会出现在大纲/目录中 %%
<h1>这是标题 1</h1>
<h2>这是标题 2</h2>
<h3>这是标题 3</h3>
<h4>这是标题 4</h4>
<h5>这是标题 5</h5>
<h6>这是标题 6</h6>

## 粗体、斜体、高亮

文本格式化也可以使用[[编辑快捷键]]。

| 样式 | 语法 | 示例 | 输出 |
|-|-|-|-|
| 粗体 | `** **` 或 `__ __` | `**粗体文本**` | **粗体文本** |
| 斜体 | `* *` 或 `_ _`  | `*斜体文本*` | *斜体文本* |
| 删除线 | `~~ ~~` |  `~~删除线文本~~` | ~~删除线文本~~ |
| 高亮 | `== ==` |  `==高亮文本==` | ==高亮文本== |
| 粗体和嵌套斜体 | `** **` 和 `_ _`  | `**粗体和 _嵌套斜体_ 文本**` | **粗体和 _嵌套斜体_ 文本** |
| 粗体和斜体 | `*** ***` 或 `___ ___` |  `***粗体和斜体文本***` | ***粗体和斜体文本*** |

## 内部链接

Obsidian支持[[内部链接]]两种格式之间的链接：

- Wiki链接：`[[运动三定律]]`
- Markdown链接：`[运动三定律](运动三定律.md)`

## 外部链接

如果要链接到外部URL，可以通过在方括号（`[ ]`）中包围链接文本，然后在括号中（`（）`）添加URL来创建内联链接。

```md
[Obsidian帮助](https://help.obsidian.md)
```

[Obsidian帮助](https://help.obsidian.md)

你也可以创建到其他仓库文件的外部链接，通过链接到[[Obsidian URI|Obsidian URI]]。

```md
[笔记](obsidian://open?vault=主仓库&file=笔记.md)
```

### 在链接中转义空格

如果你的URL包含空格，必须用 `%20` 替换它们进行转义。

```md
[我的笔记](obsidian://open?vault=主仓库&file=我的%20笔记.md)
```

你也可以用尖括号（`< >`）来包裹URL进行转义。

```md
[我的笔记]（<obsidian://open?vault=主仓库&file=我的 笔记.md>）
```

## 外部图片

你可以通过在[[#外部链接|外部链接]]前加上 `!` 符号来添加外部URL的图片。

```md
![Engelbart](https://history-computer.com/ModernComputer/Basis/images/Engelbart.jpg)
```

![Engelbart](https://history-computer.com/ModernComputer/Basis/images/Engelbart.jpg)

你可以通过在链接目的地添加 `|640x480` 来更改图片尺寸，其中640是宽度，480是高度。

```md
![Engelbart|100x145](https://history-computer.com/ModernComputer/Basis/images/Engelbart.jpg)
```

如果只指定了宽度，图片会根据原始长宽比进行缩放。例如：

```md
![Engelbart|100](https://history-computer.com/ModernComputer/Basis/images/Engelbart.jpg)
```

> [!提示]
> 如果要添加来自仓库内部的图片，你也可以[[嵌入文件#在笔记中嵌入图片|在笔记中嵌入图片]]。

## 引用

你可以在文本前加上 `>` 符号来引用文本。

```md
> 人类面临着越来越复杂和紧迫的问题，他们有效应对这些问题的能力对于社会的稳定和持续发展至关重要。

\- 道格·恩格尔巴特，1961
```

> 人类面临着越来越复杂和紧迫的问题，他们有效应对这些问题的能力对于社会的稳定和持续发展至关重要。

\- 道格·恩格尔巴特，1961

> [!提示]
> 你可以通过在引用中的第一行添加 `[!信息]` 来将引用变成[[标注|标注]]。

## 列表

你可以在文本前加上 `-`、`*` 或 `+` 来创建无序列表。

```md
- 第一条
- 第二条
- 第三条
```

- 第一条
- 第二条
- 第三条

要创建有序列表，每行以数字加上 `.` 符号开头。

```md
1. 第一条
2. 第二条
3. 第三条
```

1. 第一条
2. 第二条
3. 第三条

### 任务列表

要创建任务列表，每个列表项以连字符和空格开头，后跟 `[ ]`。

```md
- [x] 这是已完成的任务。
- [ ] 这是未完成的任务。
```

- [x] 这是已完成的任务。
- [ ] 这是未完成的任务。

你可以在阅读视图中通过选择复选框来切换任务状态。

> [!提示]
> 你可以在括号内使用任何字符来标记任务为已完成。
>
> ```md
> - [x] 牛奶
> - [?] 鸡蛋
> - [-] 鸡蛋
> ```
>
> - [x] 牛奶
> - [?] 鸡蛋
> - [-] 鸡蛋

### 嵌套列表

Obsidian中所有类型的列表都支持嵌套。

要创建嵌套列表，请缩进一个或多个列表项：

```md
1. 第一条
   1. 有序嵌套列表项
2. 第二条
   - 无序嵌套列表项
```

1. 第一条
   1. 有序嵌套列表项
2. 第二条
   - 无序嵌套列表项

同样，你可以通过缩进一个或多个列表项来创建嵌套任务列表：

```md
- [ ] 任务项 1
	- [ ] 子任务 1
- [ ] 任务项 2
	- [ ] 子任务 1
```

- [ ] 任务项 1
	- [ ] 子任务 1
- [ ] 任务项 2
	- [ ] 子任务 1

使用 `Tab` 或 `Shift+Tab` 来缩进或取消缩进一个或多个已选择的列表项，以便进行简单的组织。

## 水平线

你可以在单独的一行上使用三个或更多星号 `***`、短横线 `---` 或下划线 `___` 来添加水平线。你也可以用空格分隔符号。

```md
***
****
* * *
---
----
- - -
___
____
_ _ _
```

***

## 代码

你可以在句子中内联格式化代码，或将其放在自己的代码块中。

### 内联代码

你可以使用单个反引号在句子中格式化代码。

```md
反引号中的文本`将被格式化为代码。
```

反引号中的文本`将被格式化为代码。

如果要在内联代码块中放置反引号，请用双反引号包围，如：inline ``内部带有反引号`的代码``。

### 代码块

要格式化一个代码块，请用三个反引号括住代码。

~~~
```
cd ~/Desktop
```
~~~

```md
cd ~/Desktop
```

你也可以通过使用 `Tab` 键或4个空格来缩进文本来创建代码块。

```md
    cd ~/Desktop
```

你可以在第一个反引号后添加语言代码来为代码块添加语法高亮。

~~~md
```js
function fancyAlert(arg) {
  if(arg) {
    $.facebox({div:'#foo'})
  }
}
```
~~~

```js
function fancyAlert(arg) {
  if(arg) {
    $.facebox({div:'#foo'})
  }
}
```

Obsidian使用Prism进行语法高亮。有关更多信息，请参阅[支持的语言](https://prismjs.com/#supported-languages)。

> [!注意]
> [[编辑和预览 Markdown#源代码模式|源代码模式]]和[[编辑和预览 Markdown#实时预览|实时预览]]不支持PrismJS，可能会以不同方式呈现语法高亮。

## 脚注

你可以使用以下语法向笔记中添加脚注[^脚注]：

[^脚注]: 这是一个脚注。

```md
这是一个简单的脚注[^1]。

[^1]: 这是引用文本。
[^2]: 在每一行的开头添加2个空格。
  这样可以编写跨越多行的脚注。
[^注释]: 命名脚注仍然显示为数字，但可以更容易地识别和链接引用。
```

你也可以在句子中使用内联脚注。请注意插入符号在方括号外。

```md
你也可以使用内联脚注。^[这是一个内联脚注。]
```

> [!注意]
> 内联脚注仅在阅读视图中有效，不适用于实时预览。

## 注释

你可以用 `%%` 包围文本来添加注释。注释只在编辑视图中可见。

```md
这是一个 %%内联%% 注释。

%%
这是一个块注释。

块注释可以跨多行。
%%
```

## 了解更多

要了解更多高级格式化语法，如表格、图表和数学表达式，请参阅[[高级格式化语法]]。

要了解Obsidian如何解析Markdown，请参阅[[Obsidian Flavored Markdown]]。