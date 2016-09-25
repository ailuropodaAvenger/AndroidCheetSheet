```java
import android.os.Build;

String userDeviceInfo ;

userDeviceInfo = deviceData() + androidID();

String androidID(){
        String androidID = Settings.Secure.getString(this.getContentResolver(), Settings.Secure.ANDROID_ID);
        
        System.out.println(androidID);

        return  androidID ;
    }

    String deviceData(){
        String  details =  "VERSION.RELEASE : "+ Build.VERSION.RELEASE
                            +"\nVERSION.INCREMENTAL : "+ Build.VERSION.INCREMENTAL
                            +"\nVERSION.SDK.NUMBER : "+Build.VERSION.SDK_INT
                            +"\nBOARD : "+Build.BOARD
                            +"\nBOOTLOADER : "+Build.BOOTLOADER
                            +"\nBRAND : "+Build.BRAND
                            +"\nCPU_ABI : "+Build.CPU_ABI
                            +"\nCPU_ABI2 : "+Build.CPU_ABI2
                            +"\nDISPLAY : "+Build.DISPLAY
                            +"\nFINGERPRINT : "+Build.FINGERPRINT
                            +"\nHARDWARE : "+Build.HARDWARE
                            +"\nHOST : "+Build.HOST
                            +"\nID : "+Build.ID
                            +"\nMANUFACTURER : "+Build.MANUFACTURER
                            +"\nMODEL : "+Build.MODEL
                            +"\nPRODUCT : "+Build.PRODUCT
                            +"\nSERIAL : "+Build.SERIAL
                            +"\nTAGS : "+Build.TAGS
                            +"\nTIME : "+Build.TIME
                            +"\nTYPE : "+Build.TYPE
                            +"\nUNKNOWN : "+Build.UNKNOWN
                            +"\nUSER : "+Build.USER;

        System.out.println("User detail --- " + details);

        return details ;
    }
```
