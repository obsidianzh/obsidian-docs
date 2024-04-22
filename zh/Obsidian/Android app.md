This help article is legacy and only serves as a bridge to avoid breaking links. For information on the mobile app, please see [[同步笔记]].

## Sync

For information on syncing on the Android app, please see [[同步笔记#Sync notes on Android|Sync notes on Android]].

## Storage permissions

When starting Obsidian, you may notice that it prompts for permission to access your device's documents and media.

In an ideal world, we'd prefer to only ask for access rights to the vault folders you choose. However, Android's privacy-friendly file permission API (also known as "scoped storage") has a few restrictions that makes it impossible for Obsidian to function properly.

The two biggest roadblocks are:

- Scoped storage performs many extra permission checks for every single file access, causing significant performance degradation when opening and using Obsidian.
- Scoped storage doesn't provide a way to watch for external changes, which is critical when using Obsidian with a third-party syncing tool.

Google specifically gives instructions for developers of this kind of apps a special permission. Obsidian belongs to two categories in the list of exceptions: "document management apps", and "on-device file search". [Read more about it here.](https://developer.android.com/training/data-storage/manage-all-files)


---

中文翻译：
这篇帮助文章已经过时，只是作为一个桥梁，以避免破坏链接。关于移动应用程序的信息，请参阅[[在设备间同步笔记]]。

## 同步

有关在 Android 应用中同步的信息，请参阅[[在设备间同步笔记#在Android上同步笔记|在 Android 上同步笔记]]。

## 存储权限

当启动 Obsidian 时，您可能会注意到它会提示您允许访问设备的文档和媒体。

在理想的情况下，我们更希望仅请求访问您选择的保险库文件夹的访问权限。然而，Android 的注重隐私的文件权限 API（也称为“作用域存储”）有一些限制，这使得 Obsidian 无法正常运作。

最大的两个障碍是：

- 作用域存储为每个文件访问执行许多额外的权限检查，在打开和使用 Obsidian 时会导致显著的性能下降。
- 作用域存储不提供监视外部更改的方式，这在使用 Obsidian 与第三方同步工具时至关重要。

Google 特别为这类应用程序的开发者提供了特殊的权限说明。Obsidian 属于例外列表中的两个类别：“文档管理应用程序”和“设备内文件搜索”。[在此处阅读更多信息。](https://developer.android.com/training/data-storage/manage-all-files)