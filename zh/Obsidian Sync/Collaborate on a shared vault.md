---
aliases:
  - Share remote vaults
  - Collaboration
  - Teams
  - Collaborating
  - Obsidian Sync/Share remote vaults
---
With [[Introduction to Obsidian Sync|Obsidian Sync]] you can collaborate on a shared vault with your team.

All collaborators must have an active Sync subscription to access a shared vault. Joining a shared vault does not count towards your [[Sync limitations#How many remote vaults can I have?|vault limit]].

If the remote vault is [[Obsidian Sync/Security and privacy|end-to-end encrypted]], collaborators must enter the encryption password when they set up the vault.

## Manage users

### Add users

To invite a user to share a remote vault:

1. Open **Settings**.
2. In the side menu, select **Sync**.
3. Next to **Remote vault**, select **Manage**.
4. Next to the remote vault you want to share, select **Manage sharing** ( ![[lucide-users.svg#icon]] ).
5. In **Invite user**, enter the email of the user you want to invite.
6. Select **Add**.

### Remove users

1. Open **Settings**.
2. In the side menu, select **Sync**.
3. Next to **Remote vault**, select **Manage**.
4. Next to the user you want to remove access from, select **Remove user** ( ![[lucide-x.svg#icon]] ).

## Collaborate with your team

### Permissions

Fine-grained permissions are not supported yet. All collaborators receive the same permissions as the vault owner, with one exception: only the vault owner can invite collaborators.

### Live editing

Shared vaults allow teams to work together on a set of files, however Obsidian does not yet support collaborative live editing on the same file. You will not see the other user's cursor, and their edits will only appear once the changes are synced.

If multiple users are editing the same file at the same time, [[Troubleshoot Obsidian Sync#Conflict resolution|changes will be merged]] during the syncing process. Changes can be viewed and restored using [[Version history]].

![[version-history-collaboration.png]]

 
### Limitations

Be aware that Obsidian Sync has [[Sync limitations|Limitations]] that may affect your team:

- The maximum number of collaborators on a shared vault is 10 users.
- The maximum file size for attachments is 200 MB.

---

中文翻译：
---
aliases:
  - 分享远程仓库
  - 协作
  - 团队
  - 协作中
  - Obsidian Sync/分享远程仓库
---
通过[[Introduction to Obsidian Sync|Obsidian Sync]]，你可以与团队共同协作在一个共享的仓库中。

所有协作者必须拥有有效的Sync订阅才能访问共享仓库。加入共享仓库不计入你的[[Sync limitations#How many remote vaults can I have?|仓库限制]]。

如果远程仓库是[[Obsidian Sync/Security and privacy|端到端加密]]的，协作者在设置仓库时必须输入加密密码。

## 管理用户

### 添加用户

邀请用户共享远程仓库：

1. 打开**设置**。
2. 在侧边栏中，选择**同步**。
3. 在**远程仓库**旁，选择**管理**。
4. 在你想共享的远程仓库旁，选择**管理共享**（ ![[lucide-users.svg#icon]] ）。
5. 在**邀请用户**中，输入要邀请的用户的电子邮件。
6. 选择**添加**。

### 移除用户

1. 打开**设置**。
2. 在侧边栏中，选择**同步**。
3. 在**远程仓库**旁，选择**管理**。
4. 在要移除访问权限的用户旁，选择**移除用户**（ ![[lucide-x.svg#icon]] ）。

## 与团队协作

### 权限

目前不支持细粒度权限。所有协作者获得与仓库所有者相同的权限，唯一的例外是：只有仓库所有者可以邀请协作者。

### 实时编辑

共享仓库允许团队共同在一组文件上工作，但Obsidian目前尚不支持在同一文件上进行协作实时编辑。你将看不到其他用户的光标，他们的编辑只有在同步更改后才会出现。

如果多个用户同时编辑同一文件，[[Troubleshoot Obsidian Sync#Conflict resolution|更改将在同步过程中合并]]。更改可以使用[[版本历史]]查看和恢复。

![[version-history-collaboration.png]]

### 限制

请注意，Obsidian Sync有可能影响你的团队的[[Sync limitations|限制]]：

- 共享仓库上的最大协作者数量为10名用户。
- 附件的最大文件大小为200 MB。