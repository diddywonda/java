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

  }
}
