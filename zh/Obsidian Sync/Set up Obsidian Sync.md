In this guide, you'll enable [[Introduction to Obsidian Sync|Obsidian Sync]] for your vault.

> [!hint] Remote vaults and local vaults
> In this guide, you'll create a new [[Local and remote vaults|remote vault]] and connect it to an existing local vault. You don't need to create a new local vault to use Obsidian Sync.

## Prerequisites

- An Obsidian account. If you don't have one, [sign up now](https://obsidian.md/account#mode=signup).
- An active Obsidian Sync subscription. If you don't have one, subscribe from your [account page](https://obsidian.md/account).

## Log in with your Obsidian account

1. Open **Settings**.
2. In the sidebar, select **General**.
3. Under **Account → Your Account**, select **Log in**.
4. In **Email**, enter your email.
5. In **Password**, enter your password.
6. Select **Login**.
## Enable Obsidian Sync

1. Open **Settings**.
2. In the sidebar, select **Core plugins**.
3. Enable **Sync**.

## Create a new remote vault

1. Open **Settings**.
2. In the sidebar, select **Sync**.
3. Next to **Remote vault**, select **Choose**.
4. Click **Create new vault**.
5. In **Vault name**, enter the name of the remote vault.
6. In **Region**, choose your server [[#Regional sync servers|region]] for your remote vault. 
7. In **Encryption password**, choose a password for your vault. This creates an end-to-end encrypted vault. The vault password is separate from your Obsidian account and can be different for each of your vaults. For more information, refer to [[Security and privacy]].
8. Click **Create**.

### Regional sync servers

As of [Obsidian release 1.5](https://obsidian.md/changelog/2023-11-20-desktop-v1.5.0/), users can now choose the hosting location for their remote vault. 

For users not yet on release 1.5 or a later version, the assignment of their remote vault location will be handled automatically. 

![[sync-regional-sync-servers.png#interface|300]]

After selecting a location, it's crucial to be aware that the data center **cannot** be changed afterward. If you wish to relocate your data, the process involves [[#Create a new remote vault|creating a new remote vault]] and specifying the desired hosting location during the setup.

![[Obsidian Sync/Security and privacy#^sync-geo-regions]]

## Connect to a remote vault

> [!danger] Is your current vault in an iCloud, OneDrive, Dropbox, or other syncing folder? Please [[Back up your vault|read this guide]] before proceeding.


1. Next to your newly created vault, select **Connect**.
2. In **Encryption password**, enter the password you configured for the vault if you opted into [[Obsidian Sync/Security and privacy#What does end-to-end encryption mean?|end-to-end encryption]].
3. Select **Unlock vault**.
4. It is highly recommended that you <u>do not</u> start syncing yet. Instead, proceed to [[Select files and settings to sync#Initially adjusting your Sync settings|syncing your vault settings for the first time]].
	1. If you wish to start syncing right away, select **Start Syncing**.


> [!note] Sync settings and other file types
> By default, Sync only syncs notes and images. For information how to sync other file types, refer to [[Select files and settings to sync#Select file types to sync|Select file types to sync]].
>
> If you want to sync vault configuration, such as settings for [[Core plugins]], [[Hotkeys]], or [[第三方插件]], learn how to [[Select files and settings to sync#Sync vault configuration|Sync vault configuration]].




---

中文翻译：
在本指南中，您将为您的知识库启用[[Introduction to Obsidian Sync|Obsidian Sync]]。

> [!提示] 远程知识库和本地知识库
> 在本指南中，您将创建一个新的[[Local and remote vaults|远程知识库]]并将其连接到现有的本地知识库。您无需创建新的本地知识库即可使用 Obsidian Sync。

## 先决条件

- 一个 Obsidian 账户。如果没有，请[立即注册](https://obsidian.md/account#mode=signup)。
- 一个有效的 Obsidian Sync 订阅。如果没有，请在您的[账户页面](https://obsidian.md/account)上订阅。

## 使用您的 Obsidian 账户登录

1. 打开**设置**。
2. 在侧边栏中，选择**常规**。
3. 在**账户 → 您的账户**下，选择**登录**。
4. 在**电子邮件**中，输入您的电子邮件。
5. 在**密码**中，输入您的密码。
6. 选择**登录**。

## 启用 Obsidian Sync

1. 打开**设置**。
2. 在侧边栏中，选择**核心插件**。
3. 启用**同步**。

## 创建一个新的远程知识库

1. 打开**设置**。
2. 在侧边栏中，选择**同步**。
3. 在**远程知识库**旁，选择**选择**。
4. 点击**创建新知识库**。
5. 在**知识库名称**中，输入远程知识库的名称。
6. 在**地区**中，选择您远程知识库的服务器[[#区域同步服务器|地区]]。
7. 在**加密密码**中，选择一个密码用于您的知识库。这将创建一个端到端加密的知识库。知识库密码与您的 Obsidian 账户分开，并且每个知识库的密码可以不同。有关更多信息，请参阅[[安全与隐私]]。
8. 点击**创建**。

### 区域同步服务器

从[Obsidian 1.5 版本](https://obsidian.md/changelog/2023-11-20-desktop-v1.5.0/)开始，用户现在可以选择远程知识库的托管位置。

对于尚未升级到 1.5 版本或更高版本的用户，远程知识库位置的分配将自动处理。

![同步区域同步服务器.png#界面|300]

在选择位置后，重要的是要注意数据中心**无法**在之后更改。如果您希望迁移数据，该过程涉及[[#创建一个新的远程知识库|创建一个新的远程知识库]]并在设置过程中指定所需的托管位置。

![Obsidian Sync/安全与隐私#^sync-geo-regions]

## 连接到远程知识库

> [!警告] 您当前的知识库是否位于 iCloud、OneDrive、Dropbox 或其他同步文件夹中？在继续之前，请[[备份您的知识库|阅读此指南]]。

1. 在您新创建的知识库旁，选择**连接**。
2. 在**加密密码**中，输入您为该知识库配置的密码（如果您选择了[[Obsidian Sync/安全与隐私#什么是端到端加密？|端到端加密]]）。
3. 选择**解锁知识库**。
4. 强烈建议您<u>不要</u>立即开始同步。而是继续[[选择要同步的文件和设置#首次调整您的同步设置|首次调整您的同步设置]]。
	1. 如果您希望立即开始同步，请选择**开始同步**。

> [!注意] 同步设置和其他文件类型
> 默认情况下，同步仅同步笔记和图片。有关如何同步其他文件类型的信息，请参阅[[选择要同步的文件和设置#选择要同步的文件类型|选择要同步的文件类型]]。
>
> 如果您想同步知识库配置，例如[[核心插件]]、[[快捷键]]或[[社区插件]]的设置，请了解如何[[选择要同步的文件和设置#同步知识库配置|同步知识库配置]]。