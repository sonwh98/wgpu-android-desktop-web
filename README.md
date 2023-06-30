# wgpu-android-desktop-web
Drawing a triangle using low level graphics library like WebGPU is surprisingly difficulty. 
This is an example of how to get started on WebGPU for Android/Desktop/Web so you can quickly bootstrap
your own project.

Make sure to install anroid ndk side-by-side not the ndk-bundle. The ndk-bundle is legacy

# Dependencies
```bash
rustup target install armv7-linux-androideabi aarch64-linux-android i686-linux-android x86_64-linux-android
cargo install cargo-apk
export ANDROID_NDK_ROOT=/usr/local/android-sdk/ndk/25.2.9519653
```

# Build and run
```
cargo apk build --target=aarch64-linux-android
cargo build --target=wasm32-unknown-unknown
cargo apk run

wasm-pack build --target web

```

# Useful cmds
```bash
adb devices
adb install target/debug/apk/hello_triangle.apk
adb shell pm list packages|grep triangle
adb shell cmd package uninstall -k world.datom.hello_triangle
adb shell monkey -p world.datom.hello_triangle -c android.intent.category.LAUNCHER 1
adb logcat *:E

emulator -list-avds
emulator -avd pixel6pro

rustup target list --installed
python3 -m http.server
```
