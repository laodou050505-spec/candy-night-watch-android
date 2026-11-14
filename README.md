# 万圣守糖夜 — Android Gradle 工程（Unity 导出）

本仓库是 Unity 工程用 Export Project 在本地导出的 Android Gradle 工程，供云端打包使用。
Unity 源码工程在 [candy-night-watch](https://github.com/laodou050505-spec/candy-night-watch)，本工程由其提交 `43a0071d35d2cb4388a986299b118199768150c9` 导出。

- Unity 6000.5.5f1，脚本后端 IL2CPP
- IL2CPP 已预编译：libil2cpp.so 在 unityLibrary/src/main/jniLibs/arm64-v8a，工程中已不含 Il2CppOutputProject，打包时不编译 IL2CPP
- 目标架构只有 arm64-v8a，不导出调试符号（debugSymbolLevel none）
- compileSdk / targetSdk 36，minSdk 29
- 包名 `com.toybox.trickorfreeze`，版本 1.0.9

构建：`gradle assembleRelease`，产物在 `launcher/build/outputs/apk/release/`。
`local.properties` 未提交，请按构建环境设置 Android SDK 路径。
