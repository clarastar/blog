如何优化显示效果，在数据库的结果并不匹配的情况下？
通过mongoDB返回的json中的项目简介过长，在前端js中加了
str.substr(0,80)的代码，但是在页面加载中会有明显的文字全部显示又变少的效果。
尝试在server端将每个项目返回的summary变为80，forEach循环每一个project。
但是页面加载明显变慢，放弃。
将原本写在页面底部的js文件写在页面顶部:
$(document).ready(str.substr(0,80))
问题解决啦。

