---
description: how to apply on android
---

# dependency

```build.gradle```

```
	allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
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