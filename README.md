#获取米游社Cookie

注：
由于米忽悠修改了bbs接口导致一次获取的Cookie缺失，所以需要增加步骤

打开你的浏览器,进入无痕/隐身模式；
打开 http://bbs.mihoyo.com/ys 并进行登入操作;
在上一步登入完成后新建标签页，打开 http://user.mihoyo.com 并进行登入操作;
按下键盘上的F12或右键检查，打开开发者工具，点击Console/控制台，复制粘贴以下代码;
const cookie = document.cookie
const ask = confirm('Cookie:' + cookie + '\n\nDo you want to copy the cookie to the clipboard?')
if (ask == true) {
  copy(cookie)
  msg = cookie
} else {
  msg = 'Cancel'
}
然后安回车，此时Cookie已经复制到你的粘贴板上了。

配置文件
在MYS-Sign_In.js同级目录下创建ysconfig.json为文件，内容如下：

注：OCR_TOKEN获取

（不启用OCR验证码识别，OCR_TOKEN请留空，但不要删除）

{
  "YuanShen": [
    {
      "cookie": "",
      "OCR_TOKEN": "",
    },
    {
      "cookie": "",
      "OCR_TOKEN": ""
    },
    ...
  ]
}
