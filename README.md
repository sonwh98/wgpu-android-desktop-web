# android-wgpu
WebGPU example for Android that imply draws a triangle

Make sure to install anroid ndk side-by-side not the ndk-bundle. The ndk-bundle is legacy

#Dependencies
```bash
rustup target install armv7-linux-androideabi aarch64-linux-android i686-linux-android x86_64-linux-android
cargo install cargo-apk
export ANDROID_NDK_ROOT=/usr/local/android-sdk/ndk/25.2.9519653
```

#Build and run
```
cargo apk run
```

#Useful cmds
```bash
adb install target/debug/apk/hello_triangle.apk
adb shell pm list packages|grep triangle
adb shell cmd package uninstall -k world.datom.hello_triangle

emulator -list-avds
emulator -avd pixel6pro
```


