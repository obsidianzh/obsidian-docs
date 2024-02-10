Canvas is a tool for visual note-taking. Lay out notes and other resources on an infinite canvas and connect them with lines.

Visual note-taking allows you to use visual aspects, such as size and position, to make sense of your notes. Connect notes with lines and group related notes together to better understand the relationship between them.

## Create a new canvas

To start using Canvas, you first need to create a file to hold your canvas. You can create a new canvas using the following methods.

**Ribbon:**

- In the ribbon on the left, select **Create new canvas** ( ![[lucide-layout-dashboard.svg#icon]] ) to create a canvas in the same folder as the active file.

**Command palette:**

1. Open the [[Command palette]].
2. Select **Canvas: Create new canvas** to create a canvas in the same folder as the active file.

**File explorer:**

- In the [[File explorer]], right-click the folder you want to create the canvas in.
- Select **New canvas**.

> [!note]  The .canvas file extension
> Obsidian stores the configuration for each canvas in a custom JSON format in a file with the `.canvas` extension.

## Adding cards

You can drag files into your canvas from Obsidian or from other applications. For example, Markdown files, images, audio, PDFs, or even unrecognized file types.

### Add text cards

You can add text-only cards that don't reference a file. You can use Markdown, links, and code blocks just like in a note.

To add a new text card to your canvas:

- Select or drag the blank file icon at the bottom of the canvas.

You can also add text cards by double-clicking on the canvas.

To convert a text card to a file:

1. Right-click the text card and then select **Convert to file...**.
2. Enter the note name and then select **Save**.

> [!note]
> Text-only cards don't appear in [[Backlinks]]. To make them appear, you need to convert them to a file.

### Add cards from notes

To add a note from your vault to your canvas:

1. Select or drag the document icon at the bottom of the canvas.
2. Select the note you want to add.

You can also add notes from the canvas context menu:

1. Right-click the canvas and then select **Add note from vault**.
2. Select the note you want to add.

Or, you can add them to the canvas by dragging the file from the [[File explorer]].

### Add cards from media

To add media from your vault to your canvas:

1. Select or drag the image file icon at the bottom of the canvas.
2. Select the media file you want to add.

You can also add media from the canvas context menu:

1. Right-click the canvas and then select **Add media from vault**.
2. Select the media file you want to add.

Or, you can add them to the canvas by dragging the file from the [[File explorer]].

### Add cards from web pages

To embed a web page in your canvas:

1. Right-click the canvas and then select **Add web page**.
2. Enter the URL to the web page and then select **Save**.

You can also select a URL in your browser and then drag it into the canvas to embed it in a card.

To open the web page in your browser, press `Ctrl` (or `Cmd` on macOS) and select the card label. Or, right-click the card and select **Open in browser**.

### Add cards from folders

Drag a folder from the file explorer to add all files in that folder to the canvas.

### Edit a card

Double-click on a text or note card to start editing it. Click outside the card to stop editing it. You can also press `Escape` to stop editing a card.

You can also edit a card by right-clicking it and selecting **Edit**.

### Delete a card

Remove selected cards by right-clicking any of them, and then selecting **Delete**. Or, press `Backspace` (or `Delete` or macOS).

You can also select **Remove** (trash icon) in the selection controls above your selection.

### Swap cards

You can swap a note or media card for another card of the same type.

To swap a note card:

1. Right-click the card you want to replace.
2. Select **Swap file**.
3. Select the note you want to replace with.

## Selecting cards

Select cards in the canvas by clicking on them. You can select multiple cards by dragging a selection around them.

You can also add and remove cards from an existing selection by pressing `Shift` and selecting them.

Press `Ctrl+a` (or `Cmd+a` on macOS) to select all cards in the canvas.

To scroll the content of a card, you first need to select it.

### Arrange cards

Drag a selected card to move it.

Press `Alt` (or `Option` on macOS) and drag to duplicate the selection.

You can press `Shift` while dragging to only move in one direction.

Press `Space` while moving a selection to disable snapping.

Selecting a card moves it to the front.

### Resize a card

Drag any of a card's edges to resize it.

You can press `Space` while resizing to disable snapping.

To maintain the aspect ratio while resizing, press `Shift` while resizing.

## Connecting cards

Draw lines between cards to create relationships between them. Use colors and labels to describe how they relate to each other.

### Connect two cards

To connect two cards with a directed line:

1. Hover the cursor over one of the edges of a card until you see a filled circle.
2. Drag the circle to the edge of a different card to connect them.

> [!tip]
> If you drag the line without connecting it to another card, you can then add the card you want to connect it to.

### Disconnect two cards

To remove the connection between two cards:

1. Hover the cursor over a connection line until two small circles appear on the line.
2. Drag one of the circles from the card without connecting it to another.

You can also disconnect two cards by right-clicking the line between them, and then selecting **Remove**. Or, by selecting the line and then pressing `Backspace` (or `Delete` on macOS).

### Connect a card to a different card

To move one of the ends of a connection line:

1. Hover the cursor over a connection line until two small circles appear on the line.
2. Drag the circle over the end you want to reconnect, to another card.

### Navigate a connection

If two connected cards are far apart, you can navigate to the source or the target of the connection by right-clicking the line and then select **Go to target** or **Go to source**.

### Add a label to a connection

You can add a label to a line to describe the relationship between two cards.

To label a connection:

1. Double-click the line.
2. Enter the label and then press `Escape` or click anywhere on the canvas.

You can also label a connection by selecting it and then selecting **Edit label** from the selection controls.

To edit a connection label, double-click on the line, or right-click the line and then select **Edit label**.

### Change the color of a card or connection

1. Select the cards or connections you want to color.
2. In the selection controls, select **Set color** (palette icon).
3. Select a color.

## Grouping cards

### Group selected cards

To create an empty group:

- Right-click the canvas and then select **Create group**.

To group related cards:

1. Select the cards.
2. Right-click any of the selected cards and then select **Create group**.

**Rename group:** Double-click the name of the group to edit it, and then press `Enter` to save.

## Navigating the canvas

As you start adding more cards to your canvas, you want to understand how you can navigate the canvas to look at a part of it. Learn how to pan and zoom to move across the canvas with ease.

### Pan the canvas

To move the canvas vertically and horizontally, also known as _panning_, you can use any of the following approaches:

- Press `Space` and drag the canvas.
- Drag the canvas using the middle-mouse button.
- Scroll the mouse to pan vertically, and press `Shift` while scrolling to pan horizontally.

### Zoom the canvas

To zoom the canvas, press `Space`  or `Ctrl` (or `Cmd` on macOS) and scroll using the mouse wheel. Or, select **Zoom in** (plus sign) and **Zoom out** (minus sign) from the zoom controls in the upper-right corner.

#### Zoom to fit

To zoom the canvas so that every item is visible, select **Zoom to fit** (dashed square icon). Or, use the keyboard shortcut, `Shift+1`.

#### Zoom to selection

To zoom the canvas so that all selected items are visible, right-click a selected card and then select **Zoom to selection**. Or, use a keyboard shortcut by pressing `Shift+2`.

#### Reset zoom

To change the zoom level back to the default, select **Reset zoom** in the zoom controls in the upper-right corner.

## Advanced tips

We have made some quick videos to demonstrate some advanced use cases of Canvas.

You can [check out all 72 tips here](https://obsidian.md/canvas#protips). Please note that the tip videos are only visible on desktop.


---

中文翻译：
Canvas 是一个用于视觉笔记的工具。在无限画布上布置笔记和其他资源，并用线条连接它们。

视觉笔记让你可以利用视觉方面的元素，比如大小和位置，来理解你的笔记。通过线条连接笔记，将相关笔记分组在一起，以更好地理解它们之间的关系。

## 创建新画布

要开始使用 Canvas，首先需要创建一个文件来保存你的画布。你可以使用以下方法创建一个新的画布。

**Ribbon（功能区）:**

- 在左侧的功能区中，选择**创建新画布**（ ![[lucide-layout-dashboard.svg#icon]] ）以在活动文件所在的文件夹中创建一个画布。

**命令面板:**

1. 打开[[命令面板]]。
2. 选择**Canvas: 创建新画布**以在活动文件所在的文件夹中创建一个画布。

**文件资源管理器:**

- 在[[文件资源管理器]]中，右键单击要创建画布的文件夹。
- 选择**新画布**。

> [!注意]  .canvas 文件扩展名
> Obsidian会以`.canvas`扩展名的文件中以自定义 JSON 格式存储每个画布的配置。

## 添加卡片

你可以从 Obsidian 或其他应用程序中将文件拖入你的画布。例如，Markdown 文件、图片、音频、PDF 或甚至无法识别的文件类型。

### 添加文本卡片

你可以添加不引用文件的纯文本卡片。你可以像在笔记中一样使用 Markdown、链接和代码块。

要向你的画布添加新的文本卡片：

- 选择或拖动画布底部的空白文件图标。

你也可以通过双击画布来添加文本卡片。

要将文本卡片转换为文件：

1. 右键单击文本卡片，然后选择**转换为文件...**。
2. 输入笔记名称，然后选择**保存**。

> [!注意]
> 纯文本卡片不会出现在[[反向链接]]中。要使其出现，你需要将其转换为文件。

### 从笔记中添加卡片

要将仓库中的笔记添加到你的画布中：

1. 选择或拖动画布底部的文档图标。
2. 选择要添加的笔记。

你也可以通过画布上下文菜单来添加笔记：

1. 右键单击画布，然后选择**从仓库添加笔记**。
2. 选择要添加的笔记。

或者，你可以通过从[[文件资源管理器]]中拖动文件将其添加到画布中。

### 从媒体添加卡片

要将仓库中的媒体添加到你的画布中：

1. 选择或拖动画布底部的图像文件图标。
2. 选择要添加的媒体文件。

你也可以通过画布上下文菜单来添加媒体：

1. 右键单击画布，然后选择**从仓库添加媒体**。
2. 选择要添加的媒体文件。

或者，你可以通过从[[文件资源管理器]]中拖动文件将其添加到画布中。

### 从网页添加卡片

要在你的画布中嵌入网页：

1. 右键单击画布，然后选择**添加网页**。
2. 输入网页的 URL，然后选择**保存**。

你也可以在浏览器中选择一个 URL，然后将其拖到画布中以在卡片中嵌入。

要在浏览器中打开网页，请按下 `Ctrl`（或 macOS 上的 `Cmd`）并选择卡片标签。或者，右键单击卡片，然后选择**在浏览器中打开**。

### 从文件夹添加卡片

从文件资源管理器中拖动一个文件夹以将该文件夹中的所有文件添加到画布中。

### 编辑卡片

双击文本或笔记卡片即可开始编辑。单击卡片外部停止编辑。你也可以按 `Escape` 停止编辑卡片。

你还可以通过右键单击卡片并选择**编辑**来编辑卡片。

### 删除卡片

右键单击任一已选择的卡片，然后选择**删除**以删除已选择的卡片。或者，按下 `Backspace`（或 macOS 上的 `Delete`）。

你还可以在所选卡片上方的选择控件中选择**移除**（垃圾桶图标）以删除已选择的卡片。

### 交换卡片

你可以将一个笔记或媒体卡片替换为另一个相同类型的卡片。

要交换笔记卡片：

1. 右键单击要替换的卡片。
2. 选择**交换文件**。
3. 选择要替换为的笔记。

## 选择卡片

通过点击卡片来选择画布中的卡片。你可以通过在卡片周围拖动选择多个卡片。

你也可以按下 `Shift` 并选择卡片来添加和移除已选卡片。

按下 `Ctrl+a`（或 macOS 上的 `Cmd+a`）选择画布中的所有卡片。

要滚动卡片的内容，首先需要选择它。

### 排列卡片

拖动选择的卡片以移动它们。

按下 `Alt`（或 macOS 上的 `Option`）并拖动以复制选择的内容。

在拖动时按下 `Shift` 以仅在一个方向上移动。

在移动选择时按下 `Space` 以禁用吸附。

选择卡片会将其移至前面。

### 调整卡片大小

拖动任何卡片的边缘以调整大小。

在调整大小时按下 `Space` 以禁用吸附。

在调整大小时按下 `Shift` 以保持纵横比。

## 连接卡片

在卡片之间画线以创建它们之间的关系。使用颜色和标签描述它们之间的关系。

### 连接两个卡片

要使用有向线连接两个卡片：

1. 将鼠标悬停在卡片边缘上，直到看到一个填充的圆圈。
2. 将圆圈拖到另一个卡片的边缘以连接它们。

> [!提示]
> 如果你拖动线而不将其连接到另一张卡片，然后你可以添加要连接的卡片。

### 断开两个卡片的连接

要删除两个卡片之间的连接：

1. 将鼠标悬停在连接线上，直到线上出现两个小圆圈。
2. 从不连接到其他卡片的卡片中拖动其中一个圆圈。

你也可以通过右键单击它们之间的线并选择**移除**来断开两个卡片的连接。或者，选择该线，然后按 `Backspace`（或 macOS 上的 `Delete`）。

### 将卡片连接到不同的卡片

要移动连接线的一端：

1. 将鼠标悬停在连接线上，直到线上出现两个小圆圈。
2. 将圆圈拖动到你想要重新连接的另一张卡片上。

### 导航到连接

如果连接的两个卡片相距很远，你可以右键单击线，然后选择**转到目标**或**转到源**以导航到连接的源或目标。

### 为连接添加标签

你可以为线条添加标签以描述两个卡片之间的关系。

要为连接添加标签：

1. 双击线条。
2. 输入标签，然后按 `Escape` 或单击画布的任何位置。

你也可以通过选择它然后在选择控件中选择**编辑标签**来为连接添加标签。

要编辑连接标签，双击线条，或右键单击线条然后选择**编辑标签**。

### 更改卡片或连接的颜色

1. 选择要着色的卡片或连接。
2. 在选择控件中选择**设置颜色**（调色板图标）。
3. 选择一种颜色。

## 分组卡片

### 分组选择的卡片

要创建一个空分组：

- 右键单击画布，然后选择**创建分组**。

要将相关卡片分组：

1. 选择卡片。
2. 右键单击任何已选择的卡片，然后选择**创建分组**。

**重命名分组：**双击分组名称进行编辑，然后按 `Enter` 保存。

## 浏览画布

当你开始向画布添加更多卡片时，你需要了解如何导航画布以查看其中的一部分。学习如何平移和缩放以轻松移动画布。

### 平移画布

要垂直和水平移动画布，也称为_平移_，你可以使用以下任一方法：

- 按下 `Space` 并拖动画布。
- 使用鼠标中键拖动画布。
- 滚动鼠标以垂直平移，并在滚动时按下 `Shift` 以水平平移。

### 缩放画布

要缩放画布，按下 `Space` 或 `Ctrl`（或 macOS 上的 `Cmd`）并使用鼠标滚轮滚动。或者，从右上角的缩放控件中选择**放大**（加号）和**缩小**（减号）。

#### 缩放至适合

要缩放画布以使每个项目都可见，请选择**缩放至适合**（虚线方框图标）。或者，使用快捷键 `Shift+1`。

#### 缩放至选择

要缩放画布以使所有选定项目都可见，请右键单击选定的卡片，然后选择**缩放至选择**。或者，通过按 `Shift+2` 使用快捷键。

#### 重置缩放

要将缩放级别恢复为默认值，请在右上角的缩放控件中选择**重置缩放**。

## 高级提示

我们制作了一些快速视频来演示 Canvas 的一些高级用例。

你可以[在这里查看所有 72 个提示](https://obsidian.md/canvas#protips)。请注意，这些提示视频仅在桌面上可见。