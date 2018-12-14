# qrcode
简陋的。。网址，用来将文本内容转换为二维码图片展示出来<br/>
## 需求来源
因为目前在做支付相关的开发，最近对接的第三方支付通道，其中包含了C扫B的接口，即用户扫商家的二维码进行支付。该接
口req入参包含订单金额相关内容，res出参为生成的码信息，如微信可能是这样的：weixin：//wxpay/s/An4baqw，支付宝的可能是这样的
：https://qr.alipay.com/bavh4wjlxf12tper3a<br/>
为了测试支付需要将这样的内容需要进行转换，转换成二维码图片，以便扫码支付。所以coding了代码，并挂到服务器上，便于日后测试。
<br/>

## demo介绍
该code可以将文本内容转换成二维码图片显示出来，转换文本限于除中文以外的内容<br/>
demo为index.html，可以将所有文件放入webapp下即可<br/>
**网站效果图**
![网页效果图](https://github.com/Jump-Boy/qrcode/blob/master/qrcode.png)

**网站地址**
[点此访问](http://www.yauwdxk.xyz:8080/qrcode)

* code原理<br/>
该demo的核心技术点也是唯一技术点就是通过第三方提供的JQuery工具库来完成二维码的转换，用js代替服务，减少服务器压力。<br/>

* 第三方JQuery库  https://github.com/jeromeetienne/jquery-qrcode
> jquery.qrcode.js is jquery plugin for a pure browser qrcode generation. It allow you to easily add qrcode
 to your webpages. It is standalone, less than 4k after minify+gzip, no image download. It doesnt rely on 
 external services which go on and off, or add latency while loading. It is based on a library which build
  qrcode in various language. jquery.qrcode.js wraps it to make it easy to include in your own code.