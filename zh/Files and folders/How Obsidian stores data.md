---
aliases: Advanced topics/How Obsidian stores data
---
Obsidian stores your notes as [[Basic formatting syntax|Markdown-formatted]] plain text files in a _vault_. A vault is a folder on your local file system, including any subfolders.

Because notes are plain text files, you can use other text editors and file managers to edit and manage notes. Obsidian automatically refreshes your vault to keep up with any external changes.

You can create a vault anywhere your operating system allows. Obsidian syncs with [[Introduction to Obsidian Sync|Obsidian Sync]], Dropbox, iCloud, OneDrive, Git, and many other third-party services.

You can open multiple folders as individual vaults, for example to separate notes for work and personal use.

> [!warning] Vaults within vaults
> Because [[Internal links]] are local to a vault, we recommend that you don't create vaults within vaults. Links may not be updated correctly.

## Vault settings

Obsidian creates an `.obsidian` [[configuration folder]] in the root folder of the vault, which contains preferences specific to that vault, such as [[hotkeys]], [[themes]], and [[community plugins]].

By default, most operating systems hide folders that start with a period (`.`), so you may need to update the settings for your file manager to see it.

- **macOS**: In Finder, press `Cmd+Shift+.` (period) to show hidden files.
- **Windows**: [Show hidden files](https://support.microsoft.com/en-us/windows/show-hidden-files-0320fe58-0117-fd59-6851-9b7f9840fdb2)

> [!tip] Adding `.obsidian` to Git
> The `.obsidian/workspace` file stores the current workspace layout, and changes any time you open a new file. If you use [Git](https://git-scm.com) to version control your vault, you may want to add the `.obsidian/workspace` file to `.gitignore`.

## Global settings

Obsidian stores global settings in a system folder. The location of the system folder depends on the operating system you're using.

- **macOS**: `/Users/yourusername/Library/Application Support/obsidian`
- **Windows**: `%APPDATA%\Obsidian\`
- **Linux**: `$XDG_CONFIG_HOME/Obsidian/` or `~/.config/Obsidian/`

> [!warning]
> Don't create a vault in the system folder. This may lead to corrupted data or data loss.


---

中文翻译：
---
aliases: Obsidian 数据存储方式
---
Obsidian 将你的笔记以[[基本格式语法|Markdown格式]]的纯文本文件形式存储在一个名为 _vault_ 的文件夹中。Vault 是你本地文件系统上的一个文件夹，包括其中的任何子文件夹。

由于笔记是纯文本文件，你可以使用其他文本编辑器和文件管理器来编辑和管理笔记。Obsidian 会自动刷新你的 vault，以跟上任何外部更改。

你可以在操作系统允许的任何位置创建一个 vault。Obsidian 可以与[[介绍 Obsidian Sync|Obsidian Sync]]、Dropbox、iCloud、OneDrive、Git 和许多其他第三方服务同步。

你可以将多个文件夹作为单独的 vault 打开，例如为工作和个人用途分开笔记。

> [!警告] 嵌套的 vault
> 因为[[内部链接]]是相对于一个 vault 的，我们建议不要在 vault 中创建嵌套的 vault。链接可能无法正确更新。

## Vault 设置

Obsidian 在 vault 的根文件夹中创建一个名为 `.obsidian` 的[[配置文件夹]]，其中包含特定于该 vault 的偏好设置，如[[快捷键]]、[[主题]]和[[社区插件]]。

默认情况下，大多数操作系统会隐藏以句点（`.`）开头的文件夹，所以你可能需要更新文件管理器的设置才能看到它。

- **macOS**：在 Finder 中，按 `Cmd+Shift+.`（句点）显示隐藏文件。
- **Windows**：[显示隐藏文件](https://support.microsoft.com/zh-cn/windows/show-hidden-files-0320fe58-0117-fd59-6851-9b7f9840fdb2)

> [!提示] 将 `.obsidian` 添加到 Git
> `.obsidian/workspace` 文件存储当前的工作区布局，并在打开新文件时更改。如果你使用 [Git](https://git-scm.com) 来对 vault 进行版本控制，可能需要将 `.obsidian/workspace` 文件添加到 `.gitignore` 中。

## 全局设置

Obsidian 将全局设置存储在系统文件夹中。系统文件夹的位置取决于你正在使用的操作系统。

- **macOS**：`/Users/你的用户名/Library/Application Support/obsidian`
- **Windows**：`%APPDATA%\Obsidian\`
- **Linux**：`$XDG_CONFIG_HOME/Obsidian/` 或 `~/.config/Obsidian/`

> [!警告]
> 不要在系统文件夹中创建 vault。这可能导致数据损坏或数据丢失。