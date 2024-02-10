---
aliases:
  - front matter
  - Advanced topics/YAML front matter
  - metadata
  - property
---
Properties allow you to organize information about a note. Properties contain structured data such as text, links, dates, checkboxes, and numbers. Properties can also be used in combination with [[Community plugins]] that can do useful things with your structured data.

## Add properties to a note

There are several ways to add a property to a note:

- Use the **Add file property** [[Command palette|command]].
- Use the **`Cmd/Ctrl+;`** [[Hotkeys|hotkey]].
- Choose **Add file property** from the **More actions** menu (brought up by the three dots icon or by right-clicking the tab).
- Type `---` at the very beginning of a file.

Once you add a property, a row will appear at the top of the file with two inputs: the property _name_ and the property _value_.

For the name, you can choose anything you like. Obsidian provides several default properties: `tags`, `cssclasses`, and `aliases`.

Once you choose the property name, you can give it a value.

### Property types

In addition to a name and value, properties also have a *type*. A property's type describes the kind of values it can store. To change the type of a property, click the property's icon or use the **Edit file property** command.

Obsidian supports the following property types:

- **Text**
- **List**
- **Number**
- **Checkbox**
- **Date**
- **Date & time**

Once a property type is assigned to a property, all properties with that name are assumed to have the same property type.

## Advanced uses

### Links

**Text** and **List** type properties can contain URLs and [[Internal links]] using the `[[Link]]` syntax.

### Search properties

