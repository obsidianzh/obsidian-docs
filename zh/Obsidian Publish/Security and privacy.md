---
aliases:
  - Access control for Obsidian Publish
  - Security/privacy for Obsidian Publish
---
You can choose the notes you want to publish to [[Introduction to Obsidian Publish|Obsidian Publish]]. The rest of your notes stay safe in your vault.

Only the notes you choose to publish are sent to Obsidian's servers, and any notes you unpublish are removed.

## Password protection

For improved access control on your publish site, apply a site password. Visitors will be prompted for a password when attempting to access it. If you decide to remove the site password later, the entire site will become visible to the public again.

> [!warning] Individual password protection for published notes is currently not supported.

### Add a site password

1. In ribbon, to the left of the application window, click **Publish changes** (paper plane icon).
2. In the **Publish changes** dialog, click **Change site options** (cog icon).
3. Under **Other site settings**, next to **Passwords**, click **Manage**.
4. Click **New password**.
5. In **Password**, enter a password for your site.
6. (Optional) In **Nickname**, enter a nickname for the password, for example, the person you want to give site access to.
7. Click **Add this password**.

### Remove a site password

1. In ribbon, to the left of the application window, click **Publish changes** (paper plane icon).
2. In the **Publish changes** dialog, click **Change site options** (cog icon).
3. Under **Other site settings**, next to **Passwords**, click **Manage**.
5. Click the cross-icon next to the password you want to delete.

## Data collection
### Visitor data

By default, Obsidian Publish **does not** collect visitor data, store cookies, or process personal information. However you can implement analytics or log other user data by [[Customize your site|customizing your site]].

As the site owner, you are responsible for complying with GDPR and privacy regulations in your region. This includes creating your own notification banner, which can be implemented using publish.js, and adding a privacy policy page to your site.

## Access
### Managing access to Obsidian Publish on your network

To regulate access to Obsidian Publish on your network, you need to manage the following domains:

- Frontend: `publish.obsidian.md`
- Backend: `publish-main.obsidian.md`

Additionally, the backend services employ the following subdomains: `publish-xx.obsidian.md`, where `xx` is a number ranging from `1 - 100`.

> [!tip] If your firewall system supports it, we recommend whitelisting `publish-*.obsidian.md` to accommodate our continuous expansion of subdomains.


---

中文翻译：
---
aliases:
  - Obsidian Publish的访问控制
  - Obsidian Publish的安全/隐私设置
---
你可以选择要发布到[[了解Obsidian Publish|Obsidian Publish]]的笔记。其余的笔记将安全地保存在你的仓库中。

只有你选择发布的笔记才会被发送到Obsidian的服务器，取消发布的笔记将被移除。

## 密码保护

为了提高发布站点的访问控制，可以设置站点密码。访问者在尝试访问站点时将被提示输入密码。如果以后决定移除站点密码，整个站点将再次对公众可见。

> [!警告] 目前不支持为已发布的笔记设置单独的密码保护。

### 添加站点密码

1. 在应用程序窗口左侧的工具栏中，点击**发布更改**（纸飞机图标）。
2. 在**发布更改**对话框中，点击**更改站点选项**（齿轮图标）。
3. 在**其他站点设置**下，点击**密码**旁边的**管理**。
4. 点击**新密码**。
5. 在**密码**中，输入站点的密码。
6. （可选）在**昵称**中，输入密码的昵称，例如，你想要授予站点访问权限的人。
7. 点击**添加此密码**。

### 移除站点密码

1. 在应用程序窗口左侧的工具栏中，点击**发布更改**（纸飞机图标）。
2. 在**发布更改**对话框中，点击**更改站点选项**（齿轮图标）。
3. 在**其他站点设置**下，点击**密码**旁边的**管理**。
5. 点击要删除的密码旁边的叉号图标。

## 数据收集
### 访客数据

默认情况下，Obsidian Publish**不会**收集访客数据，存储Cookies或处理个人信息。但是，你可以通过[[自定义你的站点|自定义你的站点]]来实施分析或记录其他用户数据。

作为站点所有者，你有责任遵守你所在地区的GDPR和隐私法规。这包括创建自己的通知横幅，可以使用publish.js实现，并在站点上添加隐私政策页面。

## 访问
### 管理网络上的Obsidian Publish访问

为了管理网络上对Obsidian Publish的访问，你需要管理以下域名：

- 前端：`publish.obsidian.md`
- 后端：`publish-main.obsidian.md`

此外，后端服务使用以下子域：`publish-xx.obsidian.md`，其中`xx`是从`1 - 100`的数字范围。

> [!提示] 如果你的防火墙系统支持，我们建议将`publish-*.obsidian.md`列入白名单，以适应我们不断扩展的子域。