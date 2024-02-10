You can use [symbolic links](https://en.wikipedia.org/wiki/Symbolic_link) (symlinks) and [junctions](https://learn.microsoft.com/en-us/windows/win32/fileio/hard-links-and-junctions#junctions) in your vault to store files outside the vault and [[How Obsidian stores data#Global settings|system folder]].

> [!danger] Use at your own risk
> We strongly advise against using symbolic links. By using symbolic links and junctions in your vault, you risk losing or corrupting your data, or crashing Obsidian. Make sure you perform regular back-ups of your vault and settings.

Below are some limitations or issues we are aware of that you may want to keep in mind:

- Symlink loops are disallowed, to prevent crashing Obsidian due to an infinite loop.
- Symlink targets must be fully disjoint from the vault root or any other symlink targets. Disjoint means one folder doesn't contain another, or vice versa. Obsidian ignores any symlink to a parent folder of the vault, or from one folder in the vault to another folder in the same vault. It is a safeguard to ensure you don't end up with duplicated files in your vault, which could cause links to become ambiguous.
- Symlinks may not play well with Obsidian sync, or _any other kind of sync_. If the target of a symlink is itself a folder that's synced by a different Obsidian vault, you could (potentially) end up with sync conflicts or data loss. Some sync tools, such as Git, don't follow symlinks, but rather sync the _path_ the symlink points to, which may produce undesirable results if you share your vault with other people that way.
- Obsidian's file manager can't move files across device boundaries, so if you symlink to a folder on a different drive from your vault, you won't be able to drag files between that folder and other folders using Obsidian's file explorer. (You'll need to use your OS's explorer for such moves, and Obsidian will see the move as a deletion and the creation of a new file. It will also _not_ update any links that depended on the path of that file.)
- File symlinks (as opposed to folder symlinks) _may_ work, but aren't officially supported at this time. Changes performed outside of Obsidian aren't watched for, so if you change the file directly, Obsidian won't detect the change, update search indexes, etc.
- Symlinking things under the `.obsidian/` folder in order to share them between vaults **has a high chance of corrupting your settings**, unless you _really_ know what you're doing. If you decide to go this way, at least have backups.


---

中文翻译：
你可以在你的知识库中使用[符号链接](https://zh.wikipedia.org/wiki/%E7%AC%A6%E5%8F%B7%E9%93%BE%E6%8E%A5)(symlinks)和[junctions](https://learn.microsoft.com/en-us/windows/win32/fileio/hard-links-and-junctions#junctions)来存储位于知识库之外以及[[Obsidian数据存储方式#全局设置|系统文件夹]]中的文件。

> [!警告] 请谨慎使用
> 我们强烈建议不要使用符号链接。通过在知识库中使用符号链接和junctions，您可能会面临数据丢失、损坏或Obsidian崩溃的风险。请确保定期备份您的知识库和设置。

以下是我们已经意识到的一些限制或问题，您可能需要牢记：

- 禁止符号链接循环，以防止由于无限循环导致Obsidian崩溃。
- 符号链接的目标必须与知识库根目录或任何其他符号链接目标完全不相交。完全不相交意味着一个文件夹不包含另一个文件夹，反之亦然。Obsidian会忽略任何指向知识库父文件夹的符号链接，或者从知识库中的一个文件夹指向另一个文件夹的符号链接。这是为了确保您的知识库中不会出现重复文件，从而导致链接变得模糊不清。
- 符号链接可能与Obsidian同步或_任何其他类型的同步_不兼容。如果符号链接的目标本身是另一个被不同Obsidian知识库同步的文件夹，您可能会遇到同步冲突或数据丢失。一些同步工具，比如Git，不会跟随符号链接，而是同步符号链接指向的路径，这可能会导致不良结果，尤其是如果您通过这种方式与其他人共享您的知识库。
- Obsidian的文件管理器无法跨设备边界移动文件，因此，如果您将符号链接到一个与您的知识库不同驱动器上的文件夹，您将无法使用Obsidian的文件资源管理器在该文件夹和其他文件夹之间拖动文件。您需要使用操作系统的资源管理器进行这些移动操作，而Obsidian将把这个操作视为删除和创建一个新文件。它也**不会**更新依赖该文件路径的任何链接。
- 文件符号链接（而非文件夹符号链接）_可能_会起作用，但目前并没有官方支持。在Obsidian之外执行的更改不会被监视，因此，如果您直接更改文件，Obsidian将无法检测到更改，更新搜索索引等。
- 为了在知识库之间共享，通过`.obsidian/`文件夹下的符号链接来连接这些文件，**有很高的可能性会损坏您的设置**，除非您真的非常了解这方面的操作。如果您决定这样做，请务必备份。