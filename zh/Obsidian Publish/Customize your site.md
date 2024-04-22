This page explains how you can customize how your [[Introduction to Obsidian Publish|Obsidian Publish]] site looks and feels.

## Static assets

You can customize your site by [[Publish and unpublish notes#Publish notes|publishing]] the following files to your site:

- `publish.css` to add custom CSS
- `publish.js` to add custom JavaScript
- `favicon-32x32.png` to set the favicon

**Notes:**

- Since Obsidian doesn't support CSS or JavaScript files, you need to use another application to create and edit them.
- Both `publish.css` and `publish.js` must be located in the root directory (`/`) of your vault.
- By default, `publish.css` and `publish.js` don't appear in the file explorer, but you can still publish them from the **Publish changes** dialog.
- To use custom JavaScript with `publish.js`, you need to [[Set up a custom domain]].

For favicons, Obsidian Publish supports the following naming conventions, where `32` is the icon dimensions in pixels:

- `favicon-32.png`
- `favicon-32x32.png`
- `favicon.ico`

We recommend that you provide one or more of the following dimensions:

- `favicon-32x32.png`
- `favicon-128x128.png`
- `favicon-152x152.png`
- `favicon-167x167.png`
- `favicon-180x180.png`
- `favicon-192x192.png`
- `favicon-196x196.png`

You have flexibility in placing favicons anywhere within the vault, as long as they are published to your site.

## Use a community theme

To use one of the community themes for your site:

1. Open your vault in the default file explorer for your OS.
2. Go to the vault settings folder (default: `.obsidian`).
3. Open the `themes` folder.
4. Copy the CSS file for the theme you want to use for your site.
5. Paste the file into the root folder of your vault.
6. Rename the CSS file to `publish.css`.
7. [[Publish and unpublish notes#Publish notes|Publish]] `publish.css`.

**Notes:**

- If the style doesn't change within a few minutes, you may need to refresh your browser cache.
- You can switch between light and dark mode in the [[Manage sites#View site options|site options]].

> [!tip] Developing themes
> Can't find the theme for you? Learn how to [Build a Publish theme](https://docs.obsidian.md/Themes/Obsidian+Publish+themes/Build+a+Publish+theme) yourself.

## Enable UI features

You can toggle several UI features for your site, such as the graph view or a table of contents.

Browse the available UI features under the **Reading experience** and **Components** sections in the [[Manage sites#View site options|site options]]

### Customize navigation

Within Obsidian Publish, you have the ability to customize the navigation order and display of files and folders within the Publish [[File explorer]]. Navigation items are listed in published order by default. Notes not published will not appear within this pane.

#### Accessing Customize navigation options

1. In ribbon, to the left of the application window, select **Publish changes** (paper plane icon).
2. In the **Publish changes** dialog, select **Change site options** (cog icon).
3. Under **Components settings**, next to **Customize navigation**, select the **manage** button. 

A new pop-up window titled **Navigation** will appear over your **Change site options** window.

#### Adjust navigation items

In the section labeled **Navigation preview**, you can adjust the display order of your published content.

1. Select the folder or note you want to adjust.
2. Drag the note or folder up or down until it is your desired place.
3. In the lower right of the **Navigation** window, select **Done**. 

Publish will send your navigation changes to your site. 


#### Hide and unhide navigation items

If there are notes or folders you have published, but you do not want visible within your Navigation, you can opt to hide those items instead. 

1. Select the folder or note you want to adjust.
2. Right click and select **Hide in navigation**. The item should now disappear from the **Navigation preview**.
3. In the lower right of the **Navigation** window, select **Done**. 

Publish will send your navigation changes to your site. 

> [!tip] You can **Show hidden** files by selecting the checkbox to the right of the **Navigation Preview** title

#### FAQ

> [!question]- Q1. Can I move files from one folder to another within the **Navigation**?
> No.
> 
> The file navigation structure for notes within folders needs to be maintained. You can adjust note order within folders (including the vault root), and folder order within other folders. 

> [!question]- Q2. Can I edit the order of multiple notes and folders before selecting **Done**?
> Yes!

> [!question]- Q3. How do I revert these changes?
> **Display order**: Select the **Restore Default** icon (counter clockwise rotate arrow) next to **Navigation item display order**. This will restore your navigation items to alphabetical order.
>
> **Hidden status**: Select the **Restore Default** icon (counter clockwise rotate arrow) next to **Hide pages or folders from navigation**. This will restore your hidden navigation items to a visible state.


---

中文翻译：
这个页面详细介绍了如何自定义[[Obsidian Publish|Obsidian Publish]]站点的外观和风格。

## 静态资源

您可以通过将以下文件发布到您的站点来自定义您的站点：

- `publish.css` 添加自定义 CSS
- `publish.js` 添加自定义 JavaScript
- `favicon-32x32.png` 设置站点的图标

**注意：**

- 由于 Obsidian 不支持 CSS 或 JavaScript 文件，您需要使用其他应用程序来创建和编辑它们。
- `publish.css` 和 `publish.js` 必须位于您的仓库的根目录（`/`）中。
- 默认情况下，`publish.css` 和 `publish.js` 不会出现在文件列表中，但您仍然可以通过**发布更改**对话框来发布它们。
- 要使用带有 `publish.js` 的自定义 JavaScript，您需要[[设置自定义域名]]。

对于图标，Obsidian Publish支持以下命名约定，其中`32`是图标的像素尺寸：

- `favicon-32.png`
- `favicon-32x32.png`
- `favicon.ico`

我们建议您提供以下一个或多个尺寸：

- `favicon-32x32.png`
- `favicon-128x128.png`
- `favicon-152x152.png`
- `favicon-167x167.png`
- `favicon-180x180.png`
- `favicon-192x192.png`
- `favicon-196x196.png`

您可以灵活地将图标放置在仓库的任何位置，只要它们被发布到您的站点上。

## 使用社区主题

要在您的站点上使用社区主题之一：

1. 在您的操作系统的默认文件浏览器中打开您的仓库。
2. 进入仓库设置文件夹（默认为`.obsidian`）。
3. 打开`themes`文件夹。
4. 复制您想要用于站点的主题的 CSS 文件。
5. 将文件粘贴到您的仓库的根文件夹中。
6. 将 CSS 文件重命名为`publish.css`。
7. [[发布和取消发布笔记#发布笔记|发布]]`publish.css`。

**注意：**

- 如果样式在几分钟内没有更改，您可能需要刷新浏览器缓存。
- 您可以在[[管理站点#查看站点选项|站点选项]]中在浅色和深色模式之间切换。

> [!提示] 开发主题
> 找不到适合您的主题吗？了解如何[构建一个发布主题](https://docs.obsidian.md/Themes/Obsidian+Publish+themes/Build+a+Publish+theme)。

## 启用 UI 功能

您可以切换站点的多个 UI 功能，例如图表视图或目录。

浏览[[管理站点#查看站点选项|站点选项]]中**阅读体验**和**组件**部分下的可用 UI 功能

### 自定义导航

在 Obsidian Publish 中，您可以自定义文件和文件夹在发布[[文件资源管理器]]中的导航顺序和显示方式。默认情况下，导航项目按发布顺序列出。未发布的笔记不会出现在此面板中。

#### 访问自定义导航选项

1. 在应用程序窗口的左侧，选择**发布更改**（纸飞机图标）。
2. 在**发布更改**对话框中，选择**更改站点选项**（齿轮图标）。
3. 在**组件设置**下，选择**自定义导航**旁边的**管理**按钮。 

将出现一个名为**导航**的新弹出窗口，覆盖在您的**更改站点选项**窗口上。

#### 调整导航项目

在标有**导航预览**的部分，您可以调整您发布内容的显示顺序。

1. 选择要调整的文件夹或笔记。
2. 将笔记或文件拖动到所需位置。
3. 在**导航**窗口右下角，选择**完成**。

发布将发送您的导航更改到您的站点。

#### 隐藏和取消隐藏导航项目

如果有一些已发布的笔记或文件夹，但您不希望在导航中看到它们，您可以选择隐藏这些项目。

1. 选择要调整的文件夹或笔记。
2. 右键单击并选择**在导航中隐藏**。该项目现在应该从**导航预览**中消失。
3. 在**导航**窗口右下角，选择**完成**。

发布将发送您的导航更改到您的站点。

> [!提示] 您可以通过选择**导航预览**标题右侧的复选框来**显示隐藏**文件

#### 常见问题解答

> [!问题]- 问：我可以在**导航**中将文件从一个文件夹移动到另一个文件夹吗？
> 答：不可以。
> 
> 需要保持文件夹内笔记的导航结构。您可以调整文件夹内笔记的顺序（包括仓库根目录内的笔记）以及文件夹在其他文件夹内的顺序。

> [!问题]- 问：我可以在选择**完成**之前编辑多个笔记和文件的顺序吗？
> 答：可以！

> [!问题]- 问：如何恢复这些更改？
> 答：**显示顺序**：选择**导航项目显示顺序**旁边的**恢复默认**图标（逆时针旋转箭头）。这将将您的导航项目恢复为按字母顺序排列。
>
> **隐藏状态**：选择**导航中隐藏页面或文件**旁边的**恢复默认**图标（逆时针旋转箭头）。这将将您隐藏的导航项目恢复为可见状态。