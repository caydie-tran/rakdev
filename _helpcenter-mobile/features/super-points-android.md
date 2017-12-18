---
title: Rakuten Super Points SDK - Android Integration
layout: helpcenter-mobile
parent: _helpcenter-mobile/features.md
categories: [Ecosystem, Analytics, Mobile, Android, iOS, rakuten super points, super points, points]
weight: 12
---

The Android Points Module provides a UI for querying point and member status information for users logged in with their Rakuten ID.

## Points UI

The points module includes standard UI to show point information for both japan and global users. 
![Japan Points Screen](../images/img_super_points_jp_ui_screen.png) 
![Global Points Screen](../images/img_super_points_global_ui_screen.png)

## Requirements

#### Supported Android Version

Android SDK 15 (4.0.3) - SDK 23 (6.0)

#### Required Android Permissions

    <uses-permission android:name="android.permission.INTERNET"/>

#### Required RAE token scope

*   memberinfo_read_name
*   memberinfo_read_point
*   memberinfo_read_rank
*   gecp_point_read (only for Global Ichiba Points)

## Setup

#### #1 Add dependency to buildscript

Download dependency from Artifactory. If you do not already have Artifactory set up in your Android Studio, click [here](http://www.raksdtd.com/android/installing-sdk/) to set it up.

```java
        repositories {
            maven {
                url 'http://artifactory.raksdtd.com/artifactory/libs-release'
            }
        }

        dependency {
            compile 'jp.co.rakuten.sdtd:points:2.0.0'
        }
```
#### #2 Initialize module in the application startup routine

In your application's startup routine:

```java
    public class AppSubClass extends Application {
        @Override
        public void onCreate() {
            super.onCreate();

            // initialize Points Manager
            PointsManager.INSTANCE.initialize(this, null);
        }
    }
```

Add the subclass in `AndroidManifest.xml`.

```
    <application android:name=".AppSubClass">
    ...
    </application>
```

#### #3 Display points screen

You can simply use the provided points UI fragment as follows.

```java
    public class PointsActivity extends AppCompatActivity {

        @Override
        public void onCreate() {
            super.onCreate();

             FragmentManager fm = getSupportFragmentManager();
             if(fm.findFragmentByTag("points") == null) {
                  Fragment fragment = PointsManager.INSTANCE.newPointFragment(accessToken, PointsManager.MALL_JAPAN);
                  fm.beginTransaction()
                          .add(R.id.fragment_holder, fragment, "points")
                          .commit();
              }
        }
    }
```

The RAE access token can be obtained using [RAE Engine Client](http://www.raksdtd.com/android-sdk/api-rae-engine-latest/) or [User Module](http://www.raksdtd.com/android-sdk/user-latest/)

## Documentation

Our Javadoc can be found at [http://www.raksdtd.com/android-sdk/points-latest/](http://www.raksdtd.com/android-sdk/points-latest/)

## Changelog

### 2.0.0

*   Remove Rakuten API (REM-7159)
*   Minimum Android SDK 15
*   Fix: Unclear error in case SDK not initialized (REM-8440)
*   Simplify TestUI Sample
*   Major refactoring of PointsManager API

### 1.7.4:

*   Minor bug fixes and stability improvements
*   Migrate to artifactory at artifactory.raksdtd.com (REM-3970)

## Additional Resources

**Rakuten Ecosystem Mobile SDK Roadmap**: [Roadmap for Rakuten Ecosystem Mobile SDK ](https://confluence.rakuten-it.com/confluence/display/SSEDPT/REM+-+Roadmap+2017) 

**SDK Reference Documentation**: 
* Android: [http://raksdtd.com/android-sdk/](http://raksdtd.com/android-sdk/) 
* iOS: [http://www.raksdtd.com/ios-sdk/](http://www.raksdtd.com/ios-sdk/) 

**Super Point SDK integration Tutorials**
* [Android tutorial](../13_super_points_android_integration)
* [iOS tutorial](../14_super_points_ios_integration)

