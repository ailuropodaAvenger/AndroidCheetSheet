
```java
shareButton.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                nativeFilterShare();
            }
});


private void nativeShare() {

        Intent i = new Intent(android.content.Intent.ACTION_SEND);
        i.setType("text/plain");
        i.putExtra(android.content.Intent.EXTRA_TEXT, link);
        startActivity(Intent.createChooser(i, "Share via"));
    }


private void nativeFilterShare() {

        List<Intent> targetShareIntents = new ArrayList<Intent>();
        Intent shareIntent = new Intent();
        shareIntent.setAction(Intent.ACTION_SEND);
        shareIntent.setType("text/plain");

        List<ResolveInfo> resInfos = this.getPackageManager().queryIntentActivities(shareIntent, 0);

        if (!resInfos.isEmpty()) {

            for (ResolveInfo resInfo : resInfos) {
                String packageName = resInfo.activityInfo.packageName;

                if (packageName.contains("com.twitter.android") || packageName.contains("com.facebook.katana") || packageName.contains("com.google.android.apps.plus")) {
                
                    Intent intent = new Intent();
                    intent.setComponent(new ComponentName(packageName, resInfo.activityInfo.name));
                    intent.setAction(Intent.ACTION_SEND);
                    intent.setType("text/plain");
                    intent.putExtra(Intent.EXTRA_TEXT, link);
                    intent.setPackage(packageName);
                    targetShareIntents.add(intent);
                                     }
                         }
            if (!targetShareIntents.isEmpty()) {

                Intent chooserIntent = Intent.createChooser(targetShareIntents.remove(0), "Share via");
                chooserIntent.putExtra(Intent.EXTRA_INITIAL_INTENTS, targetShareIntents.toArray(new Parcelable[]{}));
                startActivity(chooserIntent);
                         } 
                         else {
                                    new AlertDialog.Builder(this)
                                    .setTitle("Sorry, No sharing app is installed !")
                                    .setMessage("                            ")
                                    .show();
                                    }
                        }

            }
```