Properties have their own [[Search|search syntax]] that you can use alongside other search terms and operators. [[Search#Search properties|See search syntax for properties]].

### Templates

You can add properties to [[Templates]]. When you insert a template into the active note, all the properties from the template will be added to the note. Obsidian will also merge any properties that exist in your note with properties in the template.

### Rename properties

You can rename a property by right-clicking it in the [[Properties view|All properties view]].

### Display modes

You can change how properties are displayed in your note by going to  **Settings → Editor → Properties in document**. The options are:

- **Visible** (default) — displays properties at the top of the note, if there are any.
- **Hidden** — hides properties, can still be displayed in the sidebar via [[Properties view]].
- **Source** — displays properties in plain text YAML format.

### Not supported

A few features are not supported in Obsidian:

- **Nested properties** — to view nested properties we recommend using the Source display.
- **Bulk editing properties** — this can be achieved with community-made tools such as Python scripts.
- **Markdown in properties** — this is an intentional limitation as properties are meant for small, atomic bits of information that are both human and machine readable.

## Hotkeys

### Add a property

| Action | Hotkey |
|---|---|
|Add new property|`Cmd + ;`|

### Navigate between properties

When a property is focused 

| Action | Hotkey |
|---|---|
|Focus next property|`Down arrow` or `Tab`|
|Focus previous property|`Up arrow` or `Shift+Tab`|
|Jump to editor|`Alt+Down arrow`|

### Select properties

| Action | Hotkey |
|---|---|
|Extend selection upwards|`Shift+Up arrow`|
|Extend selection downwards|`Shift+Down arrow`|
|Select all|`Cmd+A`|

### Edit properties

| Action | Hotkey |
|---|---|
|Edit property name|`Left arrow`|
|Edit property value|`Right arrow`|
|Focus property|`Escape`|
|Delete property|`Cmd+Backspace`<br><br>if any properties are selected, it will delete the selection instead.|
|Undo|`Cmd+Z`|
|Redo|`Cmd+Shift+Z`|

### Vim (advanced)

| Action | Hotkey |
|---|---|
|Move down|`j`|
|Move up|`k`|
|Focus key|`h`|
|Focus value|`l`|
|Focus value (Cursor at end)|`A`|
|Focus value (Cursor at beginning)|`i`|
|Create new property|`o`|

## Property format

Properties are stored in [YAML](https://yaml.org/)  format at the top of the file. YAML is a widely used format that's readable by both humans and machines.

Property names are separated from their values by a colon followed by a space:

```yaml
---
name: value
---
```

While the order of each name-value pair doesn't matter, each name must be unique within a note. For example, you can't have more than one `tags` property.

Values can be text, numbers, true or false, or even collections of values (arrays).

```yaml
---
title: A New Hope
year: 1977
favorite: true
cast:
  - Mark Hamill
  - Harrison Ford
  - Carrie Fisher
---
```

Internal links in **Text** and **List** type properties must be surrounded with quotes. Obsidian will automatically add these if you manually enter internal links into properties, but be careful to add them when using templating plugins.

```yaml
---
link: "[[Link]]" 
linklist: 
  - "[[Link]]" 
  - "[[Link2]]"
---
```

**Date** and **Date & time** type properties are stored in the following format:

```yaml
---
date: 2020-08-21
time: 2020-08-21T10:30:00
---
```

The date picker follows your operating system's default date and time format. You can change it in your system preferences: 

> [!info]- Windows
> **Settings → Time & Language → Language & Region → Regional Format → Change Formats**
> 
> ![[Windows-OS-DateTime.png#interface]]

> [!info]- Mac OS
> **System Preferences → Language and Region → Date format**
> 
> ![[Mac-OS-DateTime.png|450]]

With the [[Daily notes]] plugin enabled, the date property will additionally function as an internal link to the corresponding daily note for that date.

![[Daily notes#^daily-notes-date]]
### JSON Properties

While we recommend using YAML to define properties, you can also define properties using [JSON](https://www.json.org/):

```json
---
{
  "tags": "journal",
  "publish": false
}
---
```

Note that the JSON block will be read, interpreted, and saved as YAML.

## Default properties

Obsidian comes with a set of default properties:

| Property | Description |
|-|-|
| `tags` | See [[Editing and formatting/Tags\|Tags]]. |
| `aliases` | See [[Aliases]]. |
| `cssclasses` | Allows you to style individual notes using [[CSS snippets]]. |

### Properties for Obsidian Publish

The following properties can be used with [[Introduction to Obsidian Publish|Obsidian Publish]]:

| Property | Description |
|-|-|
| `publish` | See [[Publish and unpublish notes#Automatically select notes to publish\|Automatically select notes to publish]]. |
| `permalink` | See [[Publish and unpublish notes#Permalinks\|Permalinks]]. |
| `description` | See [[Social media link previews#Description\|Description]]. |
| `image` | See [[Social media link previews#Image\|Image]]. |
| `cover` | See [[Social media link previews#Image\|Image]]. |

### Deprecated properties

These properties were deprecated in Obsidian 1.4. Please do not use them anymore:

| Property | Description |
|-|-|
| `tag` | Deprecated alias for `tags`. |
| `alias` | Deprecated alias for `aliases`. |
| `cssclass` | Deprecated alias for `cssclasses`. |



---

中文翻译：
---
aliases:
  - 前置元数据
  - 高级主题/YAML前置元数据
  - 元数据
  - 属性
---
属性允许你组织关于笔记的信息。属性包含结构化数据，如文本、链接、日期、复选框和数字。属性还可以与[[社区插件]]结合使用，这些插件可以处理你的结构化数据并完成一些有用的操作。

## 在笔记中添加属性

有几种方法可以向笔记中添加属性：

- 使用**添加文件属性**[[命令面板|命令]]。
- 使用**`Cmd/Ctrl+;`**[[快捷键|热键]]。
- 从**更多操作**菜单中选择**添加文件属性**（通过三个点图标或右键单击选项卡呼出）。
- 在文件的开头输入`---`。

添加属性后，文件顶部会出现一行，包含两个输入框：属性_名称_和属性_值_。

对于名称，你可以选择任何你喜欢的名称。Obsidian提供了几个默认属性：`tags`、`cssclasses`和`aliases`。

选择属性名称后，可以为其赋值。

### 属性类型

除了名称和值外，属性还有一个*类型*。属性的类型描述了它可以存储的值的种类。要更改属性的类型，点击属性的图标或使用**编辑文件属性**命令。

Obsidian支持以下属性类型：

- **文本**
- **列表**
- **数字**
- **复选框**
- **日期**
- **日期和时间**

一旦属性类型分配给属性，所有具有该名称的属性都被假定为具有相同的属性类型。

## 高级用法

### 链接

**文本**和**列表**类型的属性可以包含URL和[[内部链接]]，使用`[[链接]]`语法。

### 搜索属性

属性有自己的[[搜索|搜索语法]]，你可以将其与其他搜索项和运算符一起使用。[[搜索#搜索属性|查看属性搜索语法]]。

### 模板

你可以向[[模板]]中添加属性。当你将模板插入活动笔记时，模板中的所有属性都将添加到笔记中。Obsidian还会将笔记中存在的属性与模板中的属性合并。

### 重命名属性

你可以通过在[[属性视图|全部属性视图]]中右键单击属性来重命名属性。

### 显示模式

你可以通过转到**设置 → 编辑器 → 文档中的属性**来更改属性在笔记中的显示方式。选项包括：

- **可见**（默认）— 如果有属性，将在笔记顶部显示属性。
- **隐藏** — 隐藏属性，仍可通过[[属性视图]]在侧边栏中显示。
- **源代码** — 以纯文本YAML格式显示属性。

### 不支持的功能

在Obsidian中不支持一些功能：

- **嵌套属性** — 若要查看嵌套属性，建议使用源代码显示。
- **批量编辑属性** — 可以使用社区制作的工具，如Python脚本来实现。
- **属性中的Markdown** — 这是一个故意的限制，因为属性旨在用于既能人类阅读又能机器读取的小型、原子化信息。

## 快捷键

### 添加属性

| 动作 | 快捷键 |
|---|---|
|添加新属性|`Cmd + ;`|

### 在属性之间导航

当属性被聚焦时

| 动作 | 快捷键 |
|---|---|
|聚焦到下一个属性|`下箭头`或`Tab`|
|聚焦到上一个属性|`上箭头`或`Shift+Tab`|
|跳转到编辑器|`Alt+下箭头`|

### 选择属性

| 动作 | 快捷键 |
|---|---|
|向上扩展选择|`Shift+上箭头`|
|向下扩展选择|`Shift+下箭头`|
|全部选择|`Cmd+A`|

### 编辑属性

| 动作 | 快捷键 |
|---|---|
|编辑属性名称|`左箭头`|
|编辑属性值|`右箭头`|
|聚焦属性|`Escape`|
|删除属性|`Cmd+Backspace`<br><br>如果有任何属性被选中，将删除选中的内容。|
|撤销|`Cmd+Z`|
|重做|`Cmd+Shift+Z`|

### Vim（高级）

| 动作 | 快捷键 |
|---|---|
|向下移动|`j`|
|向上移动|`k`|
|聚焦到键|`h`|
|聚焦到值|`l`|
|聚焦到值（光标在结尾处）|`A`|
|聚焦到值（光标在开头处）|`i`|
|创建新属性|`o`|

## 属性格式

属性以[YAML](https://yaml.org/)格式存储在文件的顶部。YAML是一种广泛使用的格式，可供人类和机器阅读。

属性名称与值之间用冒号和空格分隔：

```yaml
---
名称: 值
---
```

每个名称-值对的顺序并不重要，但每个名称在笔记内必须是唯一的。例如，你不能有多个`tags`属性。

值可以是文本、数字、true或false，甚至是值的集合（数组）。

```yaml
---
标题: 新的希望
年份: 1977
喜爱: true
演员:
  - 马克·哈米尔
  - 汉森·福特
  - 凯丽·费雪
---
```

**文本**和**列表**类型属性中的内部链接必须用引号括起来。如果手动在属性中输入内部链接，Obsidian会自动添加这些引号，但在使用模板插件时要小心添加。

```yaml
---
链接: "[[链接]]" 
链接列表: 
  - "[[链接]]" 
  - "[[链接2]]"
---
```

**日期**和**日期和时间**类型属性以以下格式存储：

```yaml
---
日期: 2020-08-21
时间: 2020-08-21T10:30:00
---
```

日期选择器遵循你操作系统的默认日期和时间格式。你可以在系统偏好设置中更改它：

> [!信息]- Windows
> **设置 → 时间和语言 → 语言和地区 → 区域格式 → 更改格式**
> 
> ![[Windows-OS-DateTime.png#interface]]

> [!信息]- Mac OS
> **系统偏好设置 → 语言与地区 → 日期格式**
> 
> ![[Mac-OS-DateTime.png|450]]

启用[[每日笔记]]插件后，日期属性还将作为对应日期的每日笔记的内部链接。

![[Daily notes#^daily-notes-date]]
### JSON属性

虽然我们建议使用YAML定义属性，但也可以使用[JSON](https://www.json.org/)定义属性：

```json
---
{
  "标签": "日记",
  "发布": false
}
---
```

请注意，JSON块将被读取、解释和保存为YAML。 

## 默认属性

Obsidian附带一组默认属性：

| 属性 | 描述 |
|-|-|
| `tags` | 查看[[编辑和格式化/标签\|标签]]。 |
| `aliases` | 查看[[别名]]。 |
| `cssclasses` | 允许你使用[[CSS代码片段]]来为单个笔记设置样式。 |

### 用于Obsidian发布的属性

以下属性可与[[介绍Obsidian发布|Obsidian发布]]一起使用：

| 属性 | 描述 |
|-|-|
| `publish` | 查看[[发布和取消发布笔记#自动选择要发布的笔记\|自动选择要发布的笔记]]。 |
| `permalink` | 查看[[发布和取消发布笔记#永久链接\|永久链接]]。 |
| `description` | 查看[[社交媒体链接预览#描述\|描述]]。 |
| `image` | 查看[[社交媒体链接预览#图片\|图片]]。 |
| `cover` | 查看[[社交媒体链接预览#图片\|图片]]。 |

### 废弃的属性

这些属性在Obsidian 1.4中已被弃用，请不要再使用：

| 属性 | 描述 |
|-|-|
| `tag` | 用于`tags`的弃用别名。 |
| `alias` | 用于`aliases`的弃用别名。 |
| `cssclass` | 用于`cssclasses`的弃用别名。 |