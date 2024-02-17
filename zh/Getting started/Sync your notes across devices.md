Syncing means keeping your notes up to date across your devices, such as your laptop and phone.

The easiest way to sync your notes between your devices is to use [[Introduction to Obsidian Sync|Obsidian Sync]]. If you already have an Obsidian Sync subscription, see how to [[Set up Obsidian Sync]].

Note that using multiple syncing services at the same time (e.g., Obsidian Sync _and_ Dropbox) may cause data loss, corruption, and other issues. [[Back up your vault|Find out more about using Obsidian Sync with other services here.]]

> [!important] Dealing with on-demand cloud storage
> Some cloud storage services, such as OneDrive, allow you to only download files when you use them and later remove them locally to free up space. Since the files are no longer available locally, Obsidian Sync believes they've been deleted and removes them from your remote vault.
>
> To use Obsidian Sync together with Files On-Demand and similar features, make sure to configure the service to always keep the files on the device.
^sync-files-on-demand

If you don't want to use Obsidian Sync, this page lists alternative methods for syncing your vaults with multiple devices.
## Sync notes across multiple desktops

If you don't use Obsidian on your mobile devices, you can use any third-party service that syncs a local folder to a cloud storage.

For example, you can use any of the following services:

- Dropbox
- Google Drive
- iCloud Drive
- OneDrive
- Syncthing

To sync your notes, follow the instructions for the service you're using to sync a folder on your local file system. Then open the folder as an existing vault on all your desktop devices.

## Sync your notes on iPhone and iPad

To sync your notes to your iPhone or iPad, we officially support the following options:

- [[Introduction to Obsidian Sync|Obsidian Sync]]
- [[#iCloud Drive]]

**Note:** The following services aren't supported. If you discover a way to sync your notes on your iOS device using any of these services, let us know on our community channels.

- Dropbox
- Google Drive
- OneDrive
- Syncthing

### iCloud Drive

Obsidian can use iCloud Drive as a local file system.

When utilizing iCloud Drive on macOS, make sure to upgrade your desktop app's installer version to v0.13.0 or later. Additionally, ensure that you do not surpass your iCloud storage limit, as exceeding it could lead to syncing interruptions.

> [!tip]
> Ensure that you disable "**Optimize Mac Storage**" in iCloud Drive's settings before syncing your Obsidian vault using iCloud Drive on macOS. Failing to disable this feature could cause iCloud Drive to offload your files, rendering them unusable by Obsidian, and potentially leading to unexpected behavior.

#### Create a new vault in iCloud Drive

To create a new vault in iCloud Drive on your iPhone or iPad:

1. Tap **Create new vault**.
2. In **Vault name**, enter the name of your vault.
3. Enable **Store in iCloud**.
4. Tap **Create**.

Obsidian has created a new folder inside your iCloud Drive. To open the iCloud Drive folder as a vault on your computer:

1. On your computer, open **Obsidian**.
2. At the right of **Open folder as vault**, select **Open**.
3. Navigate to **iCloud Drive → Obsidian**.
4. Select the folder with the name of the vault you want to sync with.

#### Sync an existing vault with iCloud Drive

To sync an existing vault using iCloud, you need to create an empty vault in iCloud Drive and then move your notes on your other device to the empty vault.

To create a new empty vault in iCloud Drive:

1. Tap **Create new vault**.
2. In **Vault name**, enter the same name as the vault you want to sync with.
3. Enable **Store in iCloud**.
4. Tap **Create**.

To move your notes to the new vault in your iCloud Drive:

1. On your computer, open the **iCloud Drive** folder.
2. Open the **Obsidian** folder. It might take a few minutes to appear.
3. Move the files in your existing vault to the folder with the name of your vault.

iCloud syncs the files to your mobile device. Depending on the size of your vault, this might take a few minutes.

### Working Copy

If you store your notes in a [Git](https://git-scm.com/) repository, you may want to look at [Working Copy](https://apps.apple.com/us/app/working-copy-git-client/id896694807)—a Git client for your iOS.

To sync using Working Copy:

1. Create an empty vault on your iPhone or iPad.
2. Use the **Setup Folder Sync** action and select your empty vault.
3. Commit and push any changes to your vault using the Working Copy app.

**Note:** While we don't officially support this method, several of our users have reported that they've successfully used Working Copy to sync their notes.

### Why can't I sync using X?

We understand that many of you use other services for syncing files and you'd prefer to use it for syncing your notes as well.

Obsidian works differently from other Markdown editors on iOS. Editors such as 1Writer and iA Writer access one note at a time, which lets them use built-in support for documents.

In contrast, many features in Obsidian need access to your entire vault. For example if you rename a file, then Obsidian needs to update all files in the vault that links to that file.

Implementing a system to read, modify, and monitor an entire folder structure comprising of possibly thousand of notes outside of the supported locations is challenging. We hope to address this limitation in the future.

If you're a developer, you can build a plugin that uses the Web APIs for each individual sync service.

### Where are my vaults stored?

If you choose not to use iCloud Drive when you create your vault, Obsidian stores it in a local file system for the Obsidian app. Other apps, such as [[#Working Copy]], can access your vault by selecting the vault from the file system.

**Caution:** Any notes stored in the local file system are deleted by iOS when you uninstall the app. Make sure to back up your notes before you uninstall the Obsidian app.

## Sync notes on Android

The easiest way to sync your notes on your Android device is using [[Introduction to Obsidian Sync|Obsidian Sync]].

Since Obsidian stores notes in a local folder on your Android device, you can also use any app that let you sync a folder, such as:

- [Dropsync](https://play.google.com/store/apps/details?id=com.ttxapps.dropsync)
- [FolderSync](https://play.google.com/store/apps/details?id=dk.tacit.android.foldersync.lite)

**Note:** Obsidian creates an Obsidian folder in the shared Documents folder. Any folder under `Documents/Obsidian` is considered an Obsidian vault.

## Config folders

You can utilize the ability to change your configuration folder per device, to maintain device specific settings even when using a syncing service. 

![[设置文件夹#Changing your config folder]]


---

中文翻译：
同步意味着在不同设备上保持笔记内容的最新状态，比如在笔记本电脑和手机之间。

在多个设备之间同步笔记的最简单方法是使用[[Introduction to Obsidian Sync|Obsidian Sync]]。如果你已经订阅了 Obsidian Sync，请查看如何[[Set up Obsidian Sync|设置 Obsidian Sync]]。

请注意，同时使用多个同步服务（例如 Obsidian Sync _和_ Dropbox）可能会导致数据丢失、损坏以及其他问题。[[Back up your vault|在这里了解如何在 Obsidian Sync 中使用其他服务。]]

> [!重要] 处理按需云存储
> 一些云存储服务（如 OneDrive）允许你在使用文件时仅下载文件，然后稍后将其从本地移除以释放空间。由于文件不再在本地可用，Obsidian Sync 认为它们已被删除，并将其从远程仓库中移除。
>
> 若要在 Files On-Demand 和类似功能中使用 Obsidian Sync，请确保将服务配置为始终保留设备上的文件。
^sync-files-on-demand

如果你不想使用 Obsidian Sync，在这个页面列出了将你的仓库与多个设备同步的替代方法。

## 在多个桌面端同步笔记

如果你不在移动设备上使用 Obsidian，你可以使用任何将本地文件夹同步到云存储的第三方服务。

例如，你可以使用以下任何服务：

- Dropbox
- Google Drive
- iCloud Drive
- OneDrive
- Syncthing

要同步你的笔记，请按照你使用的服务的说明将本地文件夹同步。然后在所有桌面设备上将该文件夹作为现有仓库打开。

## 在 iPhone 和 iPad 上同步你的笔记

要将笔记同步到 iPhone 或 iPad 上，我们官方支持以下选项：

- [[Introduction to Obsidian Sync|Obsidian Sync]]
- [[#iCloud Drive]]

**注意：** 以下服务不受支持。如果你发现使用这些服务在 iOS 设备上同步笔记的方法，请在我们的社区渠道上告诉我们。

- Dropbox
- Google Drive
- OneDrive
- Syncthing

### iCloud Drive

Obsidian 可以使用 iCloud Drive 作为本地文件系统。

在 macOS 上使用 iCloud Drive 时，请确保将桌面应用的安装程序版本升级到 v0.13.0 或更高版本。此外，请确保不超过 iCloud 存储限制，否则可能会导致同步中断。

> [!提示]
> 在 macOS 上使用 iCloud Drive 同步 Obsidian 仓库之前，请确保在 iCloud Drive 的设置中禁用“**优化 Mac 存储**”。未禁用此功能可能导致 iCloud Drive 卸载你的文件，使它们无法被 Obsidian 使用，并可能导致意外行为。

#### 在 iCloud Drive 中创建新仓库

要在 iPhone 或 iPad 的 iCloud Drive 中创建新仓库：

1. 点击**创建新仓库**。
2. 在**仓库名称**中输入你的仓库名称。
3. 启用**存储在 iCloud 中**。
4. 点击**创建**。

Obsidian 已在你的 iCloud Drive 中创建了一个新文件夹。要在计算机上将 iCloud Drive 文件夹作为仓库打开：

1. 在你的计算机上，打开**Obsidian**。
2. 在**打开文件夹作为仓库**右侧，选择**打开**。
3. 导航到**iCloud Drive → Obsidian**。
4. 选择与你想同步的仓库名称相同的文件夹。

#### 使用 iCloud Drive 同步现有仓库

要使用 iCloud 同步现有仓库，你需要在 iCloud Drive 中创建一个空仓库，然后将你另一台设备上的笔记移动到这个空仓库中。

在 iCloud Drive 中创建一个新的空仓库：

1. 点击**创建新仓库**。
2. 在**仓库名称**中输入与你想同步的仓库相同的名称。
3. 启用**存储在 iCloud 中**。
4. 点击**创建**。

将你的笔记移动到 iCloud Drive 中的新仓库中：

1. 在你的计算机上，打开**iCloud Drive**文件夹。
2. 打开**Obsidian**文件夹。可能需要几分钟才会出现。
3. 将现有仓库中的文件移到与你的仓库名称相同的文件夹中。

iCloud 会将文件同步到你的移动设备。根据你的仓库大小，这可能需要几分钟。

### Working Copy

如果你将笔记存储在 [Git](https://git-scm.com/) 仓库中，你可能想看看 [Working Copy](https://apps.apple.com/us/app/working-copy-git-client/id896694807)——一个适用于 iOS 的 Git 客户端。

使用 Working Copy 进行同步：

1. 在你的 iPhone 或 iPad 上创建一个空仓库。
2. 使用 **设置文件夹同步** 操作并选择你的空仓库。
3. 使用 Working Copy 应用程序提交并推送任何更改到你的仓库。

**注意：** 虽然我们没有官方支持这种方法，但我们的许多用户报告说他们成功地使用 Working Copy 同步他们的笔记。

### 为什么不能使用 X 进行同步？

我们了解到许多用户使用其他服务来同步文件，并希望将其用于同步笔记。

Obsidian 在 iOS 上的工作方式与其他 Markdown 编辑器不同。诸如 1Writer 和 iA Writer 等编辑器一次只访问一个笔记，这使它们可以使用内置的文档支持。

相比之下，Obsidian 的许多功能需要访问你的整个仓库。例如，如果你重命名一个文件，那么 Obsidian 需要更新链接到该文件的仓库中的所有文件。

在不受支持的位置之外读取、修改和监视包含可能有成千上万个笔记的整个文件夹结构的系统是具有挑战性的。我们希望在未来解决这个限制。

如果你是开发者，你可以构建一个使用每个个体同步服务的 Web API 的插件。

### 我的仓库存储在哪里？

如果你选择不使用 iCloud Drive 来创建你的仓库，Obsidian 将其存储在本地文件系统中的应用程序文件夹中。其他应用程序，如[[#Working Copy]]，可以通过从文件系统中选择仓库来访问你的仓库。

**注意：** 当你卸载该应用时，iOS 会删除存储在本地文件系统中的任何笔记。请确保在卸载 Obsidian 应用程序之前备份你的笔记。

## 在 Android 上同步笔记

在 Android 设备上同步笔记的最简单方法是使用[[Introduction to Obsidian Sync|Obsidian Sync]]。

由于 Obsidian 将笔记存储在 Android 设备上的本地文件夹中，你也可以使用任何允许你同步文件夹的应用程序，例如：

- [Dropsync](https://play.google.com/store/apps/details?id=com.ttxapps.dropsync)
- [FolderSync](https://play.google.com/store/apps/details?id=dk.tacit.android.foldersync.lite)

**注意：** Obsidian 在共享文档文件夹中创建了一个 Obsidian 文件夹。`Documents/Obsidian` 下的任何文件夹都被视为一个 Obsidian 仓库。

## 配置文件夹

你可以利用每台设备更改配置文件夹的功能，以保持设备特定设置，即使使用同步服务也可以。

![[设置文件夹#Changing your config folder]]