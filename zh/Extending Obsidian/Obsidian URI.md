---
aliases:
  - Using Obsidian URI
  - Advanced topics/Using obsidian URI
  - Concepts/Obsidian URI
---
Obsidian URI is a custom URI protocol supported by Obsidian that lets you trigger various actions, such as opening a note or creating a note.

It is commonly used on macOS and mobile apps for automation and cross-app workflows.

Obsidian URIs are typically in this format:

```
obsidian://action?param1=value&param2=value
```

The `action` parameter is the action that you would like to perform.

> [!warning] Encoding
> Ensure that your values are properly URI encoded. For example, forward slash characters `/` must be encoded as `%2F` and space characters must be encoded as `%20`.
> 
 This is especially important because an improperly encoded "reserved" character may break the interpretation of the URI. [See here for details](https://en.wikipedia.org/wiki/Percent-encoding).

## Register Obsidian URI

On Windows and macOS, running the app once should be sufficient to register the Obsidian URI protocol on your computer.

On Linux, it is a much more involved process:

1. Ensure you create a `obsidian.desktop` file. [See here for details](https://developer.gnome.org/documentation/guidelines/maintainer/integrating.html#desktop-files).
2. Ensure that your desktop file specifies the `Exec` field as `Exec=executable %u`. The `%u` is used to pass the `obsidian://` URIs to the app.
3. If you're using the AppImage installer, you may have to unpack it using `Obsidian-x.y.z.AppImage --appimage-extract`. Then make sure the `Exec` directive points to the unpacked executable.

## Open notes

Opens an Obsidian vault, or open a file within that vault.

### Examples

- `obsidian://open?vault=my%20vault`
  This opens the vault `my vault`. If the vault is already open, focus on the window.

- `obsidian://open?vault=ef6ca3e3b524d22f`
  This opens the vault identified by the ID `ef6ca3e3b524d22f`.

- `obsidian://open?vault=my%20vault&file=my%20note`
  This opens the note `my note.md` in the vault `my vault`, assuming the file exists.

- `obsidian://open?path=%2Fhome%2Fuser%2Fmy%20vault%2Fpath%2Fto%2Fmy%20note`
  This will look for any vault that contains the path `/home/user/my vault/path/to/my note`. Then, the rest of the path is passed to the `file` parameter. For example, if a vault exists at `/home/user/my vault`, then this would be equivalent to `file` parameter set to `path/to/my note`.


> [!tip] Open a heading or block
> With proper URI encoding, you can navigate to a heading or block within a note. `Note%23Heading` would navigate to the heading called "Heading", whereas `Note%23%5EBlock` would navigate to the block called "Block".

### Parameters

- `vault` can be either the vault name or the vault ID[^1].
- `file` can be either a file name, or a path from the vault root to the specified file. If the file extension is `md`, the extension can be omitted.
- `path` an absolute file system path to a file.
  - Using this parameter will override both `vault` and `file`.
  - This will cause the app to search for the most specific vault which contains the specified file path.
  - Then the rest of the path replaces the `file` parameter.

## Open search

This Obsidian URI endpoint opens [[Search]] in the specified vault, and optionally perform a search query.

### Examples

- `obsidian://search?vault=my%20vault`
  This opens the vault `my vault`, and opens [[Search]].

- `obsidian://search?vault=my%20vault&query=Obsidian`
  This opens the vault `my vault`, opens [[Search]], and performs a search for `Obsidian`.

### Parameters

- `vault` can be either the vault name, or the vault ID[^1]. Same as action `open`.
- `query` (optional) The search query to perform.

## Create note

This URI endpoint creates a new note in the vault, optionally with some content.

### Examples

- `obsidian://new?vault=my%20vault&name=my%20note`
  This opens the vault `my vault`, and creates a new note called `my note`.
- `obsidian://new?vault=my%20vault&path=path%2Fto%2Fmy%20note`
  This opens the vault `my vault`, and creates a new note at `path/to/my note`.

### Parameters

- `vault` can be either the vault name, or the vault ID[^1]. Same as action `open`.
- `name` the file name to be created. If this is specified, the file location will be chosen based on your "Default location for new notes" preferences.
- `file` a vault absolute path, including the name. Will override `name` if specified.
- `path` a globally absolute path. Works similar to the `path` option in the `open` action, which will override both `vault` and `file`.
- `content` (optional) the contents of the note.
- `silent` (optional) include this parameter if you don't want to open the new note.
- `append` (optional) include this parameter to append to an existing file if one exists.
- `overwrite` (optional) overwrite an existing file if one exists, but only if `append` isn't set.
- `x-success` (optional) see [[#x-callback-url]].

## Integrate with Hook

This Obsidian URI endpoint is to be used with [Hook](https://hookproductivity.com/). 

### Example

`obsidian://hook-get-address`

### Parameters

- `vault` (optional) can be either the vault name, or the vault ID[^1]. If not provided, the current or last focused vault will be used.
- `x-success` (optional) see [[#x-callback-url]].
- `x-error` (optional) see [[#x-callback-url]].

If `x-success` is defined, this API will use it as the x-callback-url. Otherwise, it will copy a Markdown link of the current focused note to the clipboard, as an `obsidian://open` URL.

## Use x-callback-url parameters

Some endpoints will accept the x-callback-url parameters `x-success` and `x-error`. When it's provided, Obsidian will provide the following to the `x-success` callback:

- `name` the name of the file, without the file extension.
- `url` the `obsidian://` URI for this file.
- `file` (desktop only) the `file://` URL for this file.

For example, if Obsidian receives
`obsidian://.....x-success=myapp://x-callback-url`, the response would be `myapp://x-callback-url?name=...&url=obsidian%3A%2F%2Fopen...&file=file%3A%2F%2F...`

## Shorthand formats

In addition to the formats above, there are two more "shorthand" formats available to open vaults and files:

1. `obsidian://vault/my vault/my note` is equivalent to `obsidian://open?vault=my%20vault&file=my%20note`.
2. `obsidian:///absolute/path/to/my note` is equivalent to `obsidian://open?path=%2Fabsolute%2Fpath%2Fto%2Fmy%20note`.

---

[^1]: Vault ID is the random 16-character code assigned to the vault, for example `ef6ca3e3b524d22f`. This ID is unique per folder on your computer. The ID can be found by opening the vault switcher and clicking "Copy vault ID" in the context menu for the desired vault.


---

中文翻译：
Obsidian URI 是 Obsidian 支持的自定义 URI 协议，可以触发各种操作，比如打开笔记或创建笔记。

在 macOS 和移动应用中，通常用于自动化和跨应用程序工作流。

Obsidian URI 通常采用以下格式：

```
obsidian://action?param1=value&param2=value
```

`action` 参数是您想执行的操作。

> [!警告] 编码
> 确保您的数值经过正确的 URI 编码。例如，斜杠 `/` 必须编码为 `%2F`，空格必须编码为 `%20`。
> 
> 这一点尤为重要，因为未正确编码的“保留”字符可能会破坏 URI 的解释。[详细信息请参阅这里](https://en.wikipedia.org/wiki/Percent-encoding)。

## 注册 Obsidian URI

在 Windows 和 macOS 上，运行应用程序一次应该足以在计算机上注册 Obsidian URI 协议。

在 Linux 上，这是一个更加复杂的过程：

1. 确保创建了 `obsidian.desktop` 文件。[详细信息请参阅这里](https://developer.gnome.org/documentation/guidelines/maintainer/integrating.html#desktop-files)。
2. 确保您的桌面文件将 `Exec` 字段指定为 `Exec=executable %u`。`%u` 用于将 `obsidian://` URI 传递给应用程序。
3. 如果您使用的是 AppImage 安装程序，可能需要使用 `Obsidian-x.y.z.AppImage --appimage-extract` 进行解压。然后确保 `Exec` 指令指向解压后的可执行文件。

## 打开笔记

打开 Obsidian 仓库，或在该仓库内打开文件。

### 示例

- `obsidian://open?vault=my%20vault`
  这将打开名为 `my vault` 的仓库。如果该仓库已经打开，将聚焦在该窗口上。

- `obsidian://open?vault=ef6ca3e3b524d22f`
  这将打开由 ID `ef6ca3e3b524d22f` 标识的仓库。

- `obsidian://open?vault=my%20vault&file=my%20note`
  这将在名为 `my vault` 的仓库中打开名为 `my note.md` 的笔记（假设文件存在）。

- `obsidian://open?path=%2Fhome%2Fuser%2Fmy%20vault%2Fpath%2Fto%2Fmy%20note`
  这将在包含路径 `/home/user/my vault/path/to/my note` 的任何仓库中查找。然后，路径的其余部分将传递给 `file` 参数。例如，如果在 `/home/user/my vault` 下存在一个仓库，则相当于将 `file` 参数设置为 `path/to/my note`。

> [!提示] 打开标题或块
> 通过正确的 URI 编码，您可以导航到笔记中的标题或块。`Note%23Heading` 将导航到名为“Heading”的标题，而 `Note%23%5EBlock` 将导航到名为“Block”的块。

### 参数

- `vault` 可以是仓库名称或仓库 ID[^1]。
- `file` 可以是文件名，或从仓库根目录到指定文件的路径。如果文件扩展名为 `md`，则可以省略扩展名。
- `path` 到文件的绝对文件系统路径。
  - 使用此参数将覆盖 `vault` 和 `file`。
  - 这将导致应用程序搜索包含指定文件路径的最具体的仓库。
  - 然后，路径的其余部分替换 `file` 参数。

## 打开搜索

这个 Obsidian URI 终点打开了指定仓库中的[[Search|搜索]]，并可选择执行搜索查询。

### 示例

- `obsidian://search?vault=my%20vault`
  这将打开名为 `my vault` 的仓库，并打开[[Search|搜索]]。

- `obsidian://search?vault=my%20vault&query=Obsidian`
  这将打开名为 `my vault` 的仓库，打开[[Search|搜索]]，并执行对 `Obsidian` 的搜索。

### 参数

- `vault` 可以是仓库名称或仓库 ID[^1]。与 `open` 动作相同。
- `query`（可选）要执行的搜索查询。

## 创建笔记

这个 URI 终点在仓库中创建一个新笔记，可选包含一些内容。

### 示例

- `obsidian://new?vault=my%20vault&name=my%20note`
  这将打开名为 `my vault` 的仓库，并创建一个名为 `my note` 的新笔记。
- `obsidian://new?vault=my%20vault&path=path%2Fto%2Fmy%20note`
  这将打开名为 `my vault` 的仓库，并在 `path/to/my note` 处创建一个新笔记。

### 参数

- `vault` 可以是仓库名称或仓库 ID[^1]。与 `open` 动作相同。
- `name` 要创建的文件名。如果指定了此选项，文件位置将根据您的“新笔记的默认位置”首选项进行选择。
- `file` 仓库绝对路径，包括名称。如果指定了此选项，将覆盖 `name`。
- `path` 全局绝对路径。与 `open` 动作中的 `path` 选项类似，将覆盖 `vault` 和 `file`。
- `content`（可选）笔记的内容。
- `silent`（可选）如果不想打开新笔记，请包含此参数。
- `append`（可选）如果存在现有文件，则包含此参数以追加内容。
- `overwrite`（可选）覆盖现有文件，但仅当未设置 `append` 时。
- `x-success`（可选）参见[[#x-callback-url]]。

## 与 Hook 整合

这个 Obsidian URI 终点用于与 [Hook](https://hookproductivity.com/) 配合使用。

### 示例

`obsidian://hook-get-address`

### 参数

- `vault`（可选）可以是仓库名称或仓库 ID[^1]。如果未提供，则将使用当前或最近聚焦的仓库。
- `x-success`（可选）参见[[#x-callback-url]]。
- `x-error`（可选）参见[[#x-callback-url]]。

如果定义了 `x-success`，此 API 将使用它作为 x-callback-url。否则，它将将当前聚焦笔记的 Markdown 链接复制到剪贴板，作为 `obsidian://open` URL。

## 使用 x-callback-url 参数

一些终点将接受 x-callback-url 参数 `x-success` 和 `x-error`。当提供时，Obsidian 将向 `x-success` 回调提供以下信息：

- `name` 文件名，不包括文件扩展名。
- `url` 此文件的 `obsidian://` URI。
- `file`（仅桌面端）此文件的 `file://` URL。

例如，如果 Obsidian 收到
`obsidian://.....x-success=myapp://x-callback-url`，则响应将是 `myapp://x-callback-url?name=...&url=obsidian%3A%2F%2Fopen...&file=file%3A%2F%2F...`

## 简写格式

除了上述格式外，还有两种“简写”格式可用于打开仓库和文件：

1. `obsidian://vault/my vault/my note` 等同于 `obsidian://open?vault=my%20vault&file=my%20note`。
2. `obsidian:///absolute/path/to/my note` 等同于 `obsidian://open?path=%2Fabsolute%2Fpath%2Fto%2Fmy%20note`。

---

[^1]: 仓库 ID 是分配给仓库的随机 16 个字符的代码，例如 `ef6ca3e3b524d22f`。此 ID 在计算机上的每个文件夹中是唯一的。可以通过打开仓库切换器，并在所需仓库的上下文菜单中单击“复制仓库 ID”来找到该 ID。