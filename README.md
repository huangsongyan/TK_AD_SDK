### 天空广告SDK集成文档

请在应用中嵌入以下追踪代码，每个应用具有唯一Appkey，该应用的Appkey为

`53f417b2fd98c5ff28024176`

1. 设置Appkey
    
    在AndroidManifest.xml文件application标签下添加

```xml
    <meta-data
        android:name="TK_APPKEY"
        android:value="你的appkey"/>        
```

   或者在java中设置appkey，需要在SDK.init()之后调用。

```java
     ADSDK.setAppKey("你的appkey");
```

2. AndroidManifest.xml，添加权限

```xml
    <uses-permission android:name="android.permission.INTERNET" />
    <uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
    <uses-permission android:name="android.permission.ACCESS_WIFI_STATE" />
    <uses-permission android:name="android.permission.READ_PHONE_STATE" />
    <uses-permission android:name="android.permission.CHANGE_WIFI_STATE"/>
    <uses-permission android:name="android.permission.LOCAL_MAC_ADDRESS"/>
```

3. 在应用程序的 Application类的onCreate方法中初始化SDK,并发送广告追踪。

```java
    ADSDK.init(this);
    ADSDK.sendAdTrack();
```







