---
permalink: import/zettelkasten
---
If you've been using the Zettelkasten method to name and link your notes, you may need to convert links from `[[UID]]` to `[[UID My note title]]`.

For example, if you have a note with the name `202301011230 My note title` and link to it from another note using only the UID, `[[202301011230]]`. Since Obsidian uses the full name of the note to resolve internal links, links like these will break.

To update all `[[UID]]` links in your vault to use the full name of the note instead, use the [[Format converter]].

1. Open **Settings**.
2. Under **Core plugins**, enable **Format converter** and close the Settings window.
3. In the ribbon, on the left side of the app window, select **Open format convert** (ones and zeros icon).
4. Enable **Zettelkasten link fixer**.
5. Select **Start conversion**. This will convert all the notes in your entire vault.

> [!tip] Zettelkasten link beautifier
> [[Format converter]] can also beautify your links by removing the UID from the display name. For example, `[[UID]]` converts to `[[UID My note title|My note title]]`.
>
> To beautify your Zettelkasten links, enable **Zettelkasten link beautifier** in the format converter window.

You can also use the [[Unique note creator]] to create Zettelkasten notes in Obsidian.

---

中文翻译：
---
permalink: import/zettelkasten
---
如果你一直在使用 Zettelkasten 方法来命名和链接你的笔记，那么你可能需要将链接从 `[[UID]]` 转换为 `[[UID 笔记标题]]`。

举个例子，如果你有一个名为 `202301011230 笔记标题` 的笔记，并且在另一个笔记中仅使用 UID `[[202301011230]]` 进行链接。由于 Obsidian 使用笔记的全名来解析内部链接，这样的链接将会失效。

要将仓库中所有的 `[[UID]]` 链接更新为使用笔记的全名，可以使用[[Format converter]]。

1. 打开 **设置**。
2. 在 **核心插件** 下，启用 **格式转换器** 并关闭设置窗口。
3. 在应用窗口左侧的工具栏中，选择 **打开格式转换**（一和零的图标）。
4. 启用 **Zettelkasten 链接修复工具**。
5. 选择 **开始转换**。这将转换仓库中的所有笔记。

> [!提示] Zettelkasten 链接美化器
> [[Format converter]] 还可以通过从显示名称中删除 UID 来美化你的链接。例如，`[[UID]]` 转换为 `[[UID 笔记标题|笔记标题]]`。
>
> 要美化你的 Zettelkasten 链接，请在格式转换窗口中启用 **Zettelkasten 链接美化器**。

你也可以使用[[Unique note creator]]在 Obsidian 中创建 Zettelkasten 笔记。