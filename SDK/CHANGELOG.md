# 1.2.0 (2023年2月)
版本新增以下功能：

- 支持引擎管理，可以同时创建多个发布或订阅
- 支持 Mute 本地或远端音视频流
- 支持推送外部源 YUV/H264/PCM 数据
- 支持订阅外部源 YUV/H264/PCM 数据回调
- 新增远端首帧、流状态、卡顿统计回调

# 1.0.0 (2022年8月)

版本首次发布，初始版本具有以下功能：

- 推流端支持摄像头和麦克风设备开关、支持摄像头前后置切换、支持扬声器和听筒切换
- 推流端支持视频分辨率、帧率设置
- 使用 whip 协议和 WebRTC SDK 实现开始/结束推流
- 使用 whcp 协议和 WebRTC SDK 实现开始/结束拉流
- 支持推流、拉流事件监听