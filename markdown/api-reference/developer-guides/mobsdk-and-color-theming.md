---
title: Use NowUIColoring to theme NowWebTheme and NowChatTheme
description: The NowUIColoring interface contains all the colors used by all NowSDK modules.
locale: en-US
release: xanadu
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Mobile SDK Developer Guide - Android, Developer guides, API implementation and reference]
---

# Use NowUIColoring to theme NowWebTheme and NowChatTheme

The NowUIColoring interface contains all the colors used by all NowSDK modules.

For scenarios where you use similar color variables across multiple SDK modules, you can implement the NowUIColoring interface. Using this interface you can override color values and then use that implementation to override the nowUIColoring values inside the theme classes [NowWebTheme](../../../../../app-store/dev_portal/API_reference/MobileSDKAndroid/NowWebTheme/concept/NowWebThemeAndroidInterface.md) and [NowChatTheme](../../../../../app-store/dev_portal/API_reference/MobileSDKAndroid/NowChatTheme/concept/NowChatThemeColorsAndroidInterface.md). If color variables aren’t overridden, the NowUIColoring interface uses the default colors.

The following code example shows how to override colors for both a web UI and a chat UI.

```
// Implement the NowUIColoring and override desired color variables
val nowUIColoringImpl = object : NowUIColoring {
    override val brand: Int
        get() = Color.BLUE

    override val textPrimary: Int
        get() = Color.WHITE

    //override the rest of color variables

}

// Override the nowUIColoring for NowWeb value using the NowUIColoring implementation
lifecycleScope.launch {
    sdkManager.getNowWebService()?.launch(activity, URL("https://instance-name.service-now.com"), object : NowWebTheme {
        override val nowUIColoring: NowUIColoring
            get() = nowUIColoringImpl
    })
}

//Override the nowUIColoring for NowChat value using the NowUIColoring implementation
lifecycleScope.launch {
    sdkManager.getNowChatService()?.start(activity, object : NowChatTheme {
        override val nowUIColoring: NowUIColoring
            get() = nowUIColoringImpl
    })
}
```

## Dark theme support

To support a dark theme in NowChat, you can either provide your own dark theme implementation of the NowChatTheme and use that in the NowChatService.start\(\) and NowChatService.updateTheme\(\) functions. Or you can use a NowChatThemeDark class that implements the NowChatTheme interface with default dark theme colors. You can also use this class as a base for your custom dark theme implementation.

```
val chatService = serviceManager.getNowChatService()

val chatThemeLight = object : NowChatTheme {
    override val backgroundPrimary: Int
        get() = Color.WHITE

    override val textPrimary: Int
        get() = Color.BLACK

    // Override remaining theme colors
}

//create dark theme using the NowChatThemeDark class
val chatThemeDark = object : NowChatThemeDark(){
    override val backgroundPrimary: Int
        get() = Color.BLACK

    override val textPrimary: Int
        get() = Color.WHITE

    // Override remaining theme colors
}

//start NowChat with light theme
chatService?.start(activity, chatThemeLight)


//update NowChat theme to dark theme
chatService?.updateTheme(chatThemeDark)

```

