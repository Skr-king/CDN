# ShareX

[ShareX](https://en.wikipedia.org/wiki/ShareX) 是一个Windows实用程序，您可以将图像，截屏，文本和其他类型的内容上传到多个提供的程序。借助[Chevereto API](https://chevereto.com/docs/api-v1)，您可以轻松地在Chevereto网站上使用通过ShareX从您的计算机上传图像。

## 下载ShareX

ShareX是免费的开源软件。您可以从ShareX官方网站上下载，下载后将其安装到您的电脑中。

## 将Chevereto添加到ShareX

从ShareX版本9.4.0开始，您只需：

1. 找到image destination地设置
2. 选择«Chevereto»
3. 填写您的网站信息

对于ShareX旧版本，您需要手动将Chevereto导入ShareX。首先请将以下代码块复制并进行编辑，以匹配您的Chevereto安装。

```javascript
{
  "Name": "Chevereto",
  "RequestType": "POST",
  "RequestURL": "http://mysite.com/api/1/upload", // edit this
  "FileFormName": "source",
  "Arguments": {
	"key": "your API key goes here", // edit this
	"format": "redirect",
	"source": "%input"
  },
  "ResponseType": "RedirectionURL",
  "RegexList": [],
  "URL": "",
  "ThumbnailURL": "",
  "DeletionURL": ""
}
```

准备好编辑的代码后，请复制所有代码并按照如下步骤：

1. 打开ShareX
2. 点击“目标”，然后转到“目标设置...”
3. 向下滚动并点击“自定义上传”
4. 点击“导入”，然后点击“从剪贴板”（位于左侧的列）

您将看到代码块中的信息已添加到ShareX。单击“图像上传器”部分旁边的“测试”。您可以在“测试结果”日志中看到如下的内容：

```markup
URL: http://mysite.com/image/<id>
```

如果一切正确，您将看到ShareX已准备好直接上传到您的Chevereto网站。

## 将图像上传到用户帐号

Chevereto API V1可以将图像作为访客上传。如果要将图像上传到指定用户，请查看 [API用户上传解决方法](https://chevereto.com/docs/api-v1#api-user)。

## 更多帮助

有关于ShareX和Chevereto的更多帮助，请参考 [ShareX and Chevereto](https://chevereto.com/community/threads/sharex-and-chevereto.5254/)。



































