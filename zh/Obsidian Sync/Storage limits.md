---
aliases:
  - Obsidian Sync/Remote vault size limit
---
The amount of data you can store using [[Introduction to Obsidian Sync|Obsidian Sync]] is defined by your subscription plan. Additional Sync storage can be purchased up to 100 GB via your [account dashboard](https://obsidian.md/account). See [[Sync limitations]] for more details.

There is a single account-wide storage limit for all notes across your vaults. [[Version history]] and [[附件]] are also counted towards your account's storage limit.

When you reach your account's storage limit, the Sync plugin will cease syncing files, and you will be prompted to prune your remote vault(s).

## Identify and delete large files

To identify and delete large files from the vault:

1. Open **Settings → Sync**.
2. Select **View largest files** next to **Vault size over limit**. 
	1. If you don’t see **Vault size over limit**, it means ==you haven’t hit the size limit== yet.
3. Close the **View largest files** modal.
4. Delete some of the large files you no longer need.
5. Wait for Obsidian sync to finish the task. This can take a while.
6. Open **Settings → Sync**.
7. Select **Prune** next to **Vault size over limit**. This will remove the deleted files from the remote vault to free up space.

After the prune syncs to the server, Obsidian Sync should resume functioning.

## Create a new remote vault

You can **create a new remote vault** to exclude large files before syncing. The version history for your files will be reset if you create a new remote vault. Please be sure that you don’t need version history for older files before proceeding.

To sync to a new remote vault, follow these steps:

1. Open **Settings → Sync**.
2. Select **Manage** next to **Remote vault**.
3. Choose **Create new vault** and follow the steps to create it. If you run out of vaults, you might need to disconnect from the current remote vault and delete it first.
4. Set up excluded files before you start syncing to the new remote vault (optional).
5. Start syncing to the new remote vault.

The new remote vault should be smaller than the previous vault, because of the absence of version history and excluded files.


---

中文翻译：
---
别名:
  - Obsidian Sync/远程仓库大小限制
---
你可以使用[[Introduction to Obsidian Sync|Obsidian Sync]]存储的数据量由你的订阅计划确定。额外的同步存储空间可以通过你的[账户仪表板](https://obsidian.md/account)购买，最多可扩展至100 GB。查看[[同步限制]]以获取更多详情。

所有笔记本中的笔记都有一个统一的账户存储限制。[[版本历史]]和[[附件]]也计入账户的存储限制范围。

当你达到账户存储限制时，同步插件将停止同步文件，并提示你清理远程仓库。

## 辨识并删除大文件

要辨识并删除仓库中的大文件：

1. 打开**设置 → 同步**。
2. 选择**查看最大文件**，位于**仓库大小超出限制**旁边。
	1. 如果你看不到**仓库大小超出限制**，这意味着==你还没有达到存储限制==。
3. 关闭**查看最大文件**模态窗口。
4. 删除一些你不再需要的大文件。
5. 等待 Obsidian 同步完成任务。这可能需要一些时间。
6. 打开**设置 → 同步**。
7. 选择**修剪**，位于**仓库大小超出限制**旁边。这将从远程仓库中删除已删除的文件以释放空间。

在修剪同步到服务器后，Obsidian Sync 应该会恢复正常运行。

## 创建新的远程仓库

你可以**创建一个新的远程仓库**，在同步之前排除大文件。如果你创建一个新的远程仓库，文件的版本历史将被重置。在继续之前，请确保你不需要对旧文件的版本历史。

要同步到新的远程仓库，请按照以下步骤操作：

1. 打开**设置 → 同步**。
2. 选择**管理**，位于**远程仓库**旁边。
3. 选择**创建新仓库**，并按照步骤创建。如果你的仓库用完了，你可能需要先断开当前远程仓库的连接并删除它。
4. 在开始向新远程仓库同步之前设置排除的文件（可选）。
5. 开始向新远程仓库同步。

新的远程仓库应该比之前的仓库小，因为没有版本历史和排除的文件。