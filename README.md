# java
admob
/** The Application class that manages AppOpenManager. */
public class MyApplication extends Application {

  private static AppOpenManager appOpenManager;

  @Override
  public void onCreate() {
    super.onCreate();
    MobileAds.initialize(
        this,
        new OnInitializationCompleteListener() {
          @Override
          public void onInitializationComplete(InitializationStatus initializationStatus) {}
        });

    appOpenManager = new AppOpenManager(this);

  }<manifest>
    <application>
        <!-- Sample AdMob app ID: ca-app-pub-3940256099942544~3347511713 -->
        <meta-data
            android:name="com.google.android.gms.ads.APPLICATION_ID"
            android:value="ca-app-pub-xxxxxxxxxxxxxxxx~yyyyyyyyyy"/>
    </application>
</manifest>
}
