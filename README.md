# my-raw-tool-set
**本工具集针对日文ocr翻译和tts，尤其是在日漫中效果特别好。**
_本人的工作只是搬运，并且把这些工具都串起来罢了，Modify为个人修改或者添加的部分_

**总体思路**：`Snipaste`截图保持到剪切板 → `manga-ocr`提取剪切板中图片中的文字再保存到剪切板 → `LunaTranslator`读取剪切板日文并且进行翻译和发送到vits-api获取语音


### Snipaste-2.8.5-Beta-x64-rd213rev.zip
`F1`截图，复制图片到剪切板
> From: [Snipaste](https://www.snipaste.com/)


### vits-simple-api-manga-ocr-rd213rev.zip
1. 因为是分压，所以直接解压`.zip`，`.z01`放着就好；
2. 打开`start.bat`（vits-api，已包含[zomehwh发布的804个语音](https://huggingface.co/spaces/zomehwh/vits-uma-genshin-honkai)）和`clip\manga-ocr.bat`（能从剪切板中的图片中提取出日文，使用的是日漫特化的ocr模型，所以只能识别日文）；
> From: [vits-simple-api](https://github.com/Artrajz/vits-simple-api) & [manga-ocr](https://github.com/kha-white/manga-ocr)
> Modify: 两个项目的整合，新增`clip`文件夹，`clip\manga-ocr.bat`。~~剩下的文件是本人编写的Chrome插件[AnonTranslator](https://github.com/raindrop213/AnonTranslator)中用到的，用于阅读EPUB小说，感兴趣的话请自行查看~~


### LunaTranslator-gui-rd213rev.zip
F4查看设置面板（不要使用ocr，要使用剪切板模式，这样就能输入`mange-ocr`识别的文字）
> From: [LunaTranslator](https://github.com/HIllya51/LunaTranslator)
> Modify: 语音方面添加了vitsapi接口，让`LunaTranslator`可以使用`vits-simple-api`的语音


