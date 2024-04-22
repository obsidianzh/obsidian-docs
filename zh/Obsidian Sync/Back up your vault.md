---
aliases:
  - Obsidian Sync/Obsidian Sync and third-party services
---
[[Introduction to Obsidian Sync|Obsidian Sync]] is a service for syncing your notes across devices. While it offers the ability to [[Version history|restore notes]], it is **not** designed to back up your vault.

To back up your vault we recommend using a dedicated one-way backup tool that pushes data from your device to a backup location, and doesn't rewrite the data on your local device.

## Using a third-party service to back up your vault

> [!danger] Though we recommend that you regularly back up your vault, be aware that **using a third-party syncing service together with Obsidian Sync may result in data corruption or data loss**.

If you set up the same third-party service on multiple devices, such as your phone, you risk having the service competing with Obsidian Sync whenever you make changes to your vault. This can lead to conflicts, duplicated files, or corrupted files.

To back up your vault using a third-party service, configure the service so that backups are only made from your primary device. For example, if you do most of your writing on your laptop, that's where you should configure your backups. 

In the vault switcher, your vault now has a vault icon instead of a cloud, to indicate it's no longer synced to iCloud Drive. 

> [!warning] Files must be available offline
> Some cloud storage services such as OneDrive and Dropbox allow you to only download files when you use them and later remove them locally to free up space. These features are sometimes called "Files on-demand" or "Online-only files".
> 
> Since the files are no longer available locally, they will appear deleted to Obsidian Sync, and will be removed from your remote vault.
>
> To use Obsidian Sync together with OneDrive, Dropbox, or other similar services,  disable on-demand downloads. Configure the third-party service settings to always keep files on the device.

## Remove your vault from a third-party sync service

If you're using Obsidian Sync and realize that you've set up your vault in a folder synced by a third-party service, you can use the following steps to move the vault to a safer location.

### Desktop

#### Option 1: Move your vault using the vault switcher

