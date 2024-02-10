---
permalink: import/onenote
---
Obsidian allows you to easily migrate your notes from Microsoft OneNote using the [[Importer|Importer plugin]].

## Import your OneNote data into Obsidian

You will need the official Obsidian [[Importer]] plugin, which you can [install here](obsidian://show-plugin?id=obsidian-importer).

1. Open **Settings**.
2. Go to **Community Plugins** and [install Importer](obsidian://show-plugin?id=obsidian-importer).
3. Enable the Importer plugin.
4. Open the **Importer** plugin using the command palette or ribbon icon.
5. Under **File format** choose **Microsoft OneNote**.
6. Click **Sign in** to open your web browser to the Microsoft sign-in page. Enter the credentials for your Microsoft account which contains your OneNote Notebooks. More information about the Microsoft sign-in process is available below.
7. Click **Accept** to grant Obsidian permission to view your OneNote Notebooks.
8. Click **Open Link** to allow your browser to redirect you to the Obsidian app.
9. In the Obsidian app, the Importer dialog will now display that you are signed in and list your OneNote Notebooks and Sections. Check the sections you wish to import.

![[OneNote-Importer-Select-Sections.png]]

10. Click **Import** and wait until import is complete.
11. You're done!

## Troubleshooting

### No sections or notebooks appear

Make sure that the notebooks you're trying to import are synced to OneDrive and visible in OneNote Web. They must be owned by you (shared notebooks written by others are unsupported).

If a specific section is missing, make sure it's not a locked section — those are invisible without removing the lock first.

### Imported notes are empty or missing content

This issue may occur on notebooks that you rarely use. To solve the issue follow these steps:

1. Open [OneNote Web](https://onenote.com/notebooks) in your browser.
2. **Right click** on the Notebooks which are missing content.
3. Select **Export Notebook** from the menu.
4. **Unzip** the file you've just downloaded into a folder.
5. Upload your OneNote notebooks [here](https://www.onenote.com/notebooks/exportimport?toImport=true).
6. Open **Obsidian Importer** and try importing again

If you've followed these tips and your issue remains unresolved, it's possible that there is a temporary problem with Microsoft servers. If that's the case, wait a few minutes and try again. If the problem persists, please open an issue on the [Obsidian Importer GitHub repository](https://github.com/obsidianmd/obsidian-importer/issues).

## Privacy

The Obsidian Importer plugin uses [OAuth](https://learn.microsoft.com/en-us/azure/active-directory/develop/v2-oauth2-auth-code-flow) to authenticate with your Microsoft account and import your OneNote notebooks. This grants a short term access token to your account which is used only from your computer and is never stored. After the import completes you may optionally revoke the token from the [Microsoft apps & services page](https://account.live.com/consent/Manage). 


---

中文翻译：
---
permalink: import/onenote
---
使用[[Importer|Importer插件]]，你可以轻松将Microsoft OneNote中的笔记迁移到Obsidian中。

## 将你的 OneNote 数据导入 Obsidian

你需要安装官方的 Obsidian [[Importer]] 插件，你可以在[这里安装](obsidian://show-plugin?id=obsidian-importer)。

1. 打开 **设置**。
2. 进入 **社区插件** 并[安装 Importer](obsidian://show-plugin?id=obsidian-importer)。
3. 启用 Importer 插件。
4. 使用命令面板或功能区图标打开 **Importer** 插件。
5. 在 **文件格式** 下选择 **Microsoft OneNote**。
6. 点击 **登录**，打开你的网络浏览器到 Microsoft 登录页面。输入包含你的 OneNote 笔记本的 Microsoft 账户凭据。有关 Microsoft 登录过程的更多信息请参考下面的说明。
7. 点击 **接受**，授权 Obsidian 查看你的 OneNote 笔记本。
8. 点击 **打开链接**，允许浏览器重定向到 Obsidian 应用程序。
9. 在 Obsidian 应用中，Importer 对话框将显示你已登录，并列出你的 OneNote 笔记本和章节。勾选你想要导入的章节。

![[OneNote-Importer-Select-Sections.png]]

10. 点击 **导入**，等待导入完成。
11. 完成！

## 故障排除

### 没有显示任何章节或笔记本

确保你尝试导入的笔记本已同步到 OneDrive 并在 OneNote Web 中可见。这些笔记本必须属于你（他人编写的共享笔记本不受支持）。

如果特定章节丢失，请确保它不是被锁定的章节 —— 这些章节在解除锁定前是不可见的。

### 导入的笔记为空或内容丢失

这个问题可能发生在你很少使用的笔记本上。按照以下步骤解决问题：

1. 在浏览器中打开[OneNote Web](https://onenote.com/notebooks)。
2. **右键单击**缺少内容的笔记本。
3. 从菜单中选择 **导出笔记本**。
4. **解压缩**刚刚下载的文件到一个文件夹中。
5. 将你的 OneNote 笔记本上传到[这里](https://www.onenote.com/notebooks/exportimport?toImport=true)。
6. 打开 **Obsidian Importer**，再次尝试导入

如果你遵循这些建议仍未解决问题，可能是 Microsoft 服务器出现了临时问题。如果是这种情况，请等待几分钟后重试。如果问题仍然存在，请在[Obsidian Importer GitHub 仓库](https://github.com/obsidianmd/obsidian-importer/issues)上提交问题。

## 隐私

Obsidian Importer 插件使用[OAuth](https://learn.microsoft.com/en-us/azure/active-directory/develop/v2-oauth2-auth-code-flow)来验证你的 Microsoft 账户并导入你的 OneNote 笔记本。这将为你的账户授予一个短期访问令牌，仅在你的计算机上使用，绝不会被存储。导入完成后，你可以选择从[Microsoft 应用和服务页面](https://account.live.com/consent/Manage)中撤销该令牌。