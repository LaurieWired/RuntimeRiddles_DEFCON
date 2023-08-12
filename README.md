
![runtimeriddles](https://github.com/LaurieWired/RuntimeRiddles_DEFCON/assets/123765654/1de6a537-14c0-4582-ad96-9351df205f4f)

# Runtime Riddles: Abusing Manipulation Points in the Android Source

During this talk, I demonstrate how to manipulate the Android 13 Runtime to replace methods with custom code. Static methods inside the application or even inside the Android framework can be replaced with custom behavior during app execution. I also release ARTful, a new open source tool for the community.

## ARTful
[ARTful](https://github.com/LaurieWired/artful) is a native Android library the allows developers to modify the Android Runtime (ART) on Android 13 + 14. With this tool, you can dynamically change the implementation of any static method within your application or the Android Framework to affect methods called from within your application. This eliminates the requirement of using plaintext references to Android ClassLoaders to execute unexpected code and thwarts Reverse Engineering by entirely removing method cross-references.

## Link References

### Java Native Interface (JNI)
- [JNI Functions](https://docs.oracle.com/javase/7/docs/technotes/guides/jni/spec/functions.html)
- [JNI Types and Signatures](https://docs.oracle.com/javase/8/docs/technotes/guides/jni/spec/types.html#type_signatures)

### Android Source Code
- DexFile.java
  - https://cs.android.com/android/platform/superproject/+/master:libcore/dalvik/src/main/java/dalvik/system/DexFile.java
- art_method.h
  - https://cs.android.com/android/platform/superproject/+/master:art/runtime/art_method.h;drc=c9af14e93f6a2691bf8231752d8d7c3e41b14c76;l=18
- Executable.java
  - https://cs.android.com/android/platform/superproject/+/master:libcore/ojluni/src/main/java/java/lang/reflect/Executable.java
