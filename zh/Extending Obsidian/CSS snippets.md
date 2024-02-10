Learn how to modify aspects of the Obsidian appearance without needing to [Build a theme](https://docs.obsidian.md/Themes/App+themes/Build+a+theme).

CSS is a language to describe how to present a HTML document. By adding CSS snippets, you can redefine parts of the Obsidian user interface, such as the size and color of headings. Obsidian includes [CSS variables](https://docs.obsidian.md/Reference/CSS+variables/CSS+variables) that you can use to easily customize parts of the interface.

Obsidian looks for CSS snippets inside the vault configuration folder.

To add a CSS snippet, follow these steps:

1. Open **Settings**.
2. Under **Appearance → CSS snippets**, select **Open snippets folder** (folder icon).
3. In the snippets folder, create a CSS file that contains your snippet.
4. In Obsidian, under **Appearance → CSS snippets**, select **Reload snippets** (refresh icon) to see the snippet in the list.

Obsidian detects changes to CSS snippets automatically and applies them when you save your snippet. You don't need to restart Obsidian for changes to take effect.

> [!tip] Example: Change text color
> For example, create a file called `snippet.css` with the following content to change the text color to red:
>
>
>
> ```css
> body {
>   --text-normal: red;
> }
> ```

## Learn more

- If you're new to CSS, refer to [Learn to style HTML using CSS](https://developer.mozilla.org/en-US/docs/Learn/CSS) by Mozilla.
- If you want more tips on styling Obsidian, refer to [About styling](https://docs.obsidian.md/Reference/CSS+variables/About+styling).


---

中文翻译：
学习如何修改 Obsidian 外观的各个方面，而无需[构建主题](https://docs.obsidian.md/Themes/App+themes/Build+a+theme)。

CSS 是一种描述如何呈现 HTML 文档的语言。通过添加 CSS 代码片段，你可以重新定义 Obsidian 用户界面的各个部分，比如标题的大小和颜色。Obsidian 包含[CSS 变量](https://docs.obsidian.md/Reference/CSS+variables/CSS+variables)，你可以使用这些变量轻松定制界面的各个部分。

Obsidian 会在仓库配置文件夹中查找 CSS 代码片段。

要添加 CSS 代码片段，请按照以下步骤操作：

1. 打开**设置**。
2. 在**外观 → CSS 代码片段**下，选择**打开片段文件夹**（文件夹图标）。
3. 在代码片段文件夹中，创建一个包含你的代码片段的 CSS 文件。
4. 在 Obsidian 中，进入**外观 → CSS 代码片段**，选择**重新加载代码片段**（刷新图标）以在列表中看到代码片段。

Obsidian 会自动检测 CSS 代码片段的更改，并在保存代码片段时应用这些更改。你无需重新启动 Obsidian 即可生效。

> [!提示] 示例：修改文本颜色
> 例如，创建一个名为 `snippet.css` 的文件，其中包含以下内容以将文本颜色更改为红色：
>
> ```css
> body {
>   --text-normal: red;
> }
> ```

## 了解更多

- 如果你对 CSS 不熟悉，可以参考 Mozilla 的[学习使用 CSS 对 HTML 进行样式设置](https://developer.mozilla.org/en-US/docs/Learn/CSS)。
- 如果你想获取更多关于样式化 Obsidian 的提示，请参考[关于样式化](https://docs.obsidian.md/Reference/CSS+variables/About+styling)。