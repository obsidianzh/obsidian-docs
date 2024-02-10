---
aliases: 
- How to/Working with tags
---

Tags are keywords or topics that help you quickly find the notes you want.

## Add a tag to a note

To create a tag, enter a hash symbol (`#`) in the editor, followed by a keyword. For example, `#meeting`.

You can also add tags using the `tags` [[Properties|property]]. Tags in YAML should always be formatted as a list:

```yaml
---
tags:
  - recipe
  - cooking
---
```

## Find notes using tags

To find notes using the [[Search]] plugin, use the `tag` [[Search#Search operators|search operator]] in your search term, for example `tag:#meeting`.

You can also search for tags by clicking on them in your notes.

To find notes using the [[Tags view|Tags view]] plugin, select **Tags: Show tags** in the [[Command palette]], and then select the tag you want to search for.

## Nested tags

Nested tags define tag hierarchies that make it easier to find and filter related tags.

Create nested tags by using forward slashes (`/`) in the tag name, for example  `#inbox/to-read` and `#inbox/processing`.

Both the [[Search]] and [[Tags view|Tags view]] plugins support nested tags.

## Tag format

You can use any of the following characters in your tags:

- Alphabetical letters
- Numbers
- Underscore (`_`)
- Hyphen (`-`)
- Forward slash (`/`) for [[#Nested tags]]

Tags must contain at least one non-numerical character. For example, #1984 isn't a valid tag, but #y1984 is.

Tags are case-insensitive. For example, #tag and #TAG will be treated as identical.

> [!note] 
> Tags will display with the casing they are first created with in the [[Tags view]]. 
> For example, creating #Tag and then #TAG will display #Tag for both. 

Tags can't contain blank spaces. To separate two or more words, you can instead use the following formats:

- #camelCase
- #PascalCase
- #snake_case
- #kebab-case


---

中文翻译：
---
aliases: 
- 如何/使用标签
---

标签是帮助你快速找到所需笔记的关键词或主题。

## 给笔记添加标签

要创建标签，在编辑器中输入井号 (`#`)，然后跟上关键词。例如，`#会议`。

你也可以使用`tags` [[属性|属性]] 来添加标签。在 YAML 中，标签应该被格式化为列表：

```yaml
---
tags:
  - 食谱
  - 烹饪
---
```

## 使用标签查找笔记

要使用[[搜索|Search]]插件查找笔记，可以在搜索词中使用 `tag` [[搜索运算符|搜索运算符]]，例如 `tag:#会议`。

你也可以通过在笔记中点击标签来查找标签。

要使用[[标签视图|Tags view]]插件查找笔记，选择在[[命令面板]]中的**标签：显示标签**，然后选择要搜索的标签。

## 嵌套标签

嵌套标签定义了标签层次结构，使查找和筛选相关标签更加容易。

通过在标签名中使用斜杠（`/`）创建嵌套标签，例如 `#收件箱/待阅读` 和 `#收件箱/处理中`。

[[搜索|Search]]和[[标签视图|Tags view]]插件都支持嵌套标签。

## 标签格式

你可以在标签中使用以下任意字符：

- 字母
- 数字
- 下划线 (`_`)
- 连字符 (`-`)
- 正斜杠 (`/`) 用于[[#Nested tags|嵌套标签]]

标签必须至少包含一个非数字字符。例如，#1984 不是有效标签，但 #y1984 是。

标签不区分大小写。例如，#标签 和 #标签 将被视为相同。

> [!注意] 
> 在[[标签视图]]中，标签将以它们最初创建时的大小写显示。
> 例如，先创建 #标签，然后创建 #标签，都会显示为 #标签。

标签不能包含空格。如果要分隔两个或多个单词，可以使用以下格式：

- #驼峰命名法
- #帕斯卡命名法
- #蛇形命名法
- #短横线命名法