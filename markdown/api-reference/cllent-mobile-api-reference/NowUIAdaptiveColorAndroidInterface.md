---
title: NowUIAdaptiveColor - Android
description: The NowUIAdaptiveColor interface provides functions that return an integer or hexadecimal color value based on the calling device's theme mode setting.Returns an integer color value based on the calling device's theme mode setting.Returns a hexadecimal color value based on the calling device's theme mode setting.
locale: en-US
release: yokohama
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Mobile SDK API reference - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowUIAdaptiveColor - Android

The NowUIAdaptiveColor interface provides functions that return an integer or hexadecimal color value based on the calling device's theme mode setting.

It returns the value for the **darkColor** theme if dark mode is enabled on the user's device and the value for the **lightColor** theme for all other scenarios.

**Parent Topic:**[Mobile SDK API reference - Android](../../concept/MobileSDKAndroidAPI.md)

## NowUIAdaptiveColor - getColor\(context: Context?\)

Returns an integer color value based on the calling device's theme mode setting.

It returns the value for the **darkColor** theme if dark mode is enabled on the user's device and the value for the **lightColor** theme for all other scenarios.

<table id="table_ofl_mdk_pzb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

context

</td><td>

Object

</td><td>

Comma-separated list of colors for which to return the color values.For examples: `NowUIAdaptiveColor(lightColor = Color.BLACK, darkColor = Color.WHITE)`

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Integer|Color value for the passed color.|

The following code example shows how to use this function.

```
lifecycleScope.launch {
  sdkManager.getNowWebService()?.launch(this@MainActivity, URL("https://instance-name.service-now.com"), object : NowWebTheme {
    override val brand: NowUIAdaptiveColor
      // Override lightColor only. For dark theme default color will be used
      get() = NowUIAdaptiveColor(lightColor = Color.BLACK)

    override val primary: NowUIAdaptiveColor
      // Override both lightColor and darkColor
       get() = NowUIAdaptiveColor(lightColor = Color.BLACK, darkColor = Color.WHITE)

    // override the rest of color variables
  })
}
```

## NowUIAdaptiveColor - toStringColor\(context: Context?\)

Returns a hexadecimal color value based on the calling device's theme mode setting.

<table id="table_j3r_hxk_pzb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

context

</td><td>

Object

</td><td>

Comma-separated list of colors for which to return the color values.For examples: `NowUIAdaptiveColor(lightColor = Color.BLACK, darkColor = Color.WHITE)`

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|Hexadecimal color value for the passed colors.|

The following code example shows how to use this function.

```
val adaptiveColor = NowUIAdaptiveColor(lightColor = Color.BLACK, darkColor = Color.WHITE)
adaptiveColor.toStringColor(context)
```

