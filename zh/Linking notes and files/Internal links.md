---
aliases:
- How to/Internal link
- How to/Link to blocks
---

Learn how to link to notes, attachments, and other files from your notes, using _internal links_. By linking notes, you can create a network of knowledge. ^b15695

Obsidian can automatically update internal links in your vault when you rename a file. If you want to be prompted instead, you can disable it under **Settings → Files & Links → Automatically update internal links**.

## Supported formats for internal links

Obsidian supports the following link formats:

- Wikilink: `[[Three laws of motion]]`
- Markdown: `[Three laws of motion](Three%20laws%20of%20motion.md)`

The examples above are equivalent—they appear the same way in the editor, and links to the same note.

> [!note]
> When using the Markdown format, make sure to [URL encode](https://en.wikipedia.org/wiki/Percent-encoding) the link destination. For example, blank spaces become `%20`.

By default, due to its more compact format, Obsidian generates links using the Wikilink format. If interoperability is important to you, you can disable Wikilinks and use Markdown links instead.

To use the Markdown format:

1. Open **Settings**.
2. Under **Files & Links**, disable **Use \[\[Wikilink\]\]**.

Even if you disable the Wikilink format, you can still autocomplete links by typing two square brackets `[[`. When you select one of the suggested files, Obsidian instead generates a Markdown link.

## Link to a file

To create a link while in Editing view, use either of the following ways:

- Type `[[` in the editor and then select the file you want to create a link to.
- Select text in the editor and then type `[[`.
- Open the [[Command palette]] and then select **Add internal link**.

While you can link to any of the [[Accepted file formats]], links to file formats other than Markdown needs to include a file extension, such as `[[Figure 1.png]]`.

## Link to a heading in a note

You can link to specific headings in notes, also known as _anchor links_.

To link to a heading, add a hash (`#`) at the end of the link destination, followed by the heading text.

For example, `[[Three laws of motion#Second law]]`.

You can add multiple hash symbols for each subheading.

For example, `[[My note#Heading 1#Heading 2]]`.

> [!tip]- Heading links across the vault
> You can search for headers to link to from across your vault using the `[[##header]]` syntax. 
> 
> ![[internal-links-header.png#interface]]


## Link to a block in a note

A block is a unit of text in your note, for example a paragraph, block quote, or even a list item.

You can link to a block by adding `#^` at the end of your link destination followed by a unique block identifier, for example, `[[2023-01-01#^37066d]]`.

Fortunately, you don't need to know the identifier. When you type the caret (`^`), you can select the block from a list of suggestions to insert the right identifier.

You can also create human-readable block identifiers by adding a blank space followed by the identifier, for example `^quote-of-the-day`, at the end of a block:

```md
"You do not rise to the level of your goals. You fall to the level of your systems." by James Clear ^quote-of-the-day
```

Now you can instead link to the block by typing `[[2023-01-01#^quote-of-the-day]]`.

Block identifiers can only consist of Latin letters, numbers, and dashes.

> [!tip]- Block links across the vault
> You can search for blocks to link to from across your vault using the `[[^^block]]` syntax. However, more items qualify as blocks in comparison to [[#Link to a heading in a note|heading links]] so this list will be much longer in comparison.
> 
> ![[link-block-heading.png#interface]]

> [!warning] Interoperability
> Block references are specific to Obsidian and not part of the standard Markdown format. Links containing block references won't work outside of Obsidian.

## Change the link display text

By default, Obsidian will show the link text, or the [[Aliases|alias]] if you opt to [[Aliases#Link to a note using an alias|link to an alias]]. You have the option to modify the text used for displaying a link. This feature comes in handy when you prefer to incorporate a link into a sentence without explicitly using the file name.

**Wikilink format:**

You can use the vertical bar (`|`) to change the text used to display a link.

For example, `[[Internal links|custom display text]]` appears as [[Internal links|custom display text]].

**Markdown format:**

Enter the display text between the square brackets (`[]`).

For example, `[custom display text](Internal%20links.md)` appears as [custom display text](Internal%20links.md).


## Preview a linked file

> [!note]
> To preview linked files, you first need to enable [[Page preview]].

To preview a linked file, press `Ctrl` (or `Cmd` on macOS) while hovering the cursor over the link. A preview of the file content appears next to the cursor.


---

中文翻译：
学习如何使用**内部链接**从你的笔记中链接到其他笔记、附件以及其他文件。通过链接笔记，你可以创建一个知识网络。 ^b15695

当你重命名文件时，Obsidian可以自动更新仓库中的内部链接。如果你希望收到提示，可以在**设置 → 文件与链接 → 自动更新内部链接**下禁用此功能。

## 内部链接支持的格式

Obsidian支持以下链接格式：

- Wikilink：`[[运动三定律]]`
- Markdown：`[运动三定律](运动三定律.md)`

上述示例是等效的——它们在编辑器中显示相同，并链接到同一笔记。

> [!注意]
> 当使用Markdown格式时，确保对链接目标进行[URL编码](https://zh.wikipedia.org/wiki/百分号编码)。例如，空格会变成`%20`。

默认情况下，出于紧凑性考虑，Obsidian使用Wikilink格式生成链接。如果你更看重互操作性，可以禁用Wikilinks，改用Markdown链接。

要使用Markdown格式：

1. 打开**设置**。
2. 在**文件与链接**下，禁用**使用\[\[Wikilink\]\]**。

即使你禁用了Wikilink格式，仍然可以通过在编辑器中输入两个方括号`[[`来自动补全链接。当你选择其中一个建议的文件时，Obsidian会生成Markdown链接。

## 链接到文件

在编辑视图下创建链接的方式有：

- 在编辑器中输入`[[`，然后选择要链接到的文件。
- 选择编辑器中的文本，然后输入`[[`。
- 打开[[命令面板]]，然后选择**添加内部链接**。

虽然你可以链接到[[接受的文件格式]]中的任何文件，但链接到除Markdown以外的文件格式需要包括文件扩展名，例如`[[图1.png]]`。

## 链接到笔记中的标题

你可以链接到笔记中的特定标题，也称为_锚链接_。

要链接到标题，需要在链接目标末尾加上井号(`#`)，后跟标题文本。

例如，`[[运动三定律#第二定律]]`。

你可以为每个子标题添加多个井号。

例如，`[[我的笔记#标题1#标题2]]`。

> [!提示]- 跨仓库的标题链接
> 你可以使用`[[##标题]]`语法从整个仓库中搜索要链接的标题。
> 
> ![[internal-links-header.png#界面]]


## 链接到笔记中的块

块是笔记中的文本单元，例如段落、块引用，甚至列表项。

你可以通过在链接目标末尾加上`#^`，后跟唯一的块标识符，例如`[[2023-01-01#^37066d]]`，来链接到一个块。

幸运的是，你不需要知道标识符。当你输入插入符号(`^`)时，可以从建议列表中选择块以插入正确的标识符。

你还可以通过在块末尾添加一个空格，后跟标识符，例如`^每日引言`，来创建易读的块标识符：

```md
"你不会达到你的目标水平。你会跌落到你的系统水平。" —— James Clear ^每日引言
```

现在你可以通过输入`[[2023-01-01#^每日引言]]`来链接到这个块。

块标识符只能包含拉丁字母、数字和短横线。

> [!提示]- 跨仓库的块链接
> 你可以使用`[[^^块]]`语法从整个仓库中搜索要链接的块。不过，与[[#链接到笔记中的标题|标题链接]]相比，更多的内容会被视为块，因此这个列表会更长。
> 
> ![[link-block-heading.png#界面]]

> [!警告] 互操作性
> 块引用是Obsidian特有的，不属于标准Markdown格式。包含块引用的链接在Obsidian之外不起作用。

## 更改链接显示文本

默认情况下，Obsidian会显示链接文本，或者如果选择[[别名|别名]]，则显示别名。你可以修改用于显示链接的文本。当你希望将链接融入到句子中而不明确使用文件名时，这个功能会派上用场。

**Wikilink格式：**

你可以使用竖线(`|`)来更改用于显示链接的文本。

例如，`[[内部链接|自定义显示文本]]` 显示为 [[内部链接|自定义显示文本]]。

**Markdown格式：**

在方括号(`[]`)之间输入显示文本。

例如，`[自定义显示文本](内部链接.md)` 显示为 [自定义显示文本](内部链接.md)。


## 预览链接文件

> [!注意]
> 要预览链接的文件，首先需要启用[[页面预览]]。

要预览链接的文件，按住`Ctrl`（或macOS上的`Cmd`）并将光标悬停在链接上。文件内容的预览会出现在光标旁边。