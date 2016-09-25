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
```
