
```java
//From fragments
  Intent i = new Intent(getActivity(), NewsviewActivity.class);
  
  i.putExtra("Url", contents.get(position).getUrl())
   .putExtra("siteName", contents.get(position).getSiteName())
   .putExtra("imageUrl", contents.get(position).getImage())
   .putExtra("tag", DEATIL_NEWS_TAG);

  getActivity().startActivity(i);


//in Activity
  public String Image, getUrl, Sitename, DEATIL_NEWS_TAG;

  Intent intent = getIntent();
  
  getUrl = intent.getExtras().getString("Url");
  Sitename = intent.getExtras().getString("siteName");
  Image = intent.getExtras().getString("imageUrl");
  DEATIL_NEWS_TAG = intent.getExtras().getString("tag");

```
