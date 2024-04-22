---
aliases:
  - How to/Embed files
  - Linking notes and files/Embedding files
---

Learn how you can embed other notes and media into your notes. By embedding files in your notes, you can reuse content across your vault.

To embed a file in your vault, add an exclamation mark (`!`) in front of an [[Internal links|Internal link]]. You can embed files in any of the [[支持的文件格式]].

## Embed a note in another note

To embed a note:

```md
![[Internal links]]
```

You can also embed links to [[Internal links#Link to a heading in a note|headings]] and [[Internal links#Link to a block in a note|blocks]].

```md
![[Internal links#^b15695]]
```

The text below is an example of an embedded block:

![[Internal links#^b15695]]

## Embed an image in a note

To embed an image:

```md
![[Engelbart.jpg]]
```

![[Engelbart.jpg#outline]]

You can change the image dimensions, by adding `|640x480` to the link destination, where 640 is the width and 480 is the height.

```md
![[Engelbart.jpg|100x145]]
```

If you only specify the width, the image scales according to its original aspect ratio. For example, `![[Engelbart.jpg|100]]`.

![[Engelbart.jpg#outline|100]]

## Embed an audio file in a note

To embed an audio file:

```md
![[Excerpt from Mother of All Demos (1968).ogg]]
```

![[Excerpt from Mother of All Demos (1968).ogg]]

## Embed a PDF in a note

To embed a PDF:

```md
![[Document.pdf]]
```

You can also open a specific page in the PDF, by adding `#page=N` to the link destination, where `N` is the number of the page:

```md
![[Document.pdf#page=3]]
```

You can also specify the height in pixels for the embedded PDF viewer, by adding `#height=[number]` to the link. For example:

```md
![[Document.pdf#height=400]]
```

## Embed a list in a note

To embed a list from a different note, first add a [[Internal links#Link to a block in a note|block identifier]] to your list:

```md

- list item 1
- list item 2

^my-list-id
```

Then link to the list using the block identifier:

```md
![[My note#^my-list-id]]
```

## Embed search results 

![[Search#Embed search results in a note]]


---

中文翻译：
---
aliases:
  - 如何/嵌入文件
  - 笔记和文件链接/嵌入文件
---

学习如何在笔记中嵌入其他笔记和媒体文件。通过在笔记中嵌入文件，你可以在整个仓库中重复使用内容。

要在你的仓库中嵌入文件，在[[内部链接|内部链接]]前加上感叹号（`!`）。你可以嵌入任何[[接受的文件格式]]。

## 在另一个笔记中嵌入一个笔记

要嵌入一个笔记：

```md
![[内部链接]]
```

你也可以嵌入到[[内部链接#链接到笔记中的标题|标题]]和[[内部链接#链接到笔记中的块|块]]。

```md
![[内部链接#^b15695]]
```

下面的文本是一个嵌入块的示例：

![[内部链接#^b15695]]

## 在笔记中嵌入图片

要嵌入图片：

```md
![[Engelbart.jpg]]
```

![[Engelbart.jpg#outline]]

你可以通过在链接目标中添加`|640x480`来更改图片尺寸，其中640是宽度，480是高度。

```md
![[Engelbart.jpg|100x145]]
```

如果只指定宽度，图片将按照原始宽高比例缩放。例如，`![[Engelbart.jpg|100]]`。

![[Engelbart.jpg#outline|100]]

## 在笔记中嵌入音频文件

要嵌入音频文件：

```md
![[Excerpt from Mother of All Demos (1968).ogg]]
```

![[Excerpt from Mother of All Demos (1968).ogg]]

## 在笔记中嵌入 PDF 文件

要嵌入 PDF 文件：

```md
![[Document.pdf]]
```

你也可以打开 PDF 中的特定页，通过在链接目标后添加`#page=N`，其中`N`为页数：

```md
![[Document.pdf#page=3]]
```

你还可以为嵌入的 PDF 查看器指定高度（以像素为单位），通过在链接中添加`#height=[数字]`。例如：

```md
![[Document.pdf#height=400]]
```

## 在笔记中嵌入列表

要在笔记中嵌入来自不同笔记的列表，首先在你的列表中添加一个[[内部链接#链接到笔记中的块|块标识符]]：

```md

- 列表项 1
- 列表项 2

^my-list-id
```

然后使用块标识符链接到列表：

```md
![[My note#^my-list-id]]
```

## 嵌入搜索结果

![[Search#在笔记中嵌入搜索结果]]