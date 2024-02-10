Any files or settings that have been synced to your [[Local and remote vaults|remote vault]] count towards your [[Sync limitations#How large can each remote vault be|storage space]]. By default, [[Introduction to Obsidian Sync|Obsidian Sync]] ignores larger files such as audio, video, and PDFs.

**Synced files and exclusions**:
Synced files remain in your remote vault even if you exclude them later on. If possible, configure the files and settings you want to sync before you start syncing your vault.

**Sync does not sync .hidden folders:**
`.hidden` folders will not sync, with the exception of the [[configuration folder]], as these are considered folders hidden from the filesystem.

Common examples include `.vscode`, `.git`, and `.idea`.

==**Sync does not sync Sync's settings**==:
This allows users to configure Sync differently on each device according to their needs. This means, however, that you must configure custom Sync settings on each device.

> [!tip] Sync settings and application restarts
> Obsidian **only** applies vault settings during start-up. If you change a setting on one device, you **need to restart** Obsidian on your other devices for the new changes to take effect. 
> 
> For example, if you change the path of your daily notes in the [[Daily Notes]] plugin, you need to restart Obsidian on your other devices to use the new path.

## Initially adjusting your Sync settings


> [!help] This set of instructions is intended for users who wish to modify their [[Set up Obsidian Sync on another device|sync settings on an additional device]] or a new vault after [[Set up Obsidian Sync#Connect to a remote vault|establishing a connection to a remote vault]].

1. If you haven't already, close (x) or dismiss the pop-up window prompting you to **Exclude Folders** and **Start Syncing**.
2. On your primary device, navigate to **Settings** → **Sync**.
3. Under **Vault configuration sync**, activate the settings you want to synchronize.
    1. If you make changes to any settings, restart Obsidian completely.
4. After restarting Obsidian, if any settings were modified, return to **Settings** → **Sync**.
5. Choose **Resume**.
6. The synchronization process will initiate, involving uploading, downloading, or merging your files, depending on whether the remote vault contains existing files or not.


## Syncing your vault settings

> [!help] These instructions are designed for users with existing multi-device sync setups who wish to modify these settings across their devices.

**Primary device**
1. Access **Settings** → **Sync**.
2. Activate the desired settings under **Vault configuration sync**.
3. Restart Obsidian
4. Allow time for the settings to synchronize with your remote vault.

**Secondary device(s)**
1. Navigate to **Settings** → **Sync**.
2. Enable the desired settings under **Vault configuration sync**.
3. Wait for the changes to be downloaded from your remote vault.
4. Restart the application to ensure that your synchronized settings take effect.

## Select file types to sync

1. Open **Settings → Sync**.
2. Under **Selective sync**, enable the file types you want to sync.

## Exclude folder from being synced

By default, Obsidian syncs all files and folders in your vault. If you don't want Obsidian to sync a certain folder, you can exclude it.

1. Open **Settings → Sync**.
2. Under **Selective sync**, next to **Excluded folders**, click **Manage**.
3. Click the checkbox to the left of folder you want to exclude.
4. Click **Done**.

## Create a settings profile

Obsidian Sync can sync multiple [[Configuration folder|configuration folders]] to the same remote vault. You can use this to create different profiles, for example one for mobile devices and another for your laptop.

To set your settings folder:

1. Open **Settings → General**.
2. In **Override config folder**, type the name of your profile, starting with a period (`.`). For example, `.obsidian-mobile`.
3. Relaunch Obsidian to have the changes take effect. 


---

中文翻译：
与[[本地和远程仓库|远程仓库]]同步的任何文件或设置都计入您的[[同步限制#每个远程仓库的大小限制|存储空间]]。默认情况下，[[了解 Obsidian 同步|Obsidian Sync]]会忽略诸如音频、视频和 PDF 等较大的文件。

**同步的文件和排除项**：
即使您稍后将它们排除在外，同步的文件仍将保留在远程仓库中。如果可能的话，在开始同步仓库之前配置您想要同步的文件和设置。

**同步不会同步 .hidden 文件夹：**
`.hidden` 文件夹不会同步，唯一的例外是[[配置文件夹]]，因为这些文件夹被视为文件系统中隐藏的文件夹。

常见的例子包括`.vscode`、`.git`和`.idea`。

==**同步不会同步 Sync 的设置**==：
这使用户可以根据自己的需求在每台设备上单独配置 Sync。然而，这也意味着您必须在每台设备上配置自定义的 Sync 设置。

> [!提示] 同步设置和应用程序重新启动
> Obsidian **仅**在启动时应用仓库设置。如果您在一台设备上更改了某个设置，则需要重新启动其他设备上的 Obsidian，以使新更改生效。
> 
> 例如，如果您更改了[[每日笔记]]插件中的每日笔记路径，您需要在其他设备上重新启动 Obsidian 以使用新路径。

## 初始调整您的同步设置

> [!帮助] 这组说明适用于希望在[[在另一设备上设置 Obsidian Sync|另一台设备上修改同步设置]]或在[[设置 Obsidian Sync#连接到远程仓库|建立与远程仓库的连接]]后修改新仓库的用户。

1. 如果尚未这样做，请关闭（x）或忽略弹出窗口，提示您**排除文件夹**和**开始同步**。
2. 在您的主设备上，转到**设置** → **同步**。
3. 在**仓库配置同步**下，激活您想要同步的设置。
    1. 如果更改了任何设置，请完全重新启动 Obsidian。
4. 重新启动 Obsidian 后，如果有任何设置被修改，请返回**设置** → **同步**。
5. 选择**恢复**。
6. 同步过程将启动，涉及上传、下载或合并文件，具体取决于远程仓库是否包含现有文件。

## 同步您的仓库设置

> [!帮助] 这些说明适用于已经建立了多设备同步设置的用户，希望在各设备上修改这些设置。

**主设备**
1. 进入**设置** → **同步**。
2. 在**仓库配置同步**下激活所需的设置。
3. 重新启动 Obsidian。
4. 等待设置与远程仓库同步。

**次设备**
1. 转到**设置** → **同步**。
2. 在**仓库配置同步**下启用所需的设置。
3. 等待更改从远程仓库下载。
4. 重新启动应用程序以确保同步的设置生效。

## 选择要同步的文件类型

1. 打开 **设置 → 同步**。
2. 在**选择性同步**下，启用您想要同步的文件类型。

## 排除不需同步的文件夹

默认情况下，Obsidian 同步仓库中的所有文件和文件夹。如果您不希望 Obsidian 同步某个特定文件夹，您可以将其排除。

1. 打开 **设置 → 同步**。
2. 在**选择性同步**下，**排除文件夹**旁边，点击**管理**。
3. 单击要排除的文件夹左侧的复选框。
4. 点击**完成**。

## 创建设置配置文件

Obsidian Sync 可以将多个[[配置文件夹]]同步到同一个远程仓库。您可以利用这一特性创建不同的配置文件，例如一个用于移动设备，另一个用于笔记本电脑。

设置您的设置文件夹：

1. 打开 **设置 → 通用**。
2. 在**覆盖配置文件夹**中，输入您的配置文件名称，以句点（`.`）开头。例如，`.obsidian-mobile`。
3. 重新启动 Obsidian 以使更改生效。