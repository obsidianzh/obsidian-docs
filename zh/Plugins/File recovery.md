File recovery helps you recover your work in the case of unintentional data loss, by regularly saving snapshots of your notes.

To avoid taking up too much space, Obsidian keeps snapshots for a certain number of days before deleting them.

> [!note] 
> By default, snapshots are saved a minimum of 5 minutes from each other, and kept for 7 days. You can configure both intervals under **Settings → File recovery**.

Snapshots are kept in the [[Obsidian 的储存机制#System directory|system directory]], outside of the vault, to account for vault-related data loss. This means that snapshots are stored with the absolute path to the note. If you've moved your vault recently, you may need to move it back to the location where it was when the snapshot was taken.

## Recover a snapshot

1. Open **Settings**.
2. In the sidebar, click **File recovery** under **Plugin options**.
3. Next to **Snapshots**, click **View**.
4. In the upper-**left** text box, start typing the name of the file you want to recover, and you'll see a suggestion list. 
5. Select the file, press Enter, and you'll see a list of snapshots available.
6. Select the snapshot you want to recover.
7. Click **Copy to clipboard** to copy the snapshot.
8. Paste the snapshot in the original note, or in a new note if you want to compare them.

## Clear snapshot history

**Caution:** Clearing the snapshot history irreversibly deletes all snapshots in your vault.

1. Open **Settings**.
2. In the sidebar, click **File recovery** under **Plugin options**.
3. Next to **Clear history**, click **Clear**.
4. Confirm that you want to delete all snapshots, by clicking **Clear**.


---

中文翻译：
文件恢复功能可以帮助您在意外数据丢失的情况下恢复工作，定期保存笔记的快照。

为了避免占用过多空间，Obsidian在删除它们之前会保留一定天数的快照。

> [!提示]
> 默认情况下，快照之间至少相隔5分钟，并保留7天。您可以在**设置 → 文件恢复**下配置这两个时间间隔。

快照保存在[[Obsidian数据存储方式#系统目录|系统目录]]中，而不是仓库内部，以防止仓库相关数据丢失。这意味着快照是以笔记的绝对路径存储的。如果您最近移动了仓库，可能需要将其移回快照创建时的位置。

## 恢复快照

1. 打开**设置**。
2. 在侧边栏中，点击**插件选项**下的**文件恢复**。
3. 在**快照**旁边，点击**查看**。
4. 在左上角的文本框中，开始输入要恢复的文件名，您将看到一个建议列表。
5. 选择文件，按Enter，您将看到可用快照列表。
6. 选择要恢复的快照。
7. 点击**复制到剪贴板**以复制快照。
8. 将快照粘贴到原始笔记中，或者如果您要进行比较，可以粘贴到新笔记中。

## 清除快照历史记录

**注意：**清除快照历史将不可逆地删除仓库中的所有快照。

1. 打开**设置**。
2. 在侧边栏中，点击**插件选项**下的**文件恢复**。
3. 在**清除历史**旁边，点击**清除**。
4. 确认您要删除所有快照，点击**清除**。