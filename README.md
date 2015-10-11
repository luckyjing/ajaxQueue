# ajaxQueue
## 请求可以分为以下一种情况
* 多个ajax请求同时发送，相互无依赖。 
* 多个ajax请求相互依赖，必须有先后顺序。 
* 多个请求被同时发送，只需要最后一个请求。 
### 1.情况1-多个ajax请求同时发送，相互无依赖
```
ajaxQueue1文件夹
ajaxQueue-requireJS //为符合AMD规范的文件，可以直接作为requireJS的模块导入
```