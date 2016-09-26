```java

// XML Structure
    <FrameLayout
        xmlns:android="http://schemas.android.com/apk/res/android"
        android:id="@+id/mainlayout"
        android:layout_width="fill_parent"
        android:layout_height="fill_parent"
        android:foregroundGravity="bottom"
        android:orientation="vertical" >

        <Imageview
            android:id="@+id/thumbnailImage"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"/>

        <LinearLayout
            android:layout_width="fill_parent"
            android:layout_height="wrap_content"
            android:layout_gravity="bottom"
            android:background="@drawable/gradient"
            android:orientation="horizontal"
            android:paddingRight="10dp"
            android:paddingLeft="10dp"
            android:paddingBottom="10dp"
            android:weightSum="1">

            <TextView
                android:id="@+id/videoTitle"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:paddingTop="@dimen/small_card_title_padding_top"
                android:text="Valobasar Pongktimala (ভালবাসার পংক্তিমাল)"
                android:textColor="@color/white"
                android:textSize="@dimen/small_card_title_text_size"
                android:layout_weight="0.85" />

        </LinearLayout>
    </FrameLayout>
    
// create gradient xml in drawable folder

    <shape xmlns:android="http://schemas.android.com/apk/res/android"
        android:shape="rectangle" >
        <gradient
            android:angle="90"
            android:endColor="#2c333131"
            android:startColor="@color/black_semi_transparent"/>
        <corners android:radius="0dp" />
    </shape>

//Or 
        <shape xmlns:android="http://schemas.android.com/apk/res/android"
            android:shape="rectangle" >

            <gradient
                android:startColor="#13000000"
                android:centerColor="#a6000000"
                android:endColor="#FF000000"
                android:angle="270"
                android:dither="true" />

            <corners android:radius="0dp" />
        </shape>
```
