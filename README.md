## 概述

CallSDK基于[ILiveSDK](https://github.com/zhaoyang21cn/ILiveSDK_Android_Demos)，实现双人视频(多人)业务功能封装，方便开发者快速搭建自己的视频聊天服务

![](https://zhaoyang21cn.github.io/ilivesdk_help/readme_img/ilivesdk_construction.png)



## 集成
CallSDK在Android Studio上开发。 导入只需要在gradle里增加一行（后面是版本号）,查看[版本更新说明](./doc/release.md)

*导入CallSdk *

compile 'com.tencent.callsdk:callsdk:1.0.15'

*导入iLiveSDK *

compile 'com.tencent.ilivesdk:ilivesdk:1.3.4'

ps: 上面iLiveSDK的版本请使用[最新版本](https://github.com/zhaoyang21cn/ILiveSDK_Android_Demos)

## API文档
[API文档1.0.15](https://zhaoyang21cn.github.io/ilivesdk_help/callsdk/)


## 功能概述

CallSdk可以使用ILiveSDK的所有功能:
>* 帐号体系(资料托管)
>* 个人关系链
>* 群组管理
>* 音视频通讯
>* 美颜/美白
>* 视频推流/录制

效果图(仅供参考):

![contact](https://zhaoyang21cn.github.io/ilivesdk_help/readme_img/contact.png)
![contact](https://zhaoyang21cn.github.io/ilivesdk_help/readme_img/call.png)

## 主要接口介绍

登录相关请参考ILiveSDK：[https://github.com/zhaoyang21cn/ILiveSDK_Android_Demos](https://github.com/zhaoyang21cn/ILiveSDK_Android_Demos)

接口|所属类别|描述
:--|:--|:--:
init|ILVCallManager|初始化视频通话能力
addIncomingListener|ILVCallManager|添加来电回调(初始化后就可以设置)
addCallListener|ILVCallManager|添加通话回调
makeCall|ILVCallManager|发起视频(语音)呼叫
acceptCall|ILVCallManager|接听视频(语音)通话
rejectCall|ILVCallManager|拒接视频(语音通话)
initAvView|ILVCallManager|设置渲染控件(AVVideoView)
endCall|ILVCallManager|结束呼叫

## 快速接入
请移步[视频聊天快速接入](./doc/helloworld.md)

## 错误码
[CallSDK错误码](./doc/error.md)

## 日志分析
[主线日志分析](./doc/mainlog.md)

## 联系我们
[新需求](https://github.com/zhaoyang21cn/CallSDK_Android_Demo/issues/new)

[BUG反馈](https://github.com/zhaoyang21cn/CallSDK_Android_Demo/issues/new)
