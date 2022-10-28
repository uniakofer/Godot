# Godot
1. Edit AndroidManifest.xml
** handle internete permission **
```
<manifest>

<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />

<meta-data
    tools:replace="android:value"
    android:name="com.google.android.gms.ads.APPLICATION_ID"
    android:value="ca-app-pub-1302743165084035~3896100795"/>
<meta-data
    android:name="com.google.android.gms.ads.DELAY_APP_MEASUREMENT_INIT"
    android:value="true"/>
```
2. Edit build.gradle
```
defaultConfig {
        multiDexEnabled = true
```
**if on Release**
```
            shrinkResources true
            minifyEnabled true
            proguardFiles getDefaultProguardFile('proguard-android.txt'), 'proguard-rules.pro'
```
