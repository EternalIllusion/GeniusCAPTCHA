# GeniusCAPTCHA3

一个整人专用的虚假验证码。
试玩链接：[🔗点我](https://eterill.xyz/GeniusCAPTCHA/)

## 功能

- 假验证码

- 在没有红绿灯的9张超级糊的图中选择红绿灯

- 假广告（也可以是真的）

## 配置与使用

你只需要配置好`main.js`中开头部分的内容就行了

```javascript
var target = "http://bing.com/"//通过验证后要跳转到哪里
var btnBefore = "请先进行验证";//点击验证码前按钮文字
var btnDuring = "验证中...";//完成验证码前按钮的文字
var btnAfter = "刷新重试";//验证失败按钮文字
var btnPass = "点击跳转";//验证成功按钮文字
var config = {
    element: "#captcha",//用来选择验证码div
    textBefore: "点击进行入机身份验证",//验证码被点击前文字
    textDuring: "正在验证，请稍等...",//验证过程文字
    textAfter: "未通过验证,您可能是入机。",//验证失败文字
    textPass: "验证通过",//验证成功文字
    dark: false,//是否暗黑模式，适配没做完，做好别用
    imgnum: 15//图库里有几张图
};
var adtitle = '骷髅打金服，上线就送VIP!';//自定义假广告标题
var adimg = "./fakeAD.webp";
var adcont = '<a href="http://eterill.xyz/"><img src="' + adimg + '"></img></a>';//假广告内容，也可以是真的广告
var addur = Math.floor(Math.random() * (20000 - 10000 + 1)) + 15000;//广告每个多少ms弹出一次，这里是15-25秒随机
```

### 自定义验证码图片

图片的标题请在 `index.html` 中修改 `红绿灯` 字样。

图片文件存放在 `\img` 目录下，命名为 `数字.webp` 数字从1开始，（不是从0开始！！！），格式为webp。

修改完图片记得更新配置中图片数量。制作图片建议用 `99*99` 分辨率拉伸到 `120*120` ~~，糊得更清晰（~~

## 引用和鸣谢

使用并融合了fucklinux/fakeCAPTCHA和fakeCAPTCHAtest,相当于融合怪。

感谢@cbbff666的灵感和支持。