1. In the bottom-left corner, select **Open another vault** ( ![[obsidian-icon-vault-switcher.svg#icon]] ).
2. Next to the vault you want to move, select **More options** ( ![[lucide-more-horizontal.svg#icon]] ). 
3. Choose a new location for the vault on your file system.

#### Option 2: Move your vault manually
  
1. Make backups of your vault. Copy your vault folder another location that you won't touch throughout the rest of this operation.
2. Quit Obsidian.  
3. Cut and paste (or move using drag and drop) your vault folder from the old location to your newly-selected vault location Don't put it in a folder that is being synced by another service.
4. Make sure your backup folder contains your vault.  
5. Relaunch Obsidian.  
6. At the bottom left, select **Open another vault** ( ![[obsidian-icon-vault-switcher.svg#icon]] ).
7. Select **Open folder as vault**.
8. Navigate to your vault's new location and choose your vault folder.  
9. Check and make sure the vault looks the same. You might have to re-enable community plugins under **Settings → Community Plugins → Turn restricted mode off**.)  
10. Set up Obsidian Sync again.


### Mobile

On Android, the majority of distributions will install directly to the filesystem, and the steps to relocate the vault are identical to those outlined in [[#Option 1 Move your vault using the vault switcher|move your vault using the vault switcher]].

#### iOS

1. Make a backup of your vault.
2. On your device, create a new vault and disable **Save in iCloud Drive**.
3. Force quit the Obsidian app on all your devices to prevent Sync from performing any operations while you move the files.
4. On your iOS device, open the Files app.
5. Under **iCloud Drive → Obsidian**, long-press on the vault folder and then select **Move**.
6. Navigate to **On My iPhone → Obsidian**. Make sure that you can see the vault you created earlier.
7. Press **Copy**.
5. After the vault has been copied, navigate back to **iCloud Drive → Obsidian**. 
6. Delete your vault folder.

The next time you open Obsidian, your vault now has a vault icon instead of a cloud, indicating it's no longer on iCloud Drive.


---

中文翻译：
---
别名:
  - Obsidian Sync/Obsidian Sync 和第三方服务
---

[[介绍 Obsidian Sync|Obsidian Sync]] 是一个用于在设备间同步笔记的服务。虽然它提供了[[版本历史|恢复笔记]]的功能，但**并不**旨在备份你的保险库。

为了备份你的保险库，我们建议使用专门的单向备份工具，将数据从你的设备推送到备份位置，而不会重写本地设备上的数据。

## 使用第三方服务备份你的保险库

> [!危险] 尽管我们建议定期备份你的保险库，但要注意**使用第三方同步服务与 Obsidian Sync 可能导致数据损坏或丢失**。

如果你在多个设备上设置了相同的第三方服务，比如你的手机，你就有可能在对保险库进行更改时让这些服务与 Obsidian Sync 产生冲突。这可能导致冲突、重复文件或损坏文件的出现。

要使用第三方服务备份你的保险库，配置服务使备份仅从你的主要设备进行。例如，如果你大部分时间都在笔记本电脑上写作，那就应该在那里配置你的备份。

在保险库切换器中，你的保险库现在有一个保险库图标，而不是云，以示它不再与 iCloud Drive 同步。

> [!警告] 必须保持文件离线可用
> 一些云存储服务，如 OneDrive 和 Dropbox，允许你仅在使用文件时下载它们，然后在稍后将它们从本地移除以释放空间。这些功能有时被称为“按需文件”或“仅在线文件”。
> 
> 由于这些文件不再在本地可用，它们将被 Obsidian Sync 视为已删除，并将从远程保险库中删除。
> 
> 要与 OneDrive、Dropbox 或其他类似服务一起使用 Obsidian Sync，禁用按需下载。配置第三方服务设置，始终保留设备上的文件。

## 从第三方同步服务中移除你的保险库

如果你正在使用 Obsidian Sync 并意识到你已经设置了你的保险库在一个被第三方服务同步的文件夹中，你可以按照以下步骤将保险库移动到一个更安全的位置。

### 桌面端

#### 选项 1：使用保险库切换器移动你的保险库

1. 在左下角，选择**打开另一个保险库**（ ![[obsidian-icon-vault-switcher.svg#icon]] ）。
2. 在要移动的保险库旁，选择**更多选项**（ ![[lucide-more-horizontal.svg#icon]] ）。
3. 为你的保险库在文件系统上选择一个新位置。

#### 选项 2：手动移动你的保险库

1. 备份你的保险库。将你的保险库文件夹复制到另一个在整个操作过程中不会触碰的位置。
2. 退出 Obsidian。
3. 剪切并粘贴（或拖放移动）你的保险库文件夹，从旧位置移动到你新选择的保险库位置。不要放在另一个服务正在同步的文件夹中。
4. 确保你的备份文件夹包含你的保险库。
5. 重新启动 Obsidian。
6. 在左下角，选择**打开另一个保险库**（ ![[obsidian-icon-vault-switcher.svg#icon]] ）。
7. 选择**作为保险库打开文件夹**。
8. 导航到你保险库的新位置并选择你的保险库文件夹。
9. 检查并确保保险库看起来一样。你可能需要在**设置 → 社区插件 → 关闭限制模式**下重新启用社区插件。
10. 重新设置 Obsidian Sync。

### 移动端

在安卓系统上，大多数发行版将直接安装到文件系统中，将保险库重新定位的步骤与[[#选项 1：使用保险库切换器移动你的保险库|使用保险库切换器移动你的保险库]]中概述的步骤相同。

#### iOS

1. 备份你的保险库。
2. 在你的设备上，创建一个新的保险库，并禁用**保存在 iCloud Drive**。
3. 强制关闭所有设备上的 Obsidian 应用，以防止同步在你移动文件时执行任何操作。
4. 在你的 iOS 设备上，打开文件应用。
5. 在**iCloud Drive → Obsidian**下，长按保险库文件夹，然后选择**移动**。
6. 导航到**我的 iPhone → Obsidian**。确保你能看到之前创建的保险库。
7. 点击**复制**。
8. 复制完成后，导航回**iCloud Drive → Obsidian**。
9. 删除你的保险库文件夹。

下次打开 Obsidian 时，你的保险库现在有一个保险库图标，而不是云，表示它不再在 iCloud Drive 上。