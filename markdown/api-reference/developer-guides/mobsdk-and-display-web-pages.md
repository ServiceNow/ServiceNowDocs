---
title: Display web pages hosted on your ServiceNow instance
description: You can display web pages hosted within your ServiceNow instance in your native Android application.
locale: en-US
release: australia
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Mobile SDK Developer Guide - Android, Developer guides, API implementation and reference]
---

# Display web pages hosted on your ServiceNow instance

You can display web pages hosted within your ServiceNow instance in your native Android application.

The Mobile SDK provides seamless handling of the required authentication and session management, while the [NowWebSDK](../../../../../app-store/dev_portal/API_reference/MobileSDKAndroid/NowWebSDK/concept/NowWebSDKAndroidAPI.md#) API provides the functionality required to handle pages residing on your ServiceNow instance. These web pages have all the dynamic interactions that are possible on the ServiceNow platform.

To use these features, you must first create an instance of the NowWebService. To do this, you must call the [makeWebService\(\)](../../../../../app-store/dev_portal/API_reference/MobileSDKAndroid/NowWebSDK/concept/NowWebSDKAndroidAPI.md#) method and provide the URL to your ServiceNow instance and an already initialized `NowSDK`. In addition, you must have imported `NowWeb` within your application. You should hold a reference to the NowWebService for as long as you're using the `NowWeb` service.

The following shows an example of how to create a NowWebService object:

```
/**
 * Helper class used to handle different Now service instances.
 */
@Singleton
class SdkManager @Inject constructor() {

    private var nowWebService: NowWebService? = null

    /**
     * Create the NowWebService once in the lifetime of the application inside the Application class or
     * another manager class that will be injected into other classes via dagger/hilt.
     * NowWebService should be created after initializing the NowSDK
     */
    suspend fun getNowWebService(): NowWebService? {
        if (nowWebService != null) return nowWebService

        return NowWebSDK.makeWebService(URL("https://instance-name.service-now.com")).getOrThrow()
            .also { this.nowWebService = it }
    }
}
```

## Pre-load pages to improve NowWeb load time

You can pre-load pages with cacheable resources in the background to improve initial NowWeb load times. The following example shows how to use the webService.preloadWebCache\(\) function to pre-load the `mesp` page. This method takes a list of URIs to pre-fetch more pages.

```
suspend fun preloadNowWeb() {
  val webService = sdkmanager.getNowWebService()
  webService.preloadWebCache(listOf(URI("mesp")))
}
```

## Create views to display web content

After you've instantiated an instance of NowWebService, you can use it to launch an activity to display web pages hosted on your ServiceNow instance.

The following example shows how to launch a NowWeb activity:

```
//Activity that will start the NowWeb
class MainActivity : AppCompatActivity() {

  @Inject
  lateinit var sdkManager: SdkManager

  override fun onCreate(savedInstanceState: Bundle?) {
    super.onCreate(savedInstanceState)

    // Start NowWeb
    lifecycleScope.launch {
      sdkManager.getNowWebService()?.launch(this@MainActivity, URL("https://instance-name.service-now.com"), object : NowWebTheme{})
    }
  }
}
```

In this example, **url** is the URL of the initial page to load within the view. This URL must point to a page that is hosted on the specified ServiceNow instance.

## Color theme support for NowWeb UI elements

You can specify a custom color theme that applies to all UI elements within a view when calling the NowWebService launch\(\) method. To create this custom color theme, create a type that implements the NowWebTheme interface and pass it in the theme parameter of the NowWebService.launch\(\) call.

```
suspend fun launchNowWeb() {
    val webService = getNowWebService()

    val webTheme = object : NowWebTheme {
        override val brand: Int
            get() = Color.BLUE

        override val textPrimary: Int
            get() = Color.BLACK

        //Override remaining theme colors
    }
    webService?.launch(activity, URL("https://instance-name.service-now.com"), webTheme)
}
```

For additional information on applying color themes within a web view, see [Use NowUIColoring to theme NowWebTheme and NowChatTheme](mobsdk-and-color-theming.md).

