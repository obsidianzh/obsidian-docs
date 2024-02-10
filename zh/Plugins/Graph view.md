The Graph view lets you visualize the relationships between the notes in your vault.

To open the Graph view, click **Open graph view** in the [[Ribbon]].

- Circles represent notes, or _nodes_.
- Lines represents [[Internal links]] between two nodes.

The more nodes that reference a given node, the bigger it gets.

To interact with notes in the graph:

- Hover over each circle to highlight that note's connections.
- Click a note in the graph to open that note.
- Right-click a note to open a context menu with the actions available for that note.

To navigate around the graph:

- Zoom in and out using the scroll wheel on your mouse, or using the `+` and `-` keys.
- Move the graph around by dragging it with your mouse cursor, or using the arrow keys.

You can hold Shift while using the keyboard to speed up the movements.

## Settings

To open the graph settings, click the cog icon in the upper-left corner of the graph view.

Click **Restore default settings** in the upper-right corner of the settings box to reset any changes you make.

### Filters

This section controls what nodes to show in the graph.

- **Search files** lets you filter notes based on a search query. To learn about how you can write more advanced search queries, refer to [[Search]].
- **Tags** toggles whether to show tags in the graph.
- **Attachments** toggles whether to show attachments in the graph.
- **Existing files only** toggles whether to show notes that exists in your vault. Since a note doesn't need to exist to link to it, this can help reduce limit your graph to notes that you actually have in your vault.
- **Orphans** toggles whether to show notes without any links.

### Groups

Create groups of notes to distinguish them from each other using color.

To create a new group:

1. Click **New group**.
2. In the search box, type a search query for the notes you want to add to the group.
3. Click the colored circle to give the group a color.

To learn about how you can write more advanced search queries, refer to [[Search]].

### Display

This section controls how to visualize nodes and links in the graph.

- **Arrows** toggles whether to show the direction of each link.
- **Text fade threshold** controls the text transparency for the name of each note.
- **Node size** controls the size of the circle representing each note.
- **Link thickness** controls the line width for each link.
- **Animate** starts a [[#Start a time-lapse animation|time-lapse animation]].

### Forces

This section controls the forces that act on each node in the graph.

- **Center force** controls how compact the graph is. A higher value creates a more circular graph.
- **Repel force** controls how much a node pushes other nodes away from it.
- **Link force** controls the pull on each link. If the link was a rubber band, the link force controls how tight or loose the band is.
- **Link distance** controls the length of the lines between each note.

## Start a time-lapse animation

Notes and attachments appear in chronological order based on their creation time.

![[obsidian-graph-view.png#interface]]

## Local Graph

To open a local Graph view, use the **Open local graph** command. While the Graph view shows all notes in your vault, a local Graph view shows you notes connected to the active note.

The local Graph view can use all of the [[#Settings]] available to the global Graph view. Additionally, you can change the depth of the local graph. Each level of depth will show notes connected to the notes revealed at the previous depth. To control local Graph depth, use the slider at the top of the local graph Settings panel.


---

中文翻译：
图形视图让你可以直观地看到仓库中笔记之间的关系。

要打开图形视图，请在[[Ribbon]]中点击**打开图形视图**。

- 圆圈代表笔记，或称为_节点_。
- 线表示两个节点之间的[[内部链接]]。

与某一节点有关联的节点越多，该节点就会变得越大。

与图中的笔记进行交互：

- 将鼠标悬停在每个圆圈上，可以突出显示该笔记的连接。
- 点击图中的一个笔记以打开该笔记。
- 右键点击一个笔记以打开包含该笔记可用操作的上下文菜单。

在图形中导航：

- 使用鼠标滚轮放大和缩小，或使用`+`和`-`键。
- 通过拖动鼠标光标或使用方向键来移动图形。

在使用键盘时按住Shift键可以加快移动速度。

## 设置

要打开图形设置，请点击图形视图左上角的齿轮图标。

点击设置框右上角的**恢复默认设置**以重置所做的任何更改。

### 过滤器

此部分控制图中显示哪些节点。

- **搜索文件**允许你根据搜索查询筛选笔记。要了解如何编写更高级的搜索查询，请参考[[搜索]]。
- **标签**切换是否在图中显示标签。
- **附件**切换是否在图中显示附件。
- **仅显示现有文件**切换是否显示存在于你的仓库中的笔记。由于笔记不需要存在才能链接到它，这可以帮助缩小图形范围至你实际拥有的笔记。
- **孤立节点**切换是否显示没有任何链接的笔记。

### 分组

使用颜色创建笔记组以区分它们。

要创建新组：

1. 点击**新组**。
2. 在搜索框中，输入要添加到组中的笔记的搜索查询。
3. 点击彩色圆圈为组选择一种颜色。

要了解如何编写更高级的搜索查询，请参考[[搜索]]。

### 显示

此部分控制如何在图中可视化节点和链接。

- **箭头**切换是否显示每个链接的方向。
- **文本淡出阈值**控制每个笔记名称文本的透明度。
- **节点大小**控制表示每个笔记的圆圈大小。
- **链接粗细**控制每个链接的线宽。
- **动画**开始一个[[#开始时间跨度动画|时间跨度动画]]。

### 力量

此部分控制作用于图中每个节点的力量。

- **中心力量**控制图的紧凑程度。数值越高，创建的图形就越圆。
- **排斥力**控制一个节点对其他节点的排斥程度。
- **链接力**控制对每个链接的拉力。如果将链接比作橡皮筋，链接力控制着橡皮筋的松紧程度。
- **链接距离**控制每个笔记之间连线的长度。

## 开始时间跨度动画

根据创建时间，笔记和附件以时间顺序出现。

![[obsidian-graph-view.png#界面]]

## 本地图形

要打开本地图形视图，请使用**打开本地图形**命令。尽管图形视图显示仓库中的所有笔记，但本地图形视图会显示连接到活动笔记的笔记。

本地图形视图可以使用全局图形视图可用的所有[[#设置]]。此外，你可以更改本地图形的深度。每个深度级别将显示连接到前一深度显示的笔记的笔记。要控制本地图形深度，请使用本地图形设置面板顶部的滑块。