---
title: NowWebService class - Android
description: The NowWebService class provides a function that launches a NowWebActivity that hosts a web view.Creates a NowWebActivity that hosts the web view.Preloads a list of specified java.net.URIs in a headless webview to pre-populate the webview cache with cacheable resources on the page.Updates the NowWeb UI theme with the specified UI theme. Use this function to update the web UI theme after it has been initially set using the launch\(\) function, such as when changing the theme from light to dark.
locale: en-US
release: australia
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Mobile SDK - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowWebService class- Android

The NowWebService class provides a function that launches a NowWebActivity that hosts a web view.

|Name|Type|Description|
|----|----|-----------|
|configuration|[NowServiceConfiguration class - Android](../../NowServiceConfiguration/concept/NowServiceConfigurationAndroidAPI.md)|Configuration information for the associated service, such as the ServiceNow instance URL and the name of the package.|

**Parent Topic:**[Mobile SDK - Android](../../concept/MobileSDKAndroidAPI.md)

## NowWebService - launch\(context: Context, url: URL, nowWebTheme: NowWebTheme\)

Creates a NowWebActivity that hosts the web view.

<table id="table_j1k_sbf_qqb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

context

</td><td>

Context

</td><td>

Context to use for launching the associated activity.

</td></tr><tr><td>

url

</td><td>

URL

</td><td>

URL of the web page to load. This web page must be on the target ServiceNow instance that the service was initialized with.

</td></tr><tr><td>

nowWebTheme

</td><td id="Web-themeColors-entry">

[NowWebTheme](../../NowWebTheme/concept/NowWebThemeAndroidInterface.md)

</td><td>

Optional. NowWebTheme object to apply to the UI elements of the view controller.Default: Default theme

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function.

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

## NowWebService – preloadWebCache\(preloadUris: List&lt;URI&gt;\)

Preloads a list of specified java.net.URIs in a headless webview to pre-populate the webview cache with cacheable resources on the page.

**Note:** Completion of this function call is based on onPageFinished\(\) being called in the webview, which does not take into account redirections or resources on the page. Because of this, preload may not be fully complete when this method returns.

|Name|Type|Description|
|----|----|-----------|
|preloadUris|List|List of java.net.URIs to pre-load. All java.net.URIs must be relative or match the current host configured in the NowSDK.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to use the webService.preloadWebCache\(\) function to pre-load the `mesp` page.

```
suspend fun preloadNowWeb() {
  val webService = serviceProvider.webService()
  webService.preloadWebCache(
    listOf(
      URI("mesp")
    )
  )
}
```

## NowWebService – updateTheme\(nowWebTheme: NowWebTheme\)

Updates the NowWeb UI theme with the specified UI theme. Use this function to update the web UI theme after it has been initially set using the launch\(\) function, such as when changing the theme from light to dark.

|Name|Type|Description|
|----|----|-----------|
|nowWebTheme|[NowWebTheme](../../NowWebTheme/concept/NowWebThemeAndroidInterface.md)|NowWebTheme object to apply to the UI elements of the view controller.|

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to update a light UI theme implemented using the launch\(\) function to the dark UI theme using the updateTheme\(\) function.

```
val webService = getNowWebService()

val lightTheme = object : NowWebTheme {
    override val brand: Int
        get() = Color.BLUE

    override val textPrimary: Int
        get() = Color.BLACK

    override val backgroundPrimary: Int
        get() = Color.WHITE

    // Override remaining theme colors
}

val darkTheme = object : NowWebTheme {
    override val brand: Int
        get() = Color.BLUE

    override val textPrimary: Int
        get() = Color.WHITE

    override val backgroundPrimary: Int
        get() = Color.BLACK

    // Override remaining theme colors
}

//launch NowWeb with light theme
webService?.launch(activity, URL("https://instance-name.service-now.com"), lightTheme)

//update NowWeb with dark theme
webService?.updateTheme(darkTheme)
```

