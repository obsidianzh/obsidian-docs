---
aliases:
  - Stacked tabs
  - Linked pane
  - Pane layout
  - User interface/Use tabs in Obsidian
---
Tabs in Obsidian work much like tabs in other apps, such as web browsers.

You can open as many tabs as you want in Obsidian. You can also arrange tabs to create custom layouts that persist until the next time you open the app.

## Open a new tab

At the top of the application window, next to the last tab on the right, select **New tab** (plus icon). Or, use a keyboard shortcut:

- **Windows and Linux:** `Ctrl+t`
- **macOS:** `Cmd+t`

## Open a link

Select a link in Obsidian to open it in the active tab.

To open a link in a new tab, press `Ctrl` (or `Cmd` on macOS) and select the link.

The following are all the modifier keys you can use to open links in various ways:

|Action|MacOS|Windows/Linux|
|---|---|---|
|**Navigate**|_None_|_None_|
|**New Tab**|`⌘` (+ `Shift` in Source Mode)|`Ctrl` (+ `Shift` in Source Mode)|
|**New Tab Group**|`⌘` `⌥`| `Ctrl` `Alt`|
|**New Window**|`⌘` `⌥` `Shift`|`Ctrl` `Alt` `Shift`|

## Organize your tabs and windows

Every tab belongs to a _tab group_. You can drag and drop tabs to rearrange them within a tab group, move them to a different tab group, or create a new tab group. On desktop, you can drag tabs out of their window to open them in a separate [[Pop-out windows|pop-out window]].

Tabs in sidebars only show the icon. Hover over the icon to show a tooltip with the tab title.

### Arrange tabs

To change the order of your tabs, drag the tab along the tabs in the tab group.

As you drag a tab, _drop zones_—areas onto which you can move the tab—become highlighted. The drop zone determines where to insert the tab. Some tabs can only be in of the sidebars.

### Split a tab group

Right-click a tab and select **Split right** or **Split down** to create a new tab group with that tab.

You can also split a tab group by dragging a tab to the bottom of another tab.

### Resize a tab group

To resize a tab group, hover the cursor over an edge of the tab group. The edge becomes highlighted when it can be dragged to resize.

You can resize sidebars similarly to make more space for the tab groups in the middle.

### Move tab to a new window

**Drag and drop:**

- Select and drag the tab outside of the application window to open it in a new window.

**Command palette:**

- Open the Command Palette, and select **Move current tab to new window**.

### Move a tab to a different window

To move a tab to another existing window, drag the tab to the window you want to move it to.

### Pin a tab

To pin a tab, right-click the tab and select **Pin**. Links in a pinned tab always open in a separate tab.

To unpin a pinned tab, right-click the tab and select **Unpin**.

## Switch to a different tab

Select a tab to switch to it. Or, use a keyboard shortcut:

| Switch To                 | MacOS            | Windows/Linux        |
|---------------------------|------------------|----------------------|
| **Next tab**              | `⌃`+`⇥`         | `Ctrl`+`Tab`         |
| **Previous tab**          | `⌃`+`⇧`+`⇥`    | `Ctrl`+`Shift`+`Tab` |
| **First tab on the left** | `⌘`+`1`          | `Ctrl`+`1`           |
| **2nd to 8th tab**        | `⌘`+`2`..`8`     | `Ctrl`+`2`..`8`      |
| **Last tab on the right** | `⌘`+`9`          | `Ctrl`+`9`           |
| **Recently closed tab**   | `⌘`+`⇧`+`t`     | `Ctrl`+`Shift`+`t`   |

## Stack tab groups

You can stack tabs to slide them over other tabs in the same tab group.

To stack notes, select the down arrow at the upper right corner of the tab group, and then select **Stack notes**.

![tab-stacks](https://user-images.githubusercontent.com/693981/188205363-0f24b2a5-3706-4a8c-b38b-7a66baa68ce6.gif)

> [!note] Matushak mode
> Tab stacks are based on [Andy Matushak's sliding notes](https://notes.andymatuschak.org/).

## Linked views

_Linked views_ are tabs that reference a different tab. When the content of the referenced tab changes, the linked view changes as well.

For note tabs, you can use the following plugins as linked views:

- [[Graph view]] (local)
- [[Backlinks]]
- [[Outline]]

To open a linked view for a note tab:

1. Select **More options** (three dots icon) in the upper right corner of the note.
2. Under **Open linked view**, select the linked view you want to open.

## Save layouts

You can save and restore window layouts using the [[Workspaces]] plugin.


---

中文翻译：
---
aliases:
  - 堆叠标签
  - 关联窗格
  - 窗格布局
  - 用户界面/在 Obsidian 中使用标签
---
在 Obsidian 中，标签的工作方式类似于其他应用程序，比如网页浏览器。

你可以在 Obsidian 中打开任意数量的标签。你还可以排列标签，创建自定义布局，这些布局会一直保留，直到下次打开应用程序。

## 打开新标签

在应用程序窗口顶部，靠近最右边的最后一个标签旁边，选择**新标签**（加号图标）。或者，可以使用键盘快捷键：

- **Windows 和 Linux：** `Ctrl+t`
- **macOS：** `Cmd+t`

## 打开链接

在 Obsidian 中选择一个链接，它将在活动标签中打开。

要在新标签中打开链接，请按下`Ctrl`（或 macOS 上的`Cmd`）并选择链接。

以下是可以用来以不同方式打开链接的所有修饰键：

|操作|MacOS|Windows/Linux|
|---|---|---|
|**导航**|_无_|_无_|
|**新建标签**|`⌘`（在源模式下加`Shift`）|`Ctrl`（在源模式下加`Shift`）|
|**新建标签组**|`⌘` `⌥`| `Ctrl` `Alt`|
|**新建窗口**|`⌘` `⌥` `Shift`|`Ctrl` `Alt` `Shift`|

## 组织你的标签和窗口

每个标签都属于一个_标签组_。你可以拖放标签来重新排列它们在标签组内的位置，将它们移动到另一个标签组，或者创建一个新的标签组。在桌面端，你可以将标签拖出它们的窗口，以在单独的[[弹出窗口|弹出窗口]]中打开它们。

侧边栏中的标签只显示图标。将鼠标悬停在图标上，将显示带有标签标题的工具提示。

### 排列标签

要更改标签的顺序，请将标签拖动到标签组中的其他标签旁边。

当你拖动一个标签时，_放置区域_——你可以将标签移动到的区域——会被突出显示。放置区域决定了标签插入的位置。有些标签只能在侧边栏之一中。

### 拆分标签组

右键单击一个标签，选择**向右拆分**或**向下拆分**以创建一个包含该标签的新标签组。

你也可以通过将一个标签拖动到另一个标签的底部来拆分标签组。

### 调整标签组大小

要调整标签组的大小，请将光标悬停在标签组的边缘上。当可以拖动调整大小时，边缘会被突出显示。

类似地，你也可以调整侧边栏的大小，以为中间的标签组腾出更多空间。

### 将标签移到新窗口

**拖放：**

- 选择并拖动标签到应用程序窗口外，以在新窗口中打开它。

**命令面板：**

- 打开命令面板，选择**将当前标签移至新窗口**。

### 将标签移到另一个窗口

要将标签移到另一个现有窗口，将标签拖动到要移动到的窗口。

### 固定标签

要固定一个标签，请右键单击标签，选择**固定**。固定标签中的链接总是在单独的标签中打开。

要取消固定一个已固定的标签，请右键单击标签，选择**取消固定**。

## 切换到不同的标签

选择一个标签以切换到它。或者，可以使用键盘快捷键：

| 切换到                 | MacOS            | Windows/Linux        |
|---------------------------|------------------|----------------------|
| **下一个标签**              | `⌃`+`⇥`         | `Ctrl`+`Tab`         |
| **上一个标签**          | `⌃`+`⇧`+`⇥`    | `Ctrl`+`Shift`+`Tab` |
| **最左边的第一个标签** | `⌘`+`1`          | `Ctrl`+`1`           |
| **第2到第8个标签**        | `⌘`+`2`..`8`     | `Ctrl`+`2`..`8`      |
| **最右边的最后一个标签** | `⌘`+`9`          | `Ctrl`+`9`           |
| **最近关闭的标签**   | `⌘`+`⇧`+`t`     | `Ctrl`+`Shift`+`t`   |

## 堆叠标签组

你可以堆叠标签，将它们滑动到同一标签组中的其他标签上。

要堆叠笔记，请选择标签组右上角的向下箭头，然后选择**堆叠笔记**。

![tab-stacks](https://user-images.githubusercontent.com/693981/188205363-0f24b2a5-3706-4a8c-b38b-7a66baa68ce6.gif)

> [!注意] Matushak 模式
> 标签堆叠基于[Andy Matushak的滑动笔记](https://notes.andymatuschak.org/)。

## 关联视图

_关联视图_是引用不同标签的标签。当引用标签的内容发生变化时，关联视图也会发生变化。

对于笔记标签，你可以使用以下插件作为关联视图：

- [[图表视图]]（本地）
- [[反向链接]]
- [[大纲]]

要为笔记标签打开关联视图：

1. 在笔记右上角选择**更多选项**（三个点图标）。
2. 在**打开关联视图**下，选择你想要打开的关联视图。

## 保存布局

你可以使用[[工作区]]插件保存和恢复窗口布局。