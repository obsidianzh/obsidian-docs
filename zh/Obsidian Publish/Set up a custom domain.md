You can set up a custom domain or subdomain for your [[Introduction to Obsidian Publish|Obsidian Publish]] site.

> [!warning]
> At the moment, we only support configuring custom domains using the following methods:
>
> - [[#Set up using CloudFlare]] using [Full mode](https://developers.cloudflare.com/ssl/origin-configuration/ssl-modes/full/).
> - [[#Set up using a proxy]]
> 
> We don't yet have a way to provision an SSL certificate on your behalf.

## Set up using CloudFlare

The easiest way to set up a custom domain or subdomain is to create a [CloudFlare](https://cloudflare.com) account and let CloudFlare manage your domain's DNS.

The following steps use CloudFlare to configure a custom domain for your Obsidian Publish site, either using a root domain (`mysite.com`) or a subdomain (`notes.mysite.com`).

> [!important]
> CloudFlare is the **only officially supported provider** for setting up custom domains. Using the following instructions with any other providers will likely not work.

**CloudFlare:**

1. Open Cloudflare to the domain where you want to host your Publish site, such as `mysite.com`, even if you want a subdomain like `notes.mysite.com`.
2. Go to **DNS** and click **Add Record**.
3. Select **CNAME**.
4. In **name**, enter your domain or subdomain, for example `notes.mysite.com`.
5. In **target**, enter `publish-main.obsidian.md`. Don't include your personal sub-URL in this value. Obsidian Publish handles this from your configuration.
6. Make sure that **proxy status** is enabled. It should be enabled by default.
7. Go to **SSL/TLS** and set the SSL/TLS encryption mode to "Full" to configure the SSL/TLS certificate automatically.

> [!note]
> To redirect both `mysite.com` and `www.mysite.com` to Obsidian Publish, you need to create a [Page Rule](https://support.cloudflare.com/hc/en-us/articles/200172336-Creating-Page-Rules) with the following settings:
>
> - URL match: `www.mysite.com/*`
> - Forward URL - 301 Permanent Redirect
> - Redirect URL: `https://mysite.com/$1`
>
> After you've created the page rule, create a CNAME record for `www.mysite.com` just like you did for `mysite.com`.

**Obsidian:**

1. Open Obsidian on your computer.
2. In the [[Ribbon]] at the left, click **Publish changes** (paper plane icon).
3. Under **Publish changes**, select **Change site options** (cog icon).
4. Next to **Custom domain**, select **Configure**.
5. In **Custom URL**, enter the URL to your domain or subdomain.

> [!note]
> If your custom domain setup ends up in a redirect loop, it's likely that the encryption mode in CloudFlare has been set to "Flexible" instead of "Full".

## Set up using a proxy

You can also set up SSL/TLS for your custom domain by using your own web server.

If you are already hosting a website under your domain or subdomain, you can also use this option and set up your website to load your Obsidian Publish site under a specific URL path, instead of hosting the full site.

Proxy all requests under that URL path to `https://publish.obsidian.md/serve?url=mysite.com/my-notes/...` and configure the site options in Obsidian to the same URL path, by setting **Custom URL** to `mysite.com/my-notes`.

You can also set up Obsidian Publish as a sub-URL of a site you own. For example, `https://mysite.com/my-notes/`. To achieve this, you must host your own server and proxy all requests to our server at `https://publish.obsidian.md/`.

### NGINX

In your NGINX configuration, add the following:

```nginx
location /my-notes {
  proxy_pass https://publish.obsidian.md/serve?url=mysite.com/my-notes/;
  proxy_ssl_server_name on;
  proxy_set_header Host publish.obsidian.md;
}
```

### Apache

In `.htaccess`, add the following:

```htaccess
RewriteEngine  on
RewriteRule    "^my-notes/(.*)$"  "https://publish.obsidian.md/serve?url=mysite.com/my-notes/$1"  [L,P]
```

> [!note]
> `mod_rewrite` must be enabled, and you may also need to configure [SSLProxyEngine](https://stackoverflow.com/questions/40938148/reverse-proxy-for-external-url-apache)

### Netlify

```plain
[[redirects]]
  from = "https://mysite.com/my-notes/*"
  to = "https://publish.obsidian.md/serve?url=mysite.com/my-notes/:splat"
  status = 200
  force = true
```

### Vercel

In `vercel.json`, [configure rewrites](https://vercel.com/docs/configuration#project/rewrites):

```json
{
  ...

  "rewrites": [
    {
      "source": "/my-notes/",
      "destination": "https://publish.obsidian.md/serve?url=mysite.com/my-notes"
    },
    {
      "source": "/my-notes/:path*",
      "destination": "https://publish.obsidian.md/serve?url=mysite.com/my-notes/:path*"
    }
  ]
}
```

### Caddy

```plain
mysite.com {
  encode zstd gzip
  handle /my-notes* {
    reverse_proxy https://publish.obsidian.md {
      header_up Host {upstream_hostport}
    }
    rewrite * /serve?url=mysite.com{path}
  }
}
```

### Traefik

This minimal configuration excerpt redirects `mysite.com` to Obsidian publish.
See the [Traefik documentation](https://doc.traefik.io/traefik/routing/overview/)
for a complete example.

```yaml
http:
  routers:
    mysite:
      rule: Host(`mysite.com`)
      service: obsidian-publish
      middlewares:
        - "publish-headers"
  services:
    obsidian-publish:
      loadBalancer:
        servers:
          - url: https://publish.obsidian.md
  middlewares:
    publish-headers:
      headers:
        customRequestHeaders:
          Host: "publish.obsidian.md"
          x-obsidian-custom-domain: "mysite.com"
```

### Supported HTTP X-Headers

If your proxy service doesn't allow query paths, you can use `https://publish.obsidian.md/` with a custom header `x-obsidian-custom-domain` set to your site URL `mysite.com/my-subpath`.

## Redirect old site to custom domain

If you want to redirect your visitors from the old `publish.obsidian.md` site to your new custom domain, enable the **Redirect to your custom domain** option when configuring your custom domain.

## Troubleshoot

Once you set up your custom domain, if you've visited your site from your previous `https://publish.obsidian.md/slug` link, you may have to clear your browser cache for certain things (like fonts, graphs, or password access) to work properly. This is due to the cross-domain security restrictions that are imposed by modern browsers. The good news is that readers of your site should never run into issue this if you only let visitors use your custom domain.


---

中文翻译：
你可以为你的[[Obsidian Publish|Obsidian发布]]站点设置自定义域名或子域名。

> [!警告]
> 目前，我们仅支持使用以下方法配置自定义域名：
>
> - 使用[CloudFlare](https://cloudflare.com)的[全模式](https://developers.cloudflare.com/ssl/origin-configuration/ssl-modes/full/)。
> - 使用代理设置。
> 
> 我们目前还没有为您代劳配置SSL证书的方式。

## 使用 CloudFlare 进行设置

设置自定义域名或子域名的最简单方式是创建一个[CloudFlare](https://cloudflare.com)账户，并让CloudFlare管理您的域名DNS。

以下步骤使用CloudFlare为您的Obsidian Publish站点配置自定义域名，无论是使用根域名（`mysite.com`）还是子域名（`notes.mysite.com`）。

> [!重要]
> CloudFlare是**唯一官方支持的提供商**，用其他提供商按照以下说明进行设置可能不会成功。

**CloudFlare:**

1. 打开Cloudflare到您想要托管发布站点的域名，比如`mysite.com`，即使您想要一个子域名如`notes.mysite.com`。
2. 转到**DNS**并点击**添加记录**。
3. 选择**CNAME**。
4. 在**名称**中输入您的域名或子域名，例如`notes.mysite.com`。
5. 在**目标**中输入`publish-main.obsidian.md`。在该数值中不要包含您的个人子URL。Obsidian Publish会在您的配置中处理这一点。
6. 确保**代理状态**已启用。默认情况下应该是启用的。
7. 转到**SSL/TLS**并将SSL/TLS加密模式设置为“Full”，以便自动配置SSL/TLS证书。

> [!注意]
> 要将`mysite.com`和`www.mysite.com`都重定向到Obsidian Publish，您需要创建一个[页面规则](https://support.cloudflare.com/hc/en-us/articles/200172336-Creating-Page-Rules)，具体设置如下：
>
> - URL匹配：`www.mysite.com/*`
> - 转发URL - 301永久重定向
> - 重定向URL：`https://mysite.com/$1`
>
> 创建完页面规则后，为`www.mysite.com`创建一个CNAME记录，就像为`mysite.com`做的一样。

**Obsidian:**

1. 在您的电脑上打开Obsidian。
2. 在左侧[[Ribbon]]中，点击**发布更改**（纸飞机图标）。
3. 在**发布更改**下，选择**更改站点选项**（齿轮图标）。
4. 在**自定义域名**旁，选择**配置**。
5. 在**自定义URL**中，输入您的域名或子域名。

> [!注意]
> 如果您的自定义域名设置最终陷入重定向循环，很可能是因为CloudFlare中的加密模式设置为“Flexible”而不是“Full”。

## 使用代理进行设置

您也可以通过使用自己的Web服务器为自定义域名设置SSL/TLS。

如果您已经在您的域名或子域名下托管了一个网站，您也可以使用这个选项，将您的网站设置为在特定URL路径下加载您的Obsidian Publish站点，而不是完全托管整个站点。

将所有请求代理到`https://publish.obsidian.md/serve?url=mysite.com/my-notes/...`的URL路径下，并在Obsidian中的站点选项中将**自定义URL**设置为`mysite.com/my-notes`。

您还可以将Obsidian Publish设置为您拥有的站点的子URL。例如，`https://mysite.com/my-notes/`。为此，您必须托管自己的服务器，并将所有请求代理到我们的服务器`https://publish.obsidian.md/`。

### NGINX

在您的NGINX配置中添加以下内容：

```nginx
location /my-notes {
  proxy_pass https://publish.obsidian.md/serve?url=mysite.com/my-notes/;
  proxy_ssl_server_name on;
  proxy_set_header Host publish.obsidian.md;
}
```

### Apache

在`.htaccess`中添加以下内容：

```htaccess
RewriteEngine  on
RewriteRule    "^my-notes/(.*)$"  "https://publish.obsidian.md/serve?url=mysite.com/my-notes/$1"  [L,P]
```

> [!注意]
> 必须启用`mod_rewrite`，您可能还需要配置[SSLProxyEngine](https://stackoverflow.com/questions/40938148/reverse-proxy-for-external-url-apache)。

### Netlify

```plain
[[redirects]]
  from = "https://mysite.com/my-notes/*"
  to = "https://publish.obsidian.md/serve?url=mysite.com/my-notes/:splat"
  status = 200
  force = true
```

### Vercel

在`vercel.json`中，[配置重写](https://vercel.com/docs/configuration#project/rewrites)：

```json
{
  ...

  "rewrites": [
    {
      "source": "/my-notes/",
      "destination": "https://publish.obsidian.md/serve?url=mysite.com/my-notes"
    },
    {
      "source": "/my-notes/:path*",
      "destination": "https://publish.obsidian.md/serve?url=mysite.com/my-notes/:path*"
    }
  ]
}
```

### Caddy

```plain
mysite.com {
  encode zstd gzip
  handle /my-notes* {
    reverse_proxy https://publish.obsidian.md {
      header_up Host {upstream_hostport}
    }
    rewrite * /serve?url=mysite.com{path}
  }
}
```

### Traefik

这个最小配置摘录将`mysite.com`重定向到Obsidian发布。
查看[Traefik文档](https://doc.traefik.io/traefik/routing/overview/)获取完整示例。

```yaml
http:
  routers:
    mysite:
      rule: Host(`mysite.com`)
      service: obsidian-publish
      middlewares:
        - "publish-headers"
  services:
    obsidian-publish:
      loadBalancer:
        servers:
          - url: https://publish.obsidian.md
  middlewares:
    publish-headers:
      headers:
        customRequestHeaders:
          Host: "publish.obsidian.md"
          x-obsidian-custom-domain: "mysite.com"
```

### 支持的HTTP X-Headers

如果您的代理服务不允许查询路径，您可以使用`https://publish.obsidian.md/`，并设置一个自定义头`x-obsidian-custom-domain`，将其设置为您的站点URL`mysite.com/my-subpath`。

## 将旧站点重定向到自定义域名

如果您想将访问者从旧的`publish.obsidian.md`站点重定向到新的自定义域名，请在配置自定义域名时启用**重定向到您的自定义域名**选项。

## 故障排除

一旦设置了自定义域名，如果您从以前的`https://publish.obsidian.md/slug`链接访问您的站点，您可能需要清除浏览器缓存，以使某些内容（如字体、图表或密码访问）能够正常工作。这是由现代浏览器强加的跨域安全限制所致。好消息是，如果您只允许访客使用您的自定义域名，那么您的站点读者应该永远不会遇到这个问题。