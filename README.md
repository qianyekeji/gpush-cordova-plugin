![cordova](https://qianyedoufu.com/images/cordova.png)
# 个推插件使用文档
##前言

###### 个推推送自定义Cordova插件
---
## 插件介绍
###该插件使用个推 SDK 实现了注册远程通知，获取客户注册id，接收远程推送通知消息，实现了本地推送，本地推送立即推送和定时推送，动态设置本地推送消息内容，实现了点击推送通知消息，直接打开App，抓取推送通知消息内容，把通知内容发送到前端。
---


###gpush-cordova-plugin使用方法
```
代码块
    <script>
    //注册推送
        function startpush() {
            var sendStr;
            //传值到原生
            sendStr = {
                "appid" : "Pt5O0RM0Za6HlRZs7s53z2",
                "appkey": "4PQOoJ0ifpAFoYmcSbcBf6",
                "appsecret":"iUJKGwDDBs5DtswxMSDLB1" 
            };
            
        gPushPlugin.startSDK(sendStr,function(data) {
            console.log('js收到推送消息'+data);
                                           },
                                        function(fail) {

                                            return;

                                        });
        }
        //本地推送
        function getuiLocal() {
            var sendStr;
            //传值到原生
            sendStr = {
                "msg" : "cordova中文网"
            };
            
        gPushPlugin.localPushMsg(sendStr,function(data) {
        alert(data);
                                                                  },
                                                                  function(fail) {

                                                                  return;

                                                                  });
        }
        //抓取推送消息通知内容
        function GPushOutputMessage(output){// 原生调用  js传递
        console.log('js收到推送消息'+output);
        }
        //获取客户注册个推推送ID
        function GPushGetClientId(output){// 原生调用  js传递
        console.log('收到客户id'+output);
        }
        

    </script>
```
## 完毕！
[README](https://qianyedoufu.com/app/plugins/gpush/README.md)