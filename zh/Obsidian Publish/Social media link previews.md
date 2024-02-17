Many social networks display a rich preview for your website when a user shares a link to it.  Using [[属性]], you can customize how your notes appear in the preview.

> [!warning]
> The tags overridden in this section are **only** visible by web crawlers. Regular web browsers are served the unmodified page for performance.

## Description

Obsidian automatically generates a description based on the note content, but you can provide your own using `description`.

```yaml
---
description: An introduction to our solar system.
---
```

> [!note] Meta tags
> `description` overrides the auto-generated description in `<meta name="description" content="...">` and the equivalents for `og:description` and `twitter:description`.

## Image

You can use a custom image for the link preview, by adding `image` or `cover` with a path to the image.

The path can be an absolute path from the root of your vault:

```yaml
---
cover: "Attachments/Cover image.png"
---
```

Or, an external URL:

```yaml
---
image: "https://example.com/cover%20image.png"
---
```

`image` and `cover` are identical. Only use one of them.

> [!note] Meta tags
> `image` and `cover` overrides the auto-generated image in `<meta property="og:image" content="...">`.


---

中文翻译：
许多社交网络在用户分享网站链接时会显示网站的丰富预览。使用[[属性]]，你可以自定义笔记在预览中的显示方式。

> [!警告]
> 此部分中覆盖的标签**仅**对网络爬虫可见。为了提高性能，普通网络浏览器将显示未经修改的页面。

## 描述

Obsidian会根据笔记内容自动生成描述，但你也可以使用`description`自定义描述信息。

```yaml
---
description: 我们太阳系的简介。
---
```

> [!注意] 元标签
> `description`会覆盖`<meta name="description" content="...">`以及`og:description`和`twitter:description`等等的自动生成描述。

## 图片

你可以通过添加`image`或`cover`并提供图片路径来自定义链接预览中的图片。

路径可以是从仓库根目录开始的绝对路径：

```yaml
---
cover: "Attachments/Cover image.png"
---
```

或者是外部 URL：

```yaml
---
image: "https://example.com/cover%20image.png"
---
```

`image`和`cover`是相同的，只需使用其中之一即可。

> [!注意] 元标签
> `image`和`cover`会覆盖`<meta property="og:image" content="...">`中的自动生成图片。