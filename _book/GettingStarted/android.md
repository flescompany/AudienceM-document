---
description: how to apply on android
---


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
  implementation 'com.github.flescompany:AudienceM-SDK-Library:0.0.04'
}
```


# import

```java
import com.oneclick.audiencem_sdk_library.AudienceMSDK;
```

# usage

```java
AudienceMSDK AMSdk = new AudienceMSDK(Context,"appKey"); // 객체 선언

AMSdk.AMInit("event", JSONObject); // 앱 실행 시 AMTrack() 호출전에 가장 먼저 호출되어야 하는 함수 (단 한번만 호출되어야 함. 두번 호출 시 에러)

AMSdk.AMTrack("event", JSONObject); 
AMSdk.AMTrack("event", JSONObject);
```