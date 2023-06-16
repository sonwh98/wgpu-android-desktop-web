# android-wgpu

adb install target/debug/apk/hello_triangle.apk
adb shell pm list packages|grep triangle
adb shell cmd package uninstall -k world.datom.hello_triangle


cargo apk run
