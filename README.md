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
## 使用示例
```
Data.get([{
            url:"demo1.json",
            type:"post",
            dataType:"json",
            done: function (data) {
                console.log("我执行完毕了");
            },
            fail: function () {
                console.log("我执行失败了");
            },
            always: function () {
                console.log("只要发起ajax请求我就会被执行");
            }
        },{
            url:"demo2.json",
            type:"post",
            dataType:"json",
            done: function (data) {
                console.log("我执行完毕了");
            },
            fail: function () {
                console.log("我执行失败了");
            },
            always: function () {
                console.log("只要发起ajax请求我就会被执行");
            }
        }],function(){
			//全部执行完毕后回调我
            alert("OK");
        });
```