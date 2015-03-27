# Android-ScreenSlidePager
Full screen slide pager to display images fetched from Internet by Picasso

## demo

![](https://raw.githubusercontent.com/LyndonChin/Android-ScreenSlidePager/master/screenslidepager.gif)

The indicator below ScreenSlidePager has been extracted as a separate single aar.
So it can be used independently as following.

### Gradle

```groovy
compile 'com.liangfeizc:SlidePageIndicator:1.0.0@aar'
```

### Maven

```xml
<dependency>
    <groupId>com.liangfeizc</groupId>
    <artifactId>SlidePageIndicator</artifactId>
    <version>1.0.0</version>
    <type>aar</type>
</dependency>
```

## how to use

```CirclePageIndicator``` and ```ViewPager``` shoud be used as child views of a ```Framelayout```. But here we used ```merge``` instead, because the root view in any activity is a ```FrameLayout```.

You can use `android:gravity` to position the `CirclePageIndicator` and use `app:indicator_spacing` to adjust the spacing between two adjencent circle indicators.

    ```xml
    <merge xmlns:android="http://schemas.android.com/apk/res/android"
        xmlns:app="http://schemas.android.com/apk/res-auto">
        <android.support.v4.view.ViewPager
            android:id="@+id/pager"
            android:layout_width="match_parent"
            android:layout_height="match_parent" />
        <com.liangfeizc.slidepageindicator.CirclePageIndicator
            android:id="@+id/indicator"
            android:gravity="bottom|center_horizontal"
            app:indicator_spacing="5dp"
            android:layout_marginBottom="20dp"
            android:layout_marginStart="20dp"
            android:layout_marginLeft="20dp"
            android:layout_width="match_parent"
            android:layout_height="match_parent" />
    </merge>
    ```

## dependencies

* Picasso
