## 主线日志分析

### 过滤日志
在callsdk 1.0.3以后的版本中，可通过关键字*Key_Procedure*自己过滤日志进行简单分析及问题定位


### 发起方日志

```C
// ILiveSDK初始化日志
I/ILiveSDK: Key_Procedure|initSdk->init appid:1400013700, accountType:7285
// CallSDK初始化日志
V/ILVB-CallMgr: Key_Procedure|init entered
// 登录日志
I/ILVBLogin: Key_Procedure|ILVB-iLiveLogin strart |id:xiao
I/ILVBLogin: Key_Procedure|ILVB-iLiveLogin|login success
// 发起呼叫日志
D/ILVB-CallMgr: Key_Procedure|VideoCall|makeCall to:green, type:2
I/ILVBRoom: Key_Procedure|ILVB-Room|start create room:1575029805 enter with im:true|video:true
// 初始化渲染控件日志
I/ILVBRoom: Key_Procedure|ILVB-Room|init root view
I/AVVideoGroup: Key_Procedure|ILVB-AVVideoGroup|init sub views
I/ILVBRoom: Key_Procedure|ILVB-Room|strart enableCamera
I/ILVBRoom: Key_Procedure|createRoom->im room ok:1575029805
I/ILVBRoom: Key_Procedure|onNewMessage->size:1
W/ILVBRoom: Key_Procedure|ILVB-Room|enter av room complete result: 0
D/ILVB-CallMgr: Key_Procedure|VideoCall|createRoom success:1575029805
I/ILVBRoom: Key_Procedure|sendC2CMessage->id:green
I/ILVBRoom: Key_Procedure|ILVB-Room|onSurfaceCreated
I/ILVBRoom: Key_Procedure|ILVB-Room|strart enableCamera
I/AVRootView: Key_Procedure|ILVB-AVRootView|renderVideoView->enter index:0|0,0,1080,1865
I/ILVBRoom: Key_Procedure|ILVB-Room|onEndpointsUpdateInfo myself id has camera xiao
I/AVRootView: Key_Procedure|ILVB-AVRootView|renderVideoView->enter index:0|0,0,1080,1865
I/ILVBRoom: Key_Procedure|ILVB-Room|enable camera id:0/true
I/ILVBRoom: Key_Procedure|ILVB-Endpoint | requestRemoteVideo id [green]  
I/AVRootView: Key_Procedure|ILVB-AVRootView|renderVideoView->enter index:1|50,50,270,466
I/ILVBRoom: Key_Procedure|onNewMessage->size:1
// 被叫接听日志
V/ILVB-CallMgr: Key_Procedure|CallMgr->Accept by green
I/ILVBRoom: Key_Procedure|onNewMessage->size:1
I/ILVBRoom: Key_Procedure|sendGroupOnlineMessage->id:1575029805
I/ILVBRoom: Key_Procedure|onNewMessage->size:1
I/ILVBRoom: Key_Procedure|sendGroupOnlineMessage->id:1575029805
I/ILVBRoom: Key_Procedure|ILVB-Room|onEndpointsUpdateInfo no camera id green
I/ILVBRoom: Key_Procedure|onNewMessage->size:1
// 被叫挂断日志
V/ILVB-CallMgr: Key_Procedure|CallMgr->Hangup by green
// 结束通话日志
D/ILVB-CallMgr: Key_Procedure|ILVB-Call|endCallEx enter:1575029805, 4, Remote cancel
I/ILVBRoom: Key_Procedure|ILVB-Room|exit avroom  Complete
I/ILVBRoom: Key_Procedure|onNewMessage->size:1
```

### 接收方日志
```C
// ILiveSDK初始化日志
I/ILiveSDK: Key_Procedure|initSdk->init appid:1400013700, accountType:7285
// CallSDK初始化日志
V/ILVB-CallMgr: Key_Procedure|init entered
// 登录日志
I/ILVBLogin: Key_Procedure|ILVB-iLiveLogin strart |id:xiao
I/ILVBLogin: Key_Procedure|ILVB-iLiveLogin|login success
I/ILVBRoom: Key_Procedure|onNewMessage->size:1
// 收到来电日志
V/ILVB-CallMgr: Key_Procedure|ILVB-Call|processIncoming->new call from:green|1575038522
// 接听来电日志
D/ILVB-CallMgr: Key_Procedure|VideoCall|acceptCall enter:1575038522
I/ILVBRoom: Key_Procedure|joinRoom->id: 1575038522 isIMsupport: true
// 初始化渲染控件日志
I/ILVBRoom: Key_Procedure|ILVB-Room|init root view
I/AVVideoGroup: Key_Procedure|ILVB-AVVideoGroup|init sub views
I/ILVBRoom: Key_Procedure|ILVB-Room|strart enableCamera
I/ILVBRoom: Key_Procedure|joinLiveRoom joinIMChatRoom callback succ 
I/ILVBRoom: Key_Procedure|onNewMessage->size:1
W/ILVBRoom: Key_Procedure|ILVB-Room|enter av room complete result: 0
D/ILVB-CallMgr: Key_Procedure|VideoCall|joinRoom success:1575038522
I/ILVBRoom: Key_Procedure|sendC2COnlineMessage->id:green
I/ILVBRoom: Key_Procedure|ILVB-Room|onSurfaceCreated
I/ILVBRoom: Key_Procedure|ILVB-Room|strart enableCamera
I/AVRootView: Key_Procedure|ILVB-AVRootView|renderVideoView->enter index:0|0,0,1080,1865
I/ILVBRoom: Key_Procedure|ILVB-Room|onEndpointsUpdateInfo myself id has camera xiao
I/AVRootView: Key_Procedure|ILVB-AVRootView|renderVideoView->enter index:0|0,0,1080,1865
I/ILVBRoom: Key_Procedure|ILVB-Endpoint | requestRemoteVideo id [green]  
I/AVRootView: Key_Procedure|ILVB-AVRootView|renderVideoView->enter index:1|50,50,270,466
I/ILVBRoom: Key_Procedure|ILVB-Room|enable camera id:0/true
I/ILVBRoom: Key_Procedure|onNewMessage->size:1
// 远程挂断日志
V/ILVB-CallMgr: Key_Procedure|CallMgr->Hangup by green
// 结束通话日志
D/ILVB-CallMgr: Key_Procedure|ILVB-Call|endCallEx enter:1575038522, 4, Remote cancel
I/ILVBRoom: Key_Procedure|ILVB-Room|exit avroom  Complete
I/ILVBRoom: Key_Procedure|onNewMessage->size:1
```
