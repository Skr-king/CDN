# 内容交付网络（CDN）

内容交付网络是一个通过在多个边缘服务器之间分发您的内容来卸载您的网站的系统。当您使用CDN时，内容将缓存在此网络中，并使用最近的边缘服务器进行传送，而不是直接访问服务器中的内容。如果您想了解更多信息，可以查看 [维基百科CDN](https://en.wikipedia.org/wiki/Content_delivery_network) 。

**本文档引用了本地存储的CDN。对于外部存储上的CDN，请查看此[链接](https://chevereto.com/docs/storages#storage-cdn)。**

## 如何工作

CDN服务通过使用“拉区”来工作，在您设置时，将会为您提供“CDN URL”或者“拉区链接”。提供的链接将用于替换静态内容中常规的链接。例如，假设您可以使用以下URL访问服务器中的图像：

```
http://demo.chevereto.com/image/picture.jpg
```

当您在Chevereto中打开CDN时，系统将使用CDN 链接替换您的默认链接，因此显示的链接将为

```markup
http://pullzone-url.at.cdn-service.com/image/picture.jpg
```

根据您的使用源（服务器的链接）将内容缓存到CDN上。整个过程需要利用时间来显示用户的最终修改，具体取决于您的网站内有多少活动。

## 启用CDN方法

首先，您需要在CDN提供商中创建一个拉区。要在Chevereto中启用CDN，请按如下步骤：

1. 在仪表盘中>设置中找到外部服务.
2. 在CDN菜单中“启用”CDN"
3. 填写CND链接
4. 保存修改

## 自定义域（CNAME记录）

您的CDN供应商会为您提供一个U链接，用于从您的网站提取内容并将其放入CDN。他们很可能会给你一个像如下这样的长网址：

```markup
http://pullzone-url.at.cdn-service.com/
```

您可以使用大多数CDN供应商提供的CNAME记录，因此您最终会得到如下链接：

```markup
http://cdn.mydomain.com/
```

使用CNAME的好处是，当您更改CDN的供应商时，更改过程将是无缝链接的，并且URL将会继续工作，并且没有任何更改。此外，如果您选择关闭CDN，只需将CNAME更改为您的域名，其他一切配置都将继续有效。在此，我们强烈建议您将CDN与CNAME一起使用。

有关如何使用CNAME记录的说明，请咨询您的CDN提供商。