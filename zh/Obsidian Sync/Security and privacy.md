---
aliases:
  - Security/privacy for Obsidian Sync
  - Access control for Obsidian Sync
---
## Encryption

For your safety, [[Introduction to Obsidian Sync|Obsidian Sync]] encrypts your [[Local and remote vaults|remote vault]] and all communication with Obsidian's servers. Before anyone can access your remote vault, they first need to decrypt it with an _encryption password_.

When you create a new remote vault, you have two options:

- **End-to-end encryption:** Obsidian encrypts the vault on your device with a custom encryption key before it's sent to Obsidian's servers. This guarantees that no one—not even the Obsidian team—can access your notes.
- **Managed encryption:** If you don't want to have to remember another password, you can let Obsidian manage the encryption password for you. While we store your encryption password on our servers, we only use it to offer a more convenient way to manage your vaults.

If you forget or lose your custom encryption password, your data remains encrypted and unusable forever. We're not able to recover your password, or any encrypted data for you.

Your choice only affects your remote vault. Obsidian doesn't encrypt your local vault.
### What does end-to-end encryption mean?

End-to-end encryption means that the data is encrypted from the moment it leaves your device, and can only be decrypted using your encryption key once it's back on one of your devices.

We can't read your data. Neither can any potential eavesdroppers, such as your internet service provider.

In the rare case of a complete server breach, your data remains encrypted—no one can decrypt your files without knowing your password.

### What encryption do you use?

For data security, we implement industry-standard encryption protocols. Specifically, we use [AES-256](https://www.nist.gov/publications/advanced-encryption-standard-aes-0), the strongest encryption standard, widely employed in contexts such as online banking. The encryption process involves the following technical details:

- **Key derivation function:** [scrypt](https://en.wikipedia.org/wiki/Scrypt) with salt
- **Encryption algorithm:** AES-256 using [Galois/Counter Mode (GCM)](https://en.wikipedia.org/wiki/Galois/Counter_Mode)

### Can I verify that my data is end-to-end encrypted?

Yes. See our guide, [how to verify Obsidian Sync's end-to-end encryption](https://obsidian.md/blog/verify-obsidian-sync-encryption/). This guide provide step-by-step instructions for you to trustlessly verify the end-to-end encryption of your data when it is sent and received via Sync servers.

### Has Obsidian completed a third-party security audit?

Yes. Obsidian has been independently audited. Visit our [Security page](https://obsidian.md/security) to view audit reports. Regular audits by third-party security firms ensure that Obsidian code and procedures meet the highest security standards.

### What happens if I forget my encryption password?

If you ever lose or forget the encryption password, you won't be able to connect additional vaults to your remote vault. Since the encryption password isn't saved anywhere, it's forever lost.

Your data, however, are usually safely stored locally on each of your devices.

To continue using Obsidian Sync, we suggest doing a full re-setup to be able to add new devices to your Sync system:

1. Make a full vault backup on your primary device, just in case something goes wrong. This can be as simple as making a copy of the vault folder, or creating a zip file from the vault.
2. Disconnect the remote vault in each of your devices. This can be done by going to **Settings → Sync → Pick remote vault → Disconnect**.
3. Create a new remote vault on your primary device from the same Settings page. Optionally, you can delete the previous remote vault since you don't have the password for it anyway. (You may have to delete the previous remote vault if you are at the vault limit)
4. Wait for your primary device to sync. Watch the sync indicator at the bottom right of the screen until it displays a green checkmark.
5. Connect each of your device to the same newly created remote vault. When connecting, you will be shown a warning about vault merging, this is expected and you can proceed. Wait for each device to fully sync before moving onto the next. This reduces the chances of issues.
6. Now all your devices should be connected to the new remote vault.

## Hosting
### Where do you host the servers for Obsidian Sync?

Our data centers, powered by [DigitalOcean](https://www.digitalocean.com), provide geo-regional remote vault hosting options in the following locations:

> [!info] Sync geo-regions
> **Automatic**: Your data center is chosen based off your IP location.
> 
> **Asia**: Singapore
> **Europe**: Frankfurt, Germany
> **North America**: San Francisco, USA 
> **Oceania**: Sydney, Australia
^sync-geo-regions
### I have sync-x as my server. Where is it hosted?

The list below corresponds the Sync servers to their respective data centers. 

**San Francisco**
- `sync-01` to `sync-12`
- `sync-14` to `sync-15`

**Frankfurt**
- `sync-13`
- `sync-16`

**Singapore**
- `sync-17`

**Sydney**
- `sync-18`
## Network and access

### Managing access to Obsidian Sync on your network

To regulate access to Obsidian Sync on your network, you need to manage the following domains:

`sync-xx.obsidian.md`

The `xx` in this case represents a number ranging from `1 - 100`.

> [!tip] If your firewall system supports it, we recommend whitelisting `sync-*.obsidian.md` to account for the continuous growth in subdomain numbers.


---

中文翻译：
---
aliases:
  - Obsidian Sync 的安全与隐私
  - Obsidian Sync 的访问控制
---
## 加密

为了您的安全起见，[[Introduction to Obsidian Sync|Obsidian Sync]] 对您的[[本地和远程仓库|远程仓库]]以及与 Obsidian 服务器的所有通信进行加密。在任何人能够访问您的远程仓库之前，他们首先需要使用一个 _加密密码_ 对其进行解密。

当您创建一个新的远程仓库时，您有两个选项：

- **端到端加密：** Obsidian 在将仓库发送到 Obsidian 服务器之前，使用自定义加密密钥在您的设备上对其进行加密。这确保没有人——甚至是 Obsidian 团队——可以访问您的笔记。
- **托管加密：** 如果您不想记住另一个密码，可以让 Obsidian 为您管理加密密码。虽然我们会将您的加密密码存储在我们的服务器上，但我们只会用它来提供一种更方便的方式来管理您的仓库。

如果您忘记或丢失了自定义的加密密码，您的数据将保持加密状态，永远无法使用。我们无法为您找回密码，或者为您解密任何加密数据。

您的选择仅影响您的远程仓库。Obsidian 不会对您的本地仓库进行加密。
### 什么是端到端加密？

端到端加密意味着数据在离开您的设备时就已经被加密，只能在返回到您的设备之一时使用您的加密密钥进行解密。

我们无法阅读您的数据。潜在的窃听者，比如您的互联网服务提供商，也无法阅读。

在极少数情况下出现完全服务器遭到入侵的情况下，您的数据仍然是加密的——没有人可以在不知道您的密码的情况下解密您的文件。

### 我们使用什么样的加密？

为了数据安全，我们实施行业标准的加密协议。具体来说，我们使用 [AES-256](https://www.nist.gov/publications/advanced-encryption-standard-aes-0)，这是最强大的加密标准，在在线银行等领域被广泛应用。加密过程涉及以下技术细节：

- **密钥派生函数：** [scrypt](https://en.wikipedia.org/wiki/Scrypt) 与盐
- **加密算法：** 使用 [Galois/Counter Mode (GCM)](https://en.wikipedia.org/wiki/Galois/Counter_Mode) 的 AES-256

### 我可以验证我的数据是否端到端加密吗？

可以。请查看我们的指南，[如何验证 Obsidian Sync 的端到端加密](https://obsidian.md/blog/verify-obsidian-sync-encryption/)。该指南提供了逐步说明，让您可以在通过 Sync 服务器发送和接收数据时，无需信任地验证数据的端到端加密。

### Obsidian 是否进行过第三方安全审计？

是的。Obsidian 已经进行了独立审计。请访问我们的[安全页面](https://obsidian.md/security)查看审计报告。第三方安全公司定期审计确保 Obsidian 代码和流程符合最高安全标准。

### 如果我忘记了我的加密密码会发生什么？

如果您忘记了或丢失了加密密码，您将无法将其他仓库连接到您的远程仓库。由于加密密码没有保存在任何地方，它将永远丢失。

但是，您的数据通常安全地存储在每台设备上。

为了继续使用 Obsidian Sync，我们建议进行完整重新设置以能够将新设备添加到您的 Sync 系统：

1. 在您的主设备上对仓库进行完整备份，以防出现问题。这可以简单地是复制仓库文件夹，或者从仓库创建一个 zip 文件。
2. 在每台设备上断开远程仓库的连接。这可以通过转到**设置 → 同步 → 选择远程仓库 → 断开连接**来完成。
3. 在主设备上从同一设置页面创建一个新的远程仓库。可选地，您可以删除之前的远程仓库，因为无论如何您都没有其密码。（如果您已达到仓库限制，可能需要删除之前的远程仓库）
4. 等待主设备同步。观察屏幕右下角的同步指示器，直到显示绿色勾号。
5. 将每台设备连接到同一新创建的远程仓库。在连接时，您将收到有关仓库合并的警告，这是正常现象，您可以继续。等待每个设备完全同步后再进行下一步。这样可以减少出现问题的可能性。
6. 现在您的所有设备应该连接到新的远程仓库。

## 主机
### Obsidian Sync 的服务器托管在哪里？

由 [DigitalOcean](https://www.digitalocean.com) 提供支持的我们的数据中心在以下位置提供地理区域的远程仓库托管选项：

> [!info] 同步地理区域
> **自动**：您的数据中心根据您的 IP 地理位置进行选择。
> 
> **亚洲**：新加坡
> **欧洲**：德国法兰克福
> **北美**：美国旧金山
> **大洋洲**：澳大利亚悉尼
^sync-geo-regions
### 我的服务器是 sync-x。它托管在哪里？

以下列表对应了 Sync 服务器及其相应的数据中心。

**旧金山**
- `sync-01` 到 `sync-12`
- `sync-14` 到 `sync-15`

**法兰克福**
- `sync-13`
- `sync-16`

**新加坡**
- `sync-17`

**悉尼**
- `sync-18`
## 网络和访问

### 如何管理您网络中对 Obsidian Sync 的访问

要管理您网络中对 Obsidian Sync 的访问，您需要管理以下域：

`sync-xx.obsidian.md`

这里的 `xx` 表示从 `1 - 100` 的数字范围。

> [!tip] 如果您的防火墙系统支持，我们建议将 `sync-*.obsidian.md` 加入白名单，以适应子域号不断增加的情况。