---
aliases:
  - Obsidian Publish/Redirecting old notes
---
Renaming and removing notes is a natural part of maintaining a living vault. While Obsidian automatically updates links when you move a note within your local vault, other websites may still link to your old notes on your published [[Introduction to Obsidian Publish|Obsidian Publish]] site. In this article, you'll learn how to redirect readers from one note to another.

Imagine you want to move a note from one folder to another:

- **Guides**
  - ~~Making friends.md~~ (removed)
- **Tutorials**
  - *How to make friends.md* (added)

After you move the note, Obsidian automatically updates all links within the vault. However, if you publish the change to your Publish site, any links to `/Guides/Making+friends` will result in a 404.

To redirect readers from `/Guides/Making+friends` to `/Tutorials/How+to+make+friends`, you need to add an [[Aliases|alias]] in `How to make friends.md`, the note you want to redirect to.

```md
---
alias: Guides/Making friends
---

# How to make friends
```

> [!important]
> Make sure that you include the full path to the old note in the alias. While using only the note name as an alias works in your local vault, Publish needs the full path to the note to be able to redirect to it.

You can redirect multiple notes by adding an alias for each.

```md
---
aliases: 
  - Guides/Making friends
  - Developing friendships
---

# How to make friends
```

---

中文翻译：
重命名和删除笔记是维护活跃知识库的自然过程。虽然 Obsidian 在您本地知识库内移动笔记时会自动更新链接，但其他网站可能仍链接到您发布的[[Obsidian Publish简介|Obsidian Publish]]站点上的旧笔记。在本文中，您将学会如何将读者从一个笔记重定向到另一个笔记。

假设您想将一个笔记从一个文件夹移动到另一个文件夹：

- **指南**
  - ~~交友指南.md~~（已删除）
- **教程**
  - *如何交朋友.md*（已添加）

移动笔记后，Obsidian 会自动更新知识库内的所有链接。然而，如果您将更改发布到您的发布站点，任何链接到`/Guides/Making+friends`的链接都将导致404错误。

要将读者从`/Guides/Making+friends`重定向到`/Tutorials/How+to+make+friends`，您需要在`How to make friends.md`中添加一个[[别名|alias]]。

```md
---
alias: Guides/Making friends
---

# 如何交朋友
```

> [!重要]
> 确保在别名中包含旧笔记的完整路径。虽然在本地知识库中仅使用笔记名称作为别名可以正常工作，但发布站点需要笔记的完整路径才能进行重定向。

您可以通过为每个笔记添加一个别名来重定向多个笔记。

```md
---
aliases: 
  - Guides/Making friends
  - Developing friendships
---

# 如何交朋友
```