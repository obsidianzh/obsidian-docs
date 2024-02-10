---
aliases: 
- alias
- aliases
- How to/Add aliases to note
---

If you want to reference a file using different names, consider adding _aliases_ to the note. An alias is an alternative name for a note.

Use aliases for things like acronyms, nicknames, or to refer to a note in a different language.

## Add an alias to a note

To add an alias for a note, add `aliases` property in the note [[Properties]]. Aliases should always be formatted as a list in YAML.

```md
---
aliases:
  - Doggo
  - Woofer
  - Yapper
---

# Dog
```

## Link to a note using an alias

To link to a note using an alias:

1. Start typing the alias in an [[Internal links|internal link]]. Any alias shows up in the list of suggestions, with a curved arrow icon next to it.
2. Press `Enter` to select the alias.

Obsidian creates the link with the alias as its custom display text, for example `[[Artificial Intelligence|AI]]`.

> [!note]
> Rather than just using the alias as the link destination (`[[AI]]`), Obsidian uses the `[[Artificial Intelligence|AI]]` link format to ensure interoperability with other applications using the Wikilink format.

## Find unlinked mentions for an alias

By using [[Backlinks]], you can find unlinked mentions of aliases.

For example, after setting "AI" as an alias for "Artificial intelligence", you can see mentions of "AI" in other notes.

If you link an unlinked mention to an alias, Obsidian turns the mention into an [[Internal links|internal link]] with the alias as its display text.


---

中文翻译：
---
aliases: 
- 别名
- 别称
- 如何/向笔记添加别名
---

如果你想用不同的名称引用一个文件，可以考虑向笔记添加_别名（aliases）_。别名是笔记的另一个名称。

可以使用别名来表示首字母缩写、昵称，或者用不同语言引用笔记。

## 向笔记添加别名

要为笔记添加别名，在笔记[[属性]]中添加 `aliases` 属性。别名应该以 YAML 列表的格式编写。

```md
---
aliases:
  - Doggo
  - Woofer
  - Yapper
---

# 狗
```

## 使用别名链接到笔记

要使用别名链接到笔记：

1. 在[[内部链接|内部链接]]中开始输入别名。所有别名会在建议列表中显示，旁边有一个弯曲箭头图标。
2. 按 `Enter` 键选择别名。

Obsidian会创建带有别名的链接作为其自定义显示文本，例如 `[[人工智能|AI]]`。

> [!注意]
> Obsidian 使用 `[[人工智能|AI]]` 链接格式，而不只是使用别名作为链接目标（`[[AI]]`），以确保与其他使用 Wikilink 格式的应用程序的互操作性。

## 查找别名的未链接提及

通过使用[[反向链接]]，你可以找到别名的未链接提及。

例如，将“AI”设置为“人工智能”的别名后，你可以在其他笔记中看到“AI”的提及。

如果你将未链接提及链接到别名，Obsidian会将提及转换为带有别名的[[内部链接|内部链接]]作为其显示文本。