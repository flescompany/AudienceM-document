---
description: how to apply on android
---

SDK 작업중

# dependency

**gradle.build**

```
allprojects {
  repositories {
    ...
    maven { url 'https://gitpack.io'}
  }
}
```

```
dependencies {
  implementation 'com.github.flescompany:AudienceM-SDK-Library:0.0.02'
}
```


# import

```java
import com.oneclick.audiencem_sdk_library.ToastClass;
```

# usage

```java
ToastClass.Companion.showToast(this,"하이루 뭐야 왜 안떠");
```