---
aliases:
  - Obsidian Publish/Collaborating
---
Learn how to collaborate on your [[Introduction to Obsidian Publish|Obsidian Publish]] site with other Obsidian users. By adding your friends and colleagues as collaborators, they can publish changes to your site.

Only the site owner needs an active subscription for Obsidian Publish. Collaborators only need an [Obsidian account](https://obsidian.md/account).

> [!warning]
> Before you publish changes to a shared site, make sure to [[#Syncing changes between collaborators|sync changes from other collaborators]]. Otherwise, you risk overwriting changes from other collaborators.

## Add a collaborator to a site

1. In ribbon, to the left of the application window, click **Publish changes** (paper plane icon).
2. In the **Publish changes** dialog, click **Change site options** (cog icon).
3. Next to **Site collaboration**, select **Manage**.
4. In **Invite user**, enter the email of the collaborator.
5. Select **Add**.

## Remove a collaborator from a site

1. In ribbon, to the left of the application window, click **Publish changes** (paper plane icon).
2. In the **Publish changes** dialog, click **Change site options** (cog icon).
3. Next to **Site collaboration**, select **Manage**.
4. Next to the collaborator you want to remove, select **Remove user** (cross icon).

## Sync changes between collaborators

Obsidian Publish doesn't sync published changes between local vaults automatically. Instead, collaborators need to manually sync changes from other collaborators.

To update a local note with changes from the live site:

1. In ribbon, to the left of the application window, click **Publish changes** (paper plane icon).
2. Right-click the change you want to sync, and then select **Use live version**. **This will overwrite the note in your local vault.**

> [!tip]
> We recommend that you use another tool to sync changes between vaults, such as [[Introduction to Obsidian Sync|Obsidian Sync]] or [git](https://git-scm.com/).

## Permissions

The following table lists the available site permissions for owners and collaborators:

| Action                             | Collaborator | Owner |
|------------------------------------|:------------:|:-----:|
| Publish new pages                  | ✓            | ✓     |
| Publish changes to published pages | ✓            | ✓     |
| Unpublish pages                    | ✓            | ✓     |
| Configure site options             |              | ✓     |
| Manage permissions                 |              | ✓     |


---

中文翻译：
学习如何与其他 Obsidian 用户在你的[[Obsidian Publish|Obsidian Publish]]站点上进行协作。通过将你的朋友和同事添加为协作者，他们可以发布对你站点的更改。

只有站点所有者需要有效的 Obsidian Publish 订阅。协作者只需要一个[Obsidian 账户](https://obsidian.md/account)。

> [!警告]
> 在发布对共享站点的更改之前，请确保[[#协作者之间同步更改|同步其他协作者的更改]]。否则，你可能会意外覆盖其他协作者的更改。

## 添加站点协作者

1. 在应用程序窗口左侧的工具栏中，点击**发布更改**（纸飞机图标）。
2. 在**发布更改**对话框中，点击**更改站点选项**（齿轮图标）。
3. 在**站点协作**旁边，选择**管理**。
4. 在**邀请用户**中，输入协作者的电子邮件。
5. 选择**添加**。

## 从站点中移除协作者

1. 在应用程序窗口左侧的工具栏中，点击**发布更改**（纸飞机图标）。
2. 在**发布更改**对话框中，点击**更改站点选项**（齿轮图标）。
3. 在**站点协作**旁边，选择**管理**。
4. 在要移除的协作者旁边，选择**移除用户**（叉号图标）。

## 协作者之间同步更改

Obsidian Publish 不会自动在本地 vault 之间同步已发布的更改。相反，协作者需要手动从其他协作者那里同步更改。

要使用线上站点的更改更新本地笔记：

1. 在应用程序窗口左侧的工具栏中，点击**发布更改**（纸飞机图标）。
2. 右键单击要同步的更改，然后选择**使用线上版本**。**这将覆盖本地 vault 中的笔记。**

> [!提示]
> 我们建议你使用其他工具来在 vault 之间同步更改，例如[[Obsidian Sync|Obsidian Sync]]或[git](https://git-scm.com/)。

## 权限

以下表格列出了站点所有者和协作者的可用站点权限：

| 操作                             | 协作者 | 所有者 |
|----------------------------------|:-----:|:-----:|
| 发布新页面                      | ✓    | ✓    |
| 发布已发布页面的更改           | ✓    | ✓    |
| 撤回页面                       | ✓    | ✓    |
| 配置站点选项                   |       | ✓    |
| 管理权限                       |       | ✓    |