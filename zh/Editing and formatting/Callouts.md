---
aliases:
- How to/Use callouts
---

Use callouts to include additional content without breaking the flow of your notes.

To create a callout, add `[!info]` to the first line of a blockquote, where `info` is the _type identifier_. The type identifier determines how the callout looks and feels. To see all available types, refer to [[#Supported types]].

```markdown
> [!info]
> Here's a callout block.
> It supports **Markdown**, [[Internal link|Wikilinks]], and [[Embed files|embeds]]!
> ![[Engelbart.jpg]]
```

> [!info]
> Here's a callout block.
> It supports **Markdown**, [[Internal links|Wikilinks]] and [[Embed files|embeds]]!
> ![[Engelbart.jpg]]

Callouts are also supported natively on [[Introduction to Obsidian Publish|Obsidian Publish]].

> [!note]
> If you're also using the Admonitions plugin, you should update it to at least version 8.0.0 to avoid problems with the new callout feature.

### Change the title

By default, the title of the callout is its type identifier in title case. You can change it by adding text after the type identifier:

```markdown
> [!tip] Callouts can have custom titles
> Like this one.
```

> [!tip] Callouts can have custom titles
> Like this one.

You can even omit the body to create title-only callouts:

```markdown
> [!tip] Title-only callout
```

> [!tip] Title-only callout

### Foldable callouts

You can make a callout foldable by adding a plus (+) or a minus (-) directly after the type identifier.

A plus sign expands the callout by default, and a minus sign collapses it instead.

```markdown
> [!faq]- Are callouts foldable?
> Yes! In a foldable callout, the contents are hidden when the callout is collapsed.
```

> [!faq]- Are callouts foldable?
> Yes! In a foldable callout, the contents are hidden when collapsed.

### Nested callouts

You can nest callouts in multiple levels.

```markdown
> [!question] Can callouts be nested?
> > [!todo] Yes!, they can.
> > > [!example]  You can even use multiple layers of nesting.
```

> [!question] Can callouts be nested?
> > [!todo] Yes!, they can.
> > > [!example]  You can even use multiple layers of nesting.

### Customize callouts

[[CSS snippets]] and [[Community plugins]] can define custom callouts, or even overwrite the default configuration.

To define a custom callout, create the following CSS block:

```css
.callout[data-callout="custom-question-type"] {
    --callout-color: 0, 0, 0;
    --callout-icon: lucide-alert-circle;
}
```

The value of the `data-callout` attribute is the type identifier you want to use, for example `[!custom-question-type]`.

- `--callout-color` defines the background color using numbers (0–255) for red, green, and blue.
- `--callout-icon` can be an icon ID from [lucide.dev](https://lucide.dev), or an SVG element. 

> [!warning] Note about lucide icon versions
> Obsidian updates Lucide icons periodically. The current version included is shown below; use these or earlier icons in custom callouts.
> ![[Credits#^lucide]]

> [!tip] SVG icons
> Instead of using a Lucide icon, you can also use a SVG element as the callout icon.
>
> ```css
> --callout-icon: '<svg>...custom svg...</svg>';
> ```

### Supported types

You can use several callout types and aliases. Each type comes with a different background color and icon.

To use these default styles, replace `info` in the examples with any of these types, such as `[!tip]` or `[!warning]`.

Unless you [[#Customize callouts]], any unsupported type defaults to the `note` type. The type identifier is case-insensitive.

> [!note]
> ```md
> > [!note]
> > Lorem ipsum dolor sit amet
> ```

---

> [!abstract]-
> ```md
> > [!abstract]
> > Lorem ipsum dolor sit amet
> ```

Aliases: `summary`, `tldr`

---

> [!info]-
> ```md
> > [!info]
> > Lorem ipsum dolor sit amet
> ```

---

> [!todo]-
> ```md
> > [!todo]
> > Lorem ipsum dolor sit amet
> ```

---

> [!tip]-
> ```md
> > [!tip]
> > Lorem ipsum dolor sit amet
> ```

Aliases: `hint`, `important`

---

> [!success]-
> ```md
> > [!success]
> > Lorem ipsum dolor sit amet
> ```

Aliases: `check`, `done`

---

> [!question]-
> ```md
> > [!question]
> > Lorem ipsum dolor sit amet
> ```

Aliases: `help`, `faq`

---

> [!warning]-
>  ```md
> > [!warning]
> > Lorem ipsum dolor sit amet
> ```

Aliases: `caution`, `attention`

---

> [!failure]-
> ```md
> > [!failure]
> > Lorem ipsum dolor sit amet
> ```

Aliases: `fail`, `missing`

---

> [!danger]-
> ```md
> > [!danger]
> > Lorem ipsum dolor sit amet
> ```

Alias: `error`

---

> [!bug]-
> ```md
> > [!bug]
> > Lorem ipsum dolor sit amet
> ```

---

> [!example]-
> ```md
> > [!example]
> > Lorem ipsum dolor sit amet
> ```

---

> [!quote]-
> ```md
> > [!quote]
> > Lorem ipsum dolor sit amet
> ```

Alias: `cite`


---

中文翻译：
---
aliases:
- 如何/使用标注

使用标注可以在不打乱笔记流程的情况下包含额外内容。

要创建标注，将 `[!info]` 添加到引用块的第一行，其中 `info` 是 _类型标识符_。类型标识符决定标注的外观和感觉。要查看所有可用类型，请参阅[[#支持的类型]]。

```markdown
> [!info]
> 这是一个标注块。
> 它支持 **Markdown**、[[内部链接|维基链接]] 和 [[嵌入文件|嵌入]]！
> ![[Engelbart.jpg]]
```

> [!info]
> 这是一个标注块。
> 它支持 **Markdown**、[[内部链接|维基链接]] 和 [[嵌入文件|嵌入]]！
> ![[Engelbart.jpg]]

在[[对 Obsidian Publish 的介绍|Obsidian Publish]]中也原生支持标注。

> [!note]
> 如果你同时使用 Admonitions 插件，应将其更新至至少 8.0.0 版本，以避免与新标注功能的问题。

### 修改标题

默认情况下，标注的标题是其类型标识符的标题格式。你可以在类型标识符后添加文本来更改它：

```markdown
> [!tip] 标注可以有自定义标题
> 就像这个一样。
```

> [!tip] 标注可以有自定义标题
> 就像这个一样。

你甚至可以省略内容，创建仅带标题的标注：

```markdown
> [!tip] 仅标题的标注
```

> [!tip] 仅标题的标注

### 可折叠标注

你可以通过在类型标识符后直接添加加号（+）或减号（-）来使标注可折叠。

加号表示标注默认展开，减号表示标注收起。

```markdown
> [!faq]- 标注可以折叠吗？
> 可以！在可折叠标注中，当标注收起时，内容会被隐藏。
```

> [!faq]- 标注可以折叠吗？
> 可以！在可折叠标注中，当标注收起时，内容会被隐藏。

### 嵌套标注

你可以多层嵌套标注。

```markdown
> [!question] 标注可以嵌套吗？
> > [!todo] 可以。
> > > [!example]  你甚至可以使用多层嵌套。
```

> [!question] 标注可以嵌套吗？
> > [!todo] 可以。
> > > [!example]  你甚至可以使用多层嵌套。

### 自定义标注

[[CSS 代码片段]] 和 [[社区插件]] 可以定义自定义标注，甚至覆盖默认配置。

要定义自定义标注，创建以下 CSS 代码块：

```css
.callout[data-callout="custom-question-type"] {
    --callout-color: 0, 0, 0;
    --callout-icon: lucide-alert-circle;
}
```

`data-callout` 属性的值是你想要使用的类型标识符，例如 `[!custom-question-type]`。

- `--callout-color` 使用数字（0-255）定义背景颜色的红色、绿色和蓝色分量。
- `--callout-icon` 可以是来自 [lucide.dev](https://lucide.dev) 的图标 ID，或者一个 SVG 元素。

> [!warning] 关于 lucide 图标版本的说明
> Obsidian 定期更新 Lucide 图标。当前包含的版本如下；在自定义标注中使用这些或更早的图标。
> ![[Credits#^lucide]]

> [!tip] SVG 图标
> 除了使用 Lucide 图标，你也可以使用 SVG 元素作为标注图标。
>
> ```css
> --callout-icon: '<svg>...自定义 svg...</svg>';
> ```

### 支持的类型

你可以使用多种标注类型和别名。每种类型都带有不同的背景颜色和图标。

要使用这些默认样式，请将示例中的 `info` 替换为任何这些类型，比如 `[!tip]` 或 `[!warning]`。

除非[[#自定义标注]]，否则任何不支持的类型都会默认为 `note` 类型。类型标识符不区分大小写。

> [!note]
> ```md
> > [!note]
> > Lorem ipsum dolor sit amet
> ```

---

> [!abstract]-
> ```md
> > [!abstract]
> > Lorem ipsum dolor sit amet
> ```

别名：`summary`，`tldr`

---

> [!info]-
> ```md
> > [!info]
> > Lorem ipsum dolor sit amet
> ```

---

> [!todo]-
> ```md
> > [!todo]
> > Lorem ipsum dolor sit amet
> ```

---

> [!tip]-
> ```md
> > [!tip]
> > Lorem ipsum dolor sit amet
> ```

别名：`hint`，`important`

---

> [!success]-
> ```md
> > [!success]
> > Lorem ipsum dolor sit amet
> ```

别名：`check`，`done`

---

> [!question]-
> ```md
> > [!question]
> > Lorem ipsum dolor sit amet
> ```

别名：`help`，`faq`

---

> [!warning]-
>  ```md
> > [!warning]
> > Lorem ipsum dolor sit amet
> ```

别名：`caution`，`attention`

---

> [!failure]-
> ```md
> > [!failure]
> > Lorem ipsum dolor sit amet
> ```

别名：`fail`，`missing`

---

> [!danger]-
> ```md
> > [!danger]
> > Lorem ipsum dolor sit amet
> ```

别名：`error`

---

> [!bug]-
> ```md
> > [!bug]
> > Lorem ipsum dolor sit amet
> ```

---

> [!example]-
> ```md
> > [!example]
> > Lorem ipsum dolor sit amet
> ```

---

> [!quote]-
> ```md
> > [!quote]
> > Lorem ipsum dolor sit amet
> ```

别名：`cite`