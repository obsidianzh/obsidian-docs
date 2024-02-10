You can use Templates to insert pre-defined snippets of text into your active note.

## Set your template folder

1. In the bottom-left corner, click **Settings** (cog icon).
2. Under **Core plugins → Templates → Template folder location**, enter the folder containing your templates.

## Insert a template into the active note

**Important:**  To insert a template, you need to first [[#Set your template folder]].

1. In the ribbon, click **Insert template**.
2. Select the template to insert at the cursor position in the active note.

If your template folder contains only one note, Templates inserts it directly into the active note.

## Template variables

You can add dynamic information to your templates, using _template variables_. When you insert a template containing a template variable, Templates replaces it with its corresponding value.

| Variable    | Description                                     |
|-------------|-------------------------------------------------|
| `{{title}}` | Title of the active note.                       |
| `{{date}}`  | Today's date. **Default format:** `YYYY-MM-DD`. |
| `{{time}}`  | Current time. **Default format:** `HH:mm`.      |

Both `{{date}}` and `{{time}}` allow you to change the default format using a _format string_.

To set a format string, add a colon (`:`) followed by a string of [Moment.js format tokens](https://momentjs.com/docs/#/displaying/format/), for example `{{date:YYYY-MM-DD}}`.

You can use `{{date}}` and `{{time}}` interchangeably with format strings, for example `{{time:YYYY-MM-DD}}`.

You can change the default date and time formats under **Settings → Templates → Date format** and **Settings → Templates → Time format**.

> [!tip]
> You can also use the `{{date}}` and `{{time}}` template variables in the [[Daily notes]] and [[Unique note creator]] plugins.


---

中文翻译：
使用模板可以将预定义的文本片段插入到你的活动笔记中。

## 设置模板文件夹

1. 在左下角，点击**设置**（齿轮图标）。
2. 在**核心插件 → 模板 → 模板文件夹位置**下，输入包含你的模板的文件夹路径。

## 在活动笔记中插入模板

**重要提示：** 要插入模板，你需要首先[[#设置模板文件夹]]。

1. 在工具栏中，点击**插入模板**。
2. 选择要在活动笔记的光标位置插入的模板。

如果你的模板文件夹只包含一个笔记，模板会直接插入到活动笔记中。

## 模板变量

你可以使用 _模板变量_ 为模板添加动态信息。当你插入包含模板变量的模板时，模板会用其对应的值替换它。

| 变量        | 描述                                          |
|-------------|----------------------------------------------|
| `{{title}}` | 活动笔记的标题。                             |
| `{{date}}`  | 今天的日期。**默认格式：** `YYYY-MM-DD`。    |
| `{{time}}`  | 当前时间。**默认格式：** `HH:mm`。           |

`{{date}}` 和 `{{time}}` 都允许你使用 _格式字符串_ 来更改默认格式。

要设置格式字符串，添加一个冒号（`:`），后面跟着一串[Moment.js格式标记](https://momentjs.com/docs/#/displaying/format/)，例如 `{{date:YYYY-MM-DD}}`。

你可以在**设置 → 模板 → 日期格式**和**设置 → 模板 → 时间格式**下更改默认日期和时间格式。

> [!提示]
> 你也可以在[[每日笔记]]和[[唯一笔记生成器]]插件中使用`{{date}}`和`{{time}}`模板变量。