##Release Note
 ###V1.0.4 (2016-12-28)
 - 扩展内部信令(兼容iOS多人)
 - 修改默认呼叫配置(创建讨论组，与iOS兼容)
 - 合并多人来电到普通来电,并扩展来电回调接口(onNewIncomingCall)
 - ILVBCallMemberListener中添加onMemberEvent上抛用户进出房间事件
 - 所有信令通过ILVCallNotification上抛
 
###V1.0.3 (2016-12-07)
- 添加事件上报
- 添加[关键日志](./mainlog.md)输出
 
###V1.0.2 (2016-12-05)
- 修复imsupport为true时信令异常
- 修复未加入房间时收到信令的处理

###V1.0.1 (2016-12-02)
- 给多人添加inviteUser接口
- 更新默认心跳间隔为10s
- 修复多人通话不结束问题

###V1.0.0 (2016-11-23)
- 发布基础版本
