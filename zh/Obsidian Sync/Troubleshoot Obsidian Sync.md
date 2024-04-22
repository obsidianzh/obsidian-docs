This page lists common issues that you might encounter, and how to address them.

![[同步笔记#^sync-files-on-demand]]

## Conflict resolution

A conflict happens when you make changes to the same file on two or more devices between syncs. For example, you might have changed a file on your computer, and before that change is uploaded, you also change the same file on your phone.

Conflicts usually happen more frequently if you work offline, since there are more changes and a longer period of time between syncs and thus more potential conflicts.

When Sync downloads a new version of a file, and finds that there are conflicts with the local version, the changes are merged with Google's [diff-match-patch](https://github.com/google/diff-match-patch) algorithm.

> [!help] To find when conflicts have happened, you can search for "Merging conflicted file" in **Settings → Sync → Sync activity → View**.

## Obsidian Sync deleted a note I just created on two devices

Generally, Obsidian Sync tries to [[#Conflict resolution|resolve conflicts]] between devices by merging the content of the conflicting notes. Unfortunately, merging conflicting notes can cause issues for users who *automatically generate* or *alter notes* on startup, for example using [[Daily notes]].

If a note was created locally on a device less than a couple of minutes before Sync downloads a remote version of that note, then Sync keeps the remote version without attempting to merge the two. You can still recover the local version using [[File recovery]].

## What does "Vault limit exceeded" mean?

Your account exceeds the [[Sync limitations#How large can each remote vault be|maximum size of 50 GB]]. See [[Storage limits]].

Since attachments and version history contributes to the total size of your vault, your vault can exceed the maximum size even if the actual size of your vault is less than the limit.

To identify and purge large files from the vault:

1. Open **Settings → Sync**.
2. Explore the options under **Vault size over limit** for how you can reduce the size of your vault.

## What does "Vault not found" mean?

`{"res":"err","msg":"Vault not found."}`

This error may occur in the following scenarios:

1. The vault has been deleted from another device for any reason.
2. The sync subscription was inactive for over 30 days, leading to the removal of the remote vault.
3. The subscription was canceled or refunded, resulting in the purging of the remote vault.

In each case, it is necessary to disconnect from the remote vault and establish a new connection, ensuring the data on your device is retained.

---

中文翻译：
这个页面列出了你可能遇到的常见问题以及解决方法。

![[跨设备同步笔记#^按需同步文件]]

## 冲突解决

当你在两个或多个设备上的同一文件进行同步之间进行更改时，就会发生冲突。例如，你可能在电脑上更改了一个文件，在上传这些更改之前，你也在手机上更改了同一个文件。

通常情况下，如果你在离线状态下工作，冲突会更频繁发生，因为同步之间的更改更多，时间间隔更长，因此潜在的冲突也更多。

当同步下载一个文件的新版本，并发现与本地版本存在冲突时，这些更改会使用谷歌的[diff-match-patch](https://github.com/google/diff-match-patch)算法进行合并。

> [!帮助] 要查找冲突发生的时间，你可以在**设置 → 同步 → 同步活动 → 查看**中搜索"Merging conflicted file"。

## Obsidian Sync 删除了我在两台设备上刚创建的一个笔记

通常情况下，Obsidian Sync会尝试[[#Conflict resolution|解决设备之间的冲突]]，通过合并冲突笔记的内容。不幸的是，合并冲突笔记可能会对那些在启动时*自动生成*或*修改笔记*的用户造成问题，例如使用[[每日笔记]]。

如果一个笔记是在一个设备上本地创建的，而在同步下载该笔记的远程版本之前不到几分钟，那么同步会保留远程版本，而不尝试合并这两个版本。你仍然可以使用[[文件恢复]]功能恢复本地版本。

## "Vault limit exceeded" 是什么意思？

你的账户超过了[[同步限制#每个远程仓库的最大大小|50 GB的最大大小]]。请查看[[存储限制]]。

由于附件和版本历史会影响你的仓库总大小，即使你的仓库实际大小低于限制，也可能超出最大大小。

要识别并清理仓库中的大文件：

1. 打开**设置 → 同步**。
2. 探索**仓库大小超限**下的选项，了解如何减小仓库大小。

## "Vault not found" 是什么意思？

`{"res":"err","msg":"Vault not found."}`

这个错误可能在以下情况下发生：

1. 仓库已经被其他设备删除了。
2. 同步订阅已经超过30天未激活，导致远程仓库被删除。
3. 订阅被取消或退款，导致远程仓库被清除。

在每种情况下，有必要断开与远程仓库的连接并建立新连接，以确保设备上的数据得到保留。