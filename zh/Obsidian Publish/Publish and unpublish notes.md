This page explains how to manage your published notes.

## Publish notes

1. In ribbon, to the left of the application window, click **Publish changes** (paper plane icon).
2. In the **Publish changes** dialog, click **NEW** to see all the notes you haven't published yet.
3. Select the notes you want to publish.
4. Click **Publish**.

## Unpublish notes

Notes remain in your local vault even after you unpublish them.

1. In ribbon, to the left of the application window, click **Publish changes** (paper plane icon).
2. In the **Publish changes** dialog, click **UNCHANGED** to see all your published notes.
3. Select the notes you want to unpublish.
4. Click **Publish**.

## Update a published note

1. In ribbon, to the left of the application window, click **Publish changes** (paper plane icon).
2. In the **Publish changes** dialog, click **CHANGED** to see all the notes that have been changed since the last time they were published.
3. Select the notes you want to update.
4. Click **Publish**.

## Publish linked notes

Publishing notes that have links to other notes results in broken links unless you publish the linked notes as well. Obsidian Publish can help you by selecting notes that are linked from the notes that are already selected.

To select all linked notes, click **Add linked** in the **Publish changes** dialog.

Review the updated selection to make sure it doesn't include any notes that you're not ready to publish yet.

## Automatically select notes to publish

To automatically select a note to be published, set `publish: true` in the [[属性]] for the note.

## Ignore notes

To ignore a note in Obsidian Publish, set `publish: false` in the [[属性]] for the note.

The note no longer shows up in the list of notes to publish.

## Permalinks

You can rename the URL to your notes, using _permalinks_.

For example, you can turn this:

```
https://publish.obsidian.md/username/Company/About+us
```

Into this:

```
https://publish.obsidian.md/username/about
```

To create a permalink for a note, add the `permalink` property to your [[属性]].

```yaml
---
permalink: about
---
```

If someone visits a note using the original URL, they'll be automatically redirected to the permalink.


---

中文翻译：
这个页面详细介绍了如何管理你发布的笔记。

## 发布笔记

1. 在应用程序窗口左侧的功能区，点击**发布更改**（纸飞机图标）。
2. 在**发布更改**对话框中，点击**NEW**查看所有尚未发布的笔记。
3. 选择你想要发布的笔记。
4. 点击**发布**。

## 取消发布笔记

即使取消发布，笔记仍保留在本地仓库中。

1. 在应用程序窗口左侧的功能区，点击**发布更改**（纸飞机图标）。
2. 在**发布更改**对话框中，点击**UNCHANGED**查看所有已发布的笔记。
3. 选择你想要取消发布的笔记。
4. 点击**发布**。

## 更新已发布的笔记

1. 在应用程序窗口左侧的功能区，点击**发布更改**（纸飞机图标）。
2. 在**发布更改**对话框中，点击**CHANGED**查看自上次发布以来已更改的所有笔记。
3. 选择你想要更新的笔记。
4. 点击**发布**。

## 发布相互链接的笔记

发布具有其他笔记链接的笔记会导致断链，除非同时发布这些链接的笔记。Obsidian Publish 可以通过选择已从已选择的笔记链接的笔记来帮助您。

要选择所有链接的笔记，请在**发布更改**对话框中点击**添加链接**。

请仔细检查更新后的选择，确保不包含尚未准备好发布的笔记。

## 自动选择要发布的笔记

要自动选择要发布的笔记，请在笔记的[[属性]]中设置`publish: true`。

## 忽略笔记

要在 Obsidian Publish 中忽略一个笔记，请在笔记的[[属性]]中设置`publish: false`。

该笔记将不再显示在要发布的笔记列表中。

## 永久链接

你可以使用 _永久链接_ 为笔记的 URL 进行重命名。

例如，你可以将这个 URL：

```
https://publish.obsidian.md/username/Company/About+us
```

变为：

```
https://publish.obsidian.md/username/about
```

要为笔记创建永久链接，请在[[属性]]中添加`permalink`属性。

```yaml
---
permalink: about
---
```

如果有人使用原始 URL 访问笔记，他们将被自动重定向到永久链接。