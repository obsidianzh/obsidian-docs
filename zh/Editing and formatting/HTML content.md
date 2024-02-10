---
aliases:
  - Advanced topics/HTML sanitization
  - Editing and formatting/Using HTML
---
Obsidian supports HTML to allow you to display your notes the way you want, or even [[Embed web pages|embed web pages]]. Allowing HTML inside your notes comes with risks. To prevent malicious code from doing harm, Obsidian _sanitizes_ any HTML in your notes. 

> [!example] 
> The `<script>` element normally lets you run JavaScript whenever it loads. If Obsidian didn't sanitize HTML, an attacker could convince you to paste a text containing JavaScript that extracts sensitive information from your computer and sends it back to them.

That said, since Markdown syntax does not support all forms of styling, using sanitized HTML can be yet another way of enhancing the quality of your notes. We've included some of the more common usages of HTML. 

> [!info] More details on using `<iframe>` can be found in [[Embed web pages]].

### Comments

[[Basic formatting syntax#Comments|Markdown comments]] are the preferred way of adding hidden comments within your notes. However some methods of converting Markdown notes, such as [Pandoc](https://pandoc.org), have limited support of Markdown comments. In those instances, you can use a `<!-- HTML Comment -->` instead!

### Underline

If you need to quickly underline an item in your notes, you can use `<u>Example</u>` to create <u>your underlined text</u>.

### Span/Div

Span and div tags can be used to apply custom classes from a [[CSS snippets|CSS snippet]], or custom defined styling, onto a selected area of text. For example, using `<span style="font-family: cursive">your text</span>` can allow you to quickly <span style="font-family: cursive">change your font</span>.

## Strikethrough

Need to strike <s>some text</s>? Use `<s>this</s>` to strike it out.




---

中文翻译：
Obsidian支持HTML，让你可以按照自己的喜好显示笔记内容，甚至[[嵌入网页|嵌入网页]]。允许在笔记中使用HTML也伴随着一定的风险。为了防止恶意代码造成伤害，Obsidian会对笔记中的HTML进行_清理_。

> [!示例]
> `<script>`元素通常允许在加载时运行JavaScript。如果Obsidian不对HTML进行清理，攻击者可能会让你粘贴包含JavaScript的文本，从而提取你电脑中的敏感信息并发送给他们。

话虽如此，由于Markdown语法并不支持所有样式形式，使用经过清理的HTML也是提升笔记质量的另一种方式。我们列出了一些HTML的常见用法。

> [!信息] 关于使用`<iframe>`的更多细节可在[[嵌入网页]]中找到。

### 注释

[[基本格式语法#注释|Markdown注释]]是在笔记中添加隐藏注释的首选方式。然而，一些Markdown笔记转换方法，如[Pandoc](https://pandoc.org)，对Markdown注释的支持有限。在这种情况下，你可以使用`<!-- HTML注释 -->`代替！

### 下划线

如果需要快速给笔记中的某个项目加下划线，你可以使用`<u>示例</u>`来创建<u>下划线文本</u>。

### Span/Div

Span和div标签可用于在所选文本区域应用来自[[CSS代码片段|CSS代码片段]]或自定义定义样式的自定义类。例如，使用`<span style="font-family: cursive">你的文本</span>`可以让你快速地<span style="font-family: cursive">改变字体</span>。

## 删除线

需要给一些文本加上<s>删除线</s>吗？使用`<s>这个</s>`来划掉它。