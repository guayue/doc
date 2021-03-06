#各种通知
通知，是一种**非模态形式**的信息告知方式，以不扰民为宗旨，效果清爽炫酷为亮点。在我写这段话的时候，后web2.0时代常见的Web网站和移动App上，保守估计，流行过的通知类型大概有300多种。

弱水三千，我们只能取一瓢饮了。

# Growl-like 类通知
###简介

![](/assets/notify.jpg)

目前在PC端最常用到一种信息推送方式，很符合web2.0时代人们的阅读习惯，大概98%用alert函数的场景，都可以用这种方式来替代了。这种消息提示方式具备以下特点：

* 可灵活定位，当然常见位置是右上、上中、右下，但一般不需要用户拖拽其位置。
* 可由用户手工关闭，也具备定时自动关闭的功能。
* 短时间内的多条消息可以列表显示。
* 支持多种消息类型（成功提示／错误报警／信息提示）。
* (Best to have)可灵活定制消息内容、消息标题、以及出现／隐藏的动画效果
* 开源，免费，更新活跃

###最佳实践

成功提示消息位置为右上角，颜色为绿色，如消息发送成功、上传成功。但是如果操作成功的效果能从页面中体现，则不需要再出现提示了，否则会造成用户困扰。例如从列表中删除数据，删除成功后从列表中移除相应数据，用户已经得到反馈（删除成功了），那么就不需要再弹出消息了。

>所有的消息提示和弹窗，都要克制得使用，弹窗有毒过度使用会造成用户厌恶

信息提示消息位置为右上角，颜色为蓝色，如收到新消息。此类提示消息一定要过滤重复消息，不要造成同类消息大量堆积。

错误提示消息位置为页面正上方，颜色为红色，如消息发送失败、链接中断等。一般来说错误提示消息不建议会自动关闭，需要用户手工去关闭，已起到让用户注意的效果。

所有的信息提示控件宽度应该统一定宽定高，同时信息提示内容应该简洁精炼，不要导致控件宽高失调，更不要出现内部滚动条。

###推荐的类库：

**Angular2的最佳选择**：[PrimeNG Growl](http://www.primefaces.org/primeng/#/growl)

实现方式：

非Angular2的系统，可以考虑如下控件：

[Toastr](http://codeseven.github.io/toastr/demo.html)

[bootstrap-notify](https://github.com/mouse0270/bootstrap-notify)

## Inline 通知
相对于Growl-like类的消息通知，inline消息

