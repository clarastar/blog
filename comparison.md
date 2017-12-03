# Angular 中$http,$resource,restangular的不同点
$http是angular自带的，处理比较简单的api请求
$resource也是angular自带的，处理更复杂的api请求
restangular则是需要引入才可以，处理负责数据结构的api请求，
同时不会产生多余的boilertemplate


#Mongoose 的findOneAndUpdate create
在添加新的project的时候用的Model.create(project,cb);
在修改原有的project，保存的时候用的Model.findOneAndUpdate(query,data,options,cb);
但是在cb中处理err以后，返回状态吗200 ctx.status=200,服务器端则会一直报错 
headers have already been sent，
将返回状态码的code写在回调函数外，则顺利执行