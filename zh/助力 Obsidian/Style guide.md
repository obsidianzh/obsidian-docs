---
aliases:
  - Obsidian Style Guide
  - 文档规范
---
The Obsidian documentation uses the [Google developer documentation style guide](https://developers.google.com/style). For any topics not covered by the Google style guide, use the [Microsoft Style Guide](https://learn.microsoft.com/en-us/style-guide/).

This page lists any deviations from the Google style guide, or terminology worth highlighting.

> [!tip] Contribute
> Most of the documentation existed before this style guide did. If you find any violations of this style guide, please [create an issue](https://github.com/obsidianmd/obsidian-docs/issues/new) or submit a pull request to [obsidianmd/obsidian-docs](https://github.com/obsidianmd/obsidian-docs).

## Terminology and grammar

### Terms

- Prefer "keyboard shortcut" over "hotkey". Use Hotkey when referring to the specific feature.
- Prefer "the Obsidian app" on mobile, and "the Obsidian application" on desktop.
- Prefer "sync" or "syncing" over "synchronize" or "synchronizing".
- Prefer "search term" over "search query".
- Prefer "heading" over "header" when referring to a text that introduces a section.
- Prefer "maximum" over "max" and "minimum" over "min".

### Product names

Obsidian product names start with "Obsidian", for example "Obsidian Publish" and "Obsidian Sync".

If a paragraph becomes overly repetitive, you can use the short form in subsequent references.

For example:

_To allow device-specific configuration, Obsidian Sync doesn't sync its own settings. You need to configure Sync for each of your devices._

### UI and interactions

- Use **bold** to indicate button text
- Prefer "select" over "tap" or "click".
- Prefer "sidebar" over "side bar".
- Prefer "perform" over "invoke" and "execute" when referring to commands or actions.

When referring to multiple UI interactions in a sequence, use the → (U+2192) symbol. For example, "**Settings → Community plugins**".

### Notes, files, and folders

- Use "note" when referring to a Markdown file in the vault.
- Use "file" when referring to other file extensions than Markdown.
- Prefer "note name" over "note title".
- Prefer "active note" over "current note".
- Prefer "folder" over "directory".
- Prefer "file type" over "file format", unless specifically referring to the data format of the file content.

When moving between notes, use "open" if the destination is hidden, and "switch" if both source and destination notes are open in separate splits.

### Reference documentation for settings

When possible, any settings should be documented within Obsidian using a descriptive text. Avoid documenting a specific setting in Obsidian Help unless:

- It requires more in-depth knowledge on how and when to use it.
- It's commonly misused or asked about.
- It _drastically_ changes the user experience.

Consider using a tip callout if you want to draw attention to a specific setting.

### Directional terms

Hyphenate directional terms when using them as adjectives. Avoid hyphenation when direction is used as a noun.

**Recommended:**

- Select **Settings** in the bottom-left corner.
- Select **Settings** in the bottom left.

**Not recommended:**

- Select **Settings** in the bottom left corner.
- Select **Settings** in the bottom-left.

Prefer "upper-left" and "upper-right" over "top-left" and "top-right".

Don't indicate a direction when referring to settings. The location of the settings control depends on the device.

**Recommended:**

- Next to **Pick remote vault**, select **Choose**.

**Not recommended:**

- To the right of **Pick remote vault**, select **Choose**.

### Instructions

Use imperatives for the names of guides, section headings, and step-by-step instructions. The imperative mood is concise and action-oriented, which is more straightforward for users following instructions.

- Prefer "Set up" over "Setting up"
- Prefer "Move a file" over "Moving a file"
- Prefer "Import your notes" over "Importing your notes"

### Sentence case

Prefer *sentence case* over *title case* for headings, buttons, and titles. When referencing UI elements always match the case of the text in the UI.

**Recommended:**

- How Obsidian stores data

**Not recommended:**

- How Obsidian Stores Data
### Examples

Prefer realistic examples over nonsense terms.

**Recommended:**

- `task:(call OR schedule)`

**Not recommended:**

- `task:(foo OR bar)`

### Key names

When referring to a character on the keyboard by name, add the character between parentheses right after the name:

**Recommended:**

- Add a hyphen (-) in front of the word.

**Not recommended:**

- Add a hyphen in front of the word.
- Add a `-` in front of the word.

### Markdown

Use newlines between Markdown blocks:

**Recommended:**

```md
# Heading 1

This is a section.

1. First item
2. Second item
3. Third item
```

**Not recommended:**

```md
# Heading 1
This is a section.
1. First item
2. Second item
3. Third item
```

### Images

Use "**width** x **height** pixels" for describing image or screen dimensions.

**Example:**

Recommended image dimensions: 1920 x 1080 pixels.

## Icons and images

Include icons and images when they make it easier to explain things that are hard to describe with words, or when you need to show important parts of the Obsidian application. You can save images in the `Attachments` folder.

- The image should make the text it accompanies easier to understand.

 **Example**: Once enabled, the [[Word count]] plugin will create a new entry on your bottom statusbar.
 
![[Style-guide-zoomed-example.png#interface|300]]

- Images should be in either `.png` or `.svg` format.
- If an image looks too big in the note, make it smaller outside of Obsidian, or adjust its dimensions as explained in [[Embed files#Embed an image in a note|embedding an image in a note]].
- In rare cases, you may want to place especially large or complex images in a [[Callouts#Foldable callouts|folded callout]]. 
- For pop-up windows or modals, the image should show the entire Obsidian application window.
 ![[Style-guide-modal-example.png#interface]]

### Icons

[Lucide](https://lucide.dev/icons/) and custom Obsidian icons can be used alongside detailed elements to provide a visual representation of a feature.

**Example:** In the ribbon on the left, select **Create new canvas** ( ![[lucide-layout-dashboard.svg#icon]] ) to create a canvas in the same folder as the active file.

**Guidelines for icons**

- Store icons in the `Attachments/icons` folder.
- Add the prefix `lucide-` before the Lucide icon name.
- Add the prefix `obsidian-icon-` before the Obsidian icon name.

**Example:** The icon for creating a new canvas should be named `lucide-layout-dashboard`.

- Use the SVG version of the icons available.
- Icons should be `18` pixels in width, `18` pixels in height, and have a stroke width of `1.5`. You can adjust these settings in the SVG data.

> [!info]- Adjusting size and stroke in an SVG
> ```html
> <svg xmlns="http://www.w3.org/2000/svg" width="WIDTH" height="HEIGHT" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="STROKE-WIDTH" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-layout-dashboard"><rect width="7" height="9" x="3" y="3" rx="1"/><rect width="7" height="5" x="14" y="3" rx="1"/><rect width="7" height="9" x="14" y="12" rx="1"/><rect width="7" height="5" x="3" y="16" rx="1"/></svg>
>```

- Utilize the `icon` anchor in embedded images, to tweak the spacing around the icon so that it aligns neatly with the text in the vicinity.
- Icons should be surrounded by parenthesis. ( ![[lucide-cog.svg#icon]] )

**Example**: `( ![[lucide-cog.svg#icon]] )`

### Image anchor tags

Image anchors tags are available to add decorative changes to the embedded images. 

> [!warning] Live preview warning
> The icon anchor tags will not display correctly in **Live preview.** Use **Reading view** to confirm the anchor tag has been applied. 

**Icon**

`![[lucide-menu.svg#icon]]`

The icon anchor tag ensures correct vertical alignment for icons used to indicate interface elements.

The first menu icon uses the anchor tag ( ![[lucide-menu.svg#icon]] ), while the second menu icon ( ![[lucide-menu.svg]] ) does not.


**Interface**

`![[Vault picker.png#interface]]`

The interface anchor tag adds a decorative box shadow around the image. In the first image, the interface anchor tag is applied.
![[Vault picker.png#interface]]
In contrast, the second image does not have the interface anchor applied.

![[Vault picker.png]]

**Outline**

`![[Backlinks.png#outline]]`

The outline anchor tag adds a subtle border around the image. In the first image, the outline anchor tag is applied. 

> [!tip] Observe the lower left of the image to see the difference.

![[Backlinks.png#outline]]

The second image lacks the outline anchor tag.

![[Backlinks.png]]

### Optimization

Images slow the loading time of the page, and take valuable [[Introduction to Obsidian Publish|Publish]] storage space. Optimizing images allows a reduction in file size, but maintains the visual integrity of the image. 

Both images and icons should be optimized.


> [!success] Tools for optimizing images
> Here are a some recommended programs for reducing the size of your images.
> - **Windows:** [FileOptimizer](https://sourceforge.net/projects/nikkhokkho/)
> - **macOS:** [ImageOptim](https://imageoptim.com/)
> - **Linux/Unix** [Trimage](https://trimage.org)
> 
> We recommend an optimization rate of 65-75%.


---


Obsidian 文档采用了[Google 开发者文档风格指南](https://developers.google.com/style)。对于 Google 风格指南未包含的部分，请参照[Microsoft 风格指南](https://learn.microsoft.com/en-us/style-guide/)。

本页面列出了与 Google 风格指南有所偏差或值得强调的术语。

> [!tip] 帮助我们改进
> 很多文档在我们指定这些指南文件前就已经存在了。如果你发现任何违反指南的地方，请[创建一个问题](https://github.com/obsidianmd/obsidian-docs/issues/new)或向[Obsidian 开发者文档](https://github.com/obsidianmd/obsidian-docs)提交请求。

## 概念的表述

注意，以下内容很多仅针对于英文语境进行规定。但仍推荐中文翻译者阅读原文以了解。

### 术语

- 在“快捷键”与“热键”之间优先选择“快捷键”。
- 移动端使用“Obsidian 应用”，桌面端使用“Obsidian 应用程序”。
- 使用“同步”而非其他表述。
- 使用“检索式”而非“搜索语句”。
- 在指代笔记中的一章节时，使用“小标题”而非“标题”。
- 使用“最大”而非“最大值”，使用“最小”而非“最小值”。

### 产品名称

Obsidian 产品名称以“Obsidian”开头，例如“Obsidian 发布服务”和“Obsidian 同步服务”。

如果需要在一个段落中多次重复，则可以使用简称形式。

例如：

_为了允许每个设备使用独有的设置，Obsidian 同步不会默认同步设置。因此你需要为每个设备决定是否开启同步设置。_

### 用户界面和交互

- 使用**粗体**表示按钮文本。
- 在指代选择操作时优先使用“选择”而非“轻触”或“点击”。
- 使用“侧边栏”而非“侧栏”。
- 指代用户执行命令时，使用“执行”。

当指代多个用户界面交互时，使用 →（U+2192）符号。例如，“**设置 → 社区插件**”。

### 笔记、文件和文件夹

- 使用“笔记”指代仓库中的 Markdown 文件。
- 使用“文件”指代仓库中 Markdown 以外的其他文件。
- 使用“笔记名称”而非“笔记标题”。
- 使用“当前笔记”而非“活动笔记”。
- 使用“文件夹”而非“目录”。
- 使用“文件类型”而非“文件格式”，除非明确指的是文件内容的数据格式。

在不同笔记之间移动时，如果目标是隐藏的，则使用“打开”，如果源笔记和目标笔记在不同分栏中，则使用“切换”。

### 设置中的参考

尽可能在 Obsidian 中使用描述性话语说明设置。除非：

- 需要更深入了解如何以及何时使用它。
- 它经常被误用或被问及。
- 它会_显著_改变用户体验。

如果要提示用户注意特定设置，则考虑使用标注语法。

### 表示方向的术语

英文语境下，将方向术语用作形容词时需要加连字符，用作名词时避免连字符。

在指代设置按钮时不要指示方向，因为设置按钮的位置取决于设备。

**推荐：**

- 在**选择远程仓库**旁边，选择**选择**。

**不推荐：**

- 在**选择远程存储库**右侧，选择**选择**。

### 指令

对于指南名称、章节小标题和操作说明，请使用祈使句。因为祈使句简洁且以行动为导向，这对于用户更为直接。

### 大小写

对于标题、按钮和小标题，使用*句式*而非*标题式*。在引用用户界面元素时，始终匹配界面文本的大小写。

### 示例

优先选择现实示例而非无意义术语。

**推荐：**

- `task:(call OR schedule)`

**不推荐：**

- `task:(foo OR bar)`

### 按键名称

在引用键盘上的字符名称时，在按键名称后使用括号补充具体字符：

**推荐：**

- 在单词前加一个连字符（-）。

**不推荐：**

- 在单词前加一个连字符。

### Markdown

在 Markdown 块间使用换行：

**推荐：**

```md
# 标题 1

这是一个章节。

1. 第一项
2. 第二项
3. 第三项
```

**不推荐：**

```md
# 标题 1
这是一个章节。
1. 第一项
2. 第二项
3. 第三项
```

### 图像

用“**宽度** x **高度** 像素”来描述图像或屏幕尺寸。

**示例：**

推荐的图像尺寸：1920 x 1080 像素。

## 图标和图像

当需要解释或展示无法用文字描述的 Obsidian 应用程序重要部分时，可以使用图标或图像。您可以将图像保存在文档的“附件”文件夹中。

- 图像应使其所对应的文本更易理解。

 **示例**：启用后，[[字数统计]] 插件将在底部状态栏中创建一个新条目。

![[Style-guide-zoomed-example.png#interface|300]]

- 图像应为`.png`或`.svg`格式。
- 如果图像在笔记中看起来太大，请在 Obsidian 外部缩小它，或根据[[Embed files|在笔记中嵌入图像]]中解释的方式调整其尺寸。
- 在极少数情况下，您可能需要将特别大或复杂的图像放在[[Callouts|可折叠提示框]]中。
- 对于弹出窗口和模态窗口，则需要显示整个 Obsidian 应用程序的图像。 ![[Style-guide-modal-example.png#interface]]

### 图标

[Lucide](https://lucide.dev/icons/) 可以与 Obsidian 自定义图标一起使用，以用于展示更多功能。

**示例:** 在功能区中，选择 **新建白板** ( ![[lucide-layout-dashboard.svg#icon]] ) 可以在当前文件夹中创建并打开一个白板文件。

**图标使用指南**

- 图标文件需要保存在 `附件/图标` 文件夹中。
- 对于 Lucide 图标，需要在文件名称前加 `lucide-` 前缀。
- 对于 Obsidian 图标，需要在文件名称前加 `obsidian-icon-` 前缀。

**示例:** The icon for creating a new canvas should be named `lucide-layout-dashboard`.

- Use the SVG version of the icons available.
- Icons should be `18` pixels in width, `18` pixels in height, and have a stroke width of `1.5`. You can adjust these settings in the SVG data.

> [!信息]- 在 SVG 中调整大小和笔画
> ```html
> <svg xmlns="http://www.w3.org/2000/svg" width="WIDTH" height="HEIGHT" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="STROKE-WIDTH" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-layout-dashboard"><rect width="7" height="9" x="3" y="3" rx="1"/><rect width="7" height="5" x="14" y="3" rx="1"/><rect width="7" height="9" x="14" y="12" rx="1"/><rect width="7" height="5" x="3" y="16" rx="1"/></svg>
>```

- 在嵌入图像中，利用 `icon` 锚点调整图标周围的间距，使其与附近文本对齐整齐。
- 图标应该用括号括起来。 ( ![[lucide-cog.svg#icon]] )

**示例**：`( ![[lucide-cog.svg#icon]] )`

### 图像锚点标签

图像锚点标签可添加对嵌入图像的装饰性更改。

> [!警告] 实时预览警告
> 图标锚点标签在**实时预览**中不会正确显示。请使用**阅读视图**确认已应用锚点标签。

**图标**

`![[lucide-menu.svg#icon]]`

图标锚点标签可确保用于指示界面元素的图标的正确垂直对齐。

第一个菜单图标使用锚标签（ ![[lucide-menu.svg#icon]] ），而第二个菜单图标（ ![[lucide-menu.svg]] ）没有。

**界面**

`![[Vault picker.png#interface]]`

界面锚点标签在图像周围添加装饰性阴影。在第一张图像中，应用了界面锚点标签。
![[Vault picker.png#interface]]
相比之下，第二张图像没有应用界面锚点。

![[Vault picker.png]]

**轮廓**

`![[Backlinks.png#outline]]`

轮廓锚点标签在图像周围添加微妙的边框。在第一张图像中，应用了轮廓锚点标签。

> [!小贴士] 观察图像的左下角以查看区别。

![[Backlinks.png#outline]]

第二张图像缺少轮廓锚点标签。

![[Backlinks.png]]

### 优化

图像会拖慢页面加载时间，并占用宝贵的[[Obsidian Publish简介|发布]]存储空间。优化图像可减小文件大小，同时保持图像视觉完整性。

图像和图标都应进行优化。

> [!成功] 图像优化工具
> 以下是减小图像大小的推荐程序。
> - **Windows:** [FileOptimizer](https://sourceforge.net/projects/nikkhokkho/)
> - **macOS:** [ImageOptim](https://imageoptim.com/)
> - **Linux/Unix** [Trimage](https://trimage.org)
> 
> 我们建议将优化率设置在 65-75%。