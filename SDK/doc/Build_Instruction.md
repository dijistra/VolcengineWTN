# 编译客户端 SDK

你可以参考此项目，自行搭建通过 WTN 推拉流的客户端 SDK。也可以直接使用此 SDK，在客户端上接入 WTN 实现推拉流。
参考本文，编译客户端 SDK。

## 前提条件
编译 WTN SDK for Android 时，必须已安装 Android Studio。

## 编译步骤
### 步骤一: 在客户端 SDK 项目中添加 WebRTC 静态库
1. 获取 WebRTC 静态库，包括为 Android 和 iOS 分别编译的，针对 arm64 架构和 amrv7 架构的 SDK。参考 [编译 WebRTC 静态库](Build_webrtc.md)。
2. 将 WebRTC 静态库相关文件加入客户端 SDK 项目中：
     1. 将 WebRTC 静态库中的头文件拷贝到：`./third_party/webrtc/headers/`;
     2. 拷贝 iOS 静态库到：`./third_party/webrtc/ios/libwebrtc.a`；
     3. 拷贝 Android 静态库和 Jar 包到以下位置：
          - `./third_party/webrtc/android/armeabi-v7a/libwebrtc.a`
          - `./third_party/webrtc/android/arm64-v8a/libwebrtc.a`
          - `./third_party/webrtc/android/jar/libwebrtc.jar`

### 步骤二：编译 WTN SDK
#### 编译 WTN SDK for Android
使用 Android Studio，打开 `./sdk/android`。

#### 编译 WTN SDK for iOS
在根目录下执行：`cmake -GXcode -DRTC_PLATFORM=ios -Bbuild_ios`。

## 目录结构
项目的目录结构如下：
```
├── cmake
│   └── toolchains
├── doc
├── sdk
|   └── src
│       ├── android
│       └── ios
└── third_party
    ├── boost_1_69_0
    └── webrtc
        ├── android
        ├── headers
        └── ios
```
