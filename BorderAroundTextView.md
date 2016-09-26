```java
//Create tvborder.xml in drawable folder

  <shape xmlns:android="http://schemas.android.com/apk/res/android" android:shape="rectangle" >
      <solid android:color="#d7100f0f" />
      <stroke android:width="1dip"
          android:color="#fcfcfc"/>
      <corners android:radius="3dp" />
  </shape>

//in textview
     <TextView
          android:id="@+id/videoDuration"
          android:layout_width="wrap_content"
          android:layout_height="wrap_content"
          android:background="@drawable/tvborder"
          android:padding="5dp"
          android:text="40:00"
          android:layout_gravity="center_vertical"
          android:textColor="@color/white"
          android:textSize="@dimen/large_card_videoduration_text_size"/>
```
