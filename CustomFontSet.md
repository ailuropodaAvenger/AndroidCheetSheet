create new folder in ProjectFolder/app/src assets -> fonts -> add .otf /.ttf format fonts

most used fonts -> Myrid pro, Myrid pro semi bold , nato, roboto

<h3> Code</h3>

```java
Typeface font, fontBold; 
TextView viewCount ;

font = Typeface.createFromAsset(activity.getAssets(), "fonts/Myriad Pro Regular.ttf");
fontBold = Typeface.createFromAsset(activity.getAssets(), "fonts/Myriad Pro Semibold.ttf");

viewCount.setTypeface(font); 
viewCount.setText("400 views");


//Cutom font setting in Toolbar

//in XML
<android.support.v7.widget.Toolbar
        xmlns:android="http://schemas.android.com/apk/res/android"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:background="@color/white"
        android:id="@+id/toolbar"
        android:theme="@style/ThemeOverlay.AppCompat.Dark.ActionBar"
        app:title="3rdBell"
        app:titleTextColor="@color/thirdbell"/>

//in styles.xml value file

<style name="MyCustomTabLayout" parent="Widget.Design.TabLayout">
        <item name="tabTextAppearance">@style/MyCustomTextAppearance</item>
</style>

<style name="MyCustomTextAppearance" parent="TextAppearance.Design.Tab">
  <item name="textAllCaps">false</item>
</style>

//in java file
android.support.v7.widget.Toolbar toolbar;

toolbar = (android.support.v7.widget.Toolbar) findViewById(R.id.toolbar);
setSupportActionBar(toolbar);
toolbar.setLogo(R.mipmap.tab_icon_bell);
for(int i = 0; i < toolbar.getChildCount(); i++)
{ 
    View view = toolbar.getChildAt(i);
    
    if(view instanceof TextView) {
        TextView textView = (TextView) view;

        Typeface myCustomFont=Typeface.createFromAsset(getAssets(),"fonts/ANDROID ROBOT.ttf");
        textView.setTypeface(myCustomFont); }
  }

```
