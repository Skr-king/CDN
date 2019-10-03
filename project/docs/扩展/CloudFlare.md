# CloudFlare

CloudFlare是一种反向代理，广泛地应用于网站加速和提高网站的安全性。Chevereto中的CloudFlare的实现仍在进行中，因此某些功能可能无法按预期实现，但大多数的功能已经可以正常运行。

## 启用CloudFlare

要启用CloudFlare，您只需要创建一个账号并按照步骤操作就可以了。值得注意的是，您需要对您的网站DNS进行一些更改。由于我们常见托管公司与CloudFare建立了合作关系，您可以直接从您的托管账号中启用CloudFlare。

## CloudFlare HTTPS

CloudFare提供了大量的HTTPS的解决方案，您可以轻松的打开或关闭网站上的SSL。根据您要处理的证书类型，他们提供了“灵活”，“完整”的SSL变体。要启用HTTPS，请按以下步骤操作：

1. 转到您的网站。
2. 点击齿轮图标，然后选择“CloudFlare设置”。
3. 在下边找到SSL部分，然后选择您的配置。

### 强制 使用HTTPS

默认情况下，CloudFlare  HTTPS不会强制所有流量通过HTTPS。如果要强制HTTPS，请按照如下操作：

1. 登录您的网站
2. 登记齿轮图标并选择“页面选择”。
3. 在链接模式中输入您的网站
4. 切换“始终使用HTTPS”开关
5. 点击底部的“添加规则”

通过如上操作，您的网站所有流量都将使用HTTPS。当有人使用HTTP访问您的网站时，CloudFlare会将这些请求重新定向到HTTPS.

## 更多帮助

如果您需要更多帮助，请访问[CloudFlare Support](https://support.cloudflare.com/)。当然了您也可以联系 [Chevereto support](https://chevereto.com/support) ，我们将为您提供优质的服务。

































