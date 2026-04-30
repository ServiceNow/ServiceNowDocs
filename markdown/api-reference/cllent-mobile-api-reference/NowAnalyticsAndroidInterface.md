---
title: NowAnalyticsSDK interface - Android
description: The NowAnalyticsSDK interface provides functions that enable you to configure analytics properties, user settings, and events for managing a collection of user analytics data.Adds an application event, such as a user reaching a specific level or screen. These events appear on the dashboard in the order that they occurred.Adds an application event, such as a user reaching a specific level or screen, and enables the setting of custom properties on the event. These events appear on the dashboard in the order that they occurred.Adds a custom action. These actions appear in the user dashboard as part of the session data and describes a screen change in an application.Appends the specified item to the specified user property list.Configures the specified ServiceNow instance URL and callbacks to NowAnalytics.Deletes all local and remote data for the current user.Returns the current user's consent response to analytics tracking.Increments or decrements the value of the specified numeric property by the specified value.Enables the calling of javaScript.SNMobileAnalytics methods from within a \{@link android.webkit.WebView\}, using JavaScript.Deletes the specified property for the current user.Sets a listener on the NowAnalytics' events such as session changes and automatic screen detections.Sets the current user's consent response to analytics tracking.Sets the application-specific user identifier. Pass nil to log the current user out.Sets multiple properties with the specified values for the current user. Properties can be anything that you want to track on the dashboard for a user.Sets the specified property with the specified value for the current user. Properties can be anything that you want to track on the dashboard for a user.Logs the time when the associated screen first appears in the UI.
locale: en-US
release: zurich
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Mobile SDK - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowAnalyticsSDK interface- Android

The NowAnalyticsSDK interface provides functions that enable you to configure analytics properties, user settings, and events for managing a collection of user analytics data.

|Name|Type|Description|
|----|----|-----------|
|configuration|[NowServiceConfiguration](../../NowServiceConfiguration/concept/NowServiceConfigurationAndroidAPI.md)|Configuration to associate with the service.|

**Parent Topic:**[Mobile SDK - Android](../../concept/MobileSDKAndroidAPI.md)

## NowAnalyticsSDK - addEvent\(eventName: String\)

Adds an application event, such as a user reaching a specific level or screen. These events appear on the dashboard in the order that they occurred.

|Name|Type|Description|
|----|----|-----------|
|named eventName|String|Name of the event to add.|

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function to add an application event.

```
// Add event
NowAnalyticsSDK.getAnalyticsService().addEvent("Successful Login")
```

## NowAnalyticsSDK - addEvent\(eventName: String, props: MutableMap&lt;String, Any&gt;\)

Adds an application event, such as a user reaching a specific level or screen, and enables the setting of custom properties on the event. These events appear on the dashboard in the order that they occurred.

<table id="table_ps4_j3m_tpb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

eventName

</td><td>

String

</td><td>

Name of the event to add.

</td></tr><tr><td>

props

</td><td>

[MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/)

</td><td>

Custom property key-value pairs for the event. The total size of the event name, property key and value cannot exceed 300 bytes per property. Properties that exceed this limit are ignored. Property keys may not contain dot \('.'\) or dollar \('$'\) signs, if they do, they are trimmed. Strings are UTF-8 encoded.

Supported value types:

-   Integer
-   Double
-   Float
-   String
-   Url
-   Boolean
-   Date

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function to add an application event that includes custom properties for the event.

```
// Add event with properties
NowAnalyticsSDK.getAnalyticsService().addEvent("Open Case",
  mutableMapOf(
    "Screen Name" to "Case",
    "Case Number" to 123,
    "Case Priority" to 5
  )
)
```

## NowAnalyticsSDK - addScreenAction\(actionName: String\)

Adds a custom action. These actions appear in the user dashboard as part of the session data and describes a screen change in an application.

|Name|Type|Description|
|----|----|-----------|
|actionName|String|Name of the action to add to the screen, such as `MyButtonClick`.|

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function to add a custom action to the current screen.

```
// Add a custom action to the current screen
NowAnalyticsSDK.getAnalyticsService().addScreenAction("MyButtonClick")
```

## NowAnalyticsSDK - appendToUserProperty\(propertyName: String, item: String\)

Appends the specified item to the specified user property list.

|Name|Type|Description|
|----|----|-----------|
|propertyName|String|Name of the user property to append the list item to.|
|item|String|List item to append to the property.|

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function to append a case to the specified list.

```
// Append handled case to list
NowAnalyticsSDK.getAnalyticsService().appendToUserProperty("Case Identifiers", "TASK-1")
```

## NowAnalyticsSDK - configure\(instanceURL: URL, configureCallbacks: ConfigureCallbacks?\)

Configures the specified ServiceNow instance URL and callbacks to NowAnalytics.

Once this method is called, the actual configuration is fetched from the associated ServiceNow instance and synced automatically.

|Name|Type|Description|
|----|----|-----------|
|instanceURL|URL|URL of the ServiceNow instance to associate with the NowAnalyticfs service.|
|configureCallbacks|ConfigureCallbacks|Optional. Callback to execute whenever there is an error communicating to the ServiceNow instance. This callback can be called at any point in time and can be called multiple times for multiple reasons.|

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function to configure the specified instance.

```
// Init NowAnalytics after NowSDK is initialized
NowAnalyticsSDK.getAnalyticsService().configure(URL("https://my.instance.service-now.com"),
  // Optional - pass callback
  object: ConfigureCallbacks {
    override fun onFail(e: Exception) {
      // configuration failed
    }

    override fun onSuccess() {
      // configuration succeeded
    }
  }
)
```

## NowAnalyticsSDK - deleteCurrentUserData\(\)

Deletes all local and remote data for the current user.

This method also unsets the current active user and opts this device out of future analytics tracking.

**Note:** This method performs a synchronous call to the SNAnalytics servers. It is therefore recommended that you perform this on a side thread.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_ugk_jjj_5pb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the deletion was successful.Possible values:

-   true: Deletion was successful.
-   false: Deletion failed. Failure may occur if the SNAnalytics servers cannot be reached, such as when there is no connectivity. The method should be retried.

</td></tr></tbody>
</table>The following code example shows how to call this function to delete the current user's data.

```
// Delete user data
NowAnalyticsSDK.getAnalyticsService().deleteCurrentUserData()
```

## NowAnalyticsSDK - getTrackingConsent\(\)

Returns the current user's consent response to analytics tracking.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_ylm_cmj_5pb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the current user consented to having their data collected.Possible values:

-   true: User agreed to having their data collected.
-   false: User opted out of having their data collected.

</td></tr></tbody>
</table>The following code example shows how to call this function to request the current user's consent response to analytics tracking.

```
// Get the current user tracking consent value
val curUserConsent = NowAnalytics.sharedAnalyticsService.getTrackingConsent()
```

## NowAnalyticsSDK - incUserProperty\(propertyName: String, value: Double\)

Increments or decrements the value of the specified numeric property by the specified value.

|Name|Type|Description|
|----|----|-----------|
|propertyName|String|Name of the user property to increment.|
|value|Double|Value to increment the property by. Enter a negative value to decrement the value.|

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function.

```
// Increment numeric_property_name by one
NowAnalyticsSDK.getAnalyticsService().incUserProperty("numeric_property_name", 1.0)

// Decrement numeric_property_name by one
NowAnalyticsSDK.getAnalyticsService().incUserProperty("numeric_property_name", -1.0)
```

## NowAnalyticsSDK - installJavascriptInterface\(webView: WebView\)

Enables the calling of javaScript.SNMobileAnalytics methods from within a \{@link android.webkit.WebView\}, using JavaScript.

|Name|Type|Description|
|----|----|-----------|
|webView|WKWebView|The \{@link android.webkit.WebView\} to attach to.|

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function to enable the calling of javaScript.SNMobileAnalytics methods.

```
// Register JS object inside the web page
// This creates an object called 'SNMobileAnalytics' on JS that has the following methods:
// SNMobileAnalytics.setUserId(userId)                 
//   example: SNMobileAnalytics.setUserId("John Doe")
// SNMobileAnalytics.startScreen(screenName)
//   example: SNMobileAnalytics.startScreen("WelcomeScreen")
// SNMobileAnalytics.addScreenAction(actionName)
//   example: SNMobileAnalytics.addScreenAction("MyButtonClick")
// SNMobileAnalytics.addEvent(eventName, properties)
//   example: SNMobileAnalytics.addEvent("Successful Login")
//                                                               
SNMobileAnalytics.addEvent("Successful Login", JSON.stringify({"Screen Name": "Case", "Case Number": "123", "Case Priority": 5}))
NowAnalyticsSDK.getAnalyticsService().installJavascriptInterface(webView)
```

## NowAnalyticsSDK - removeUserProperty\(propertyName: String\)

Deletes the specified property for the current user.

|Name|Type|Description|
|----|----|-----------|
|propertyName|String|Name of the user property to delete.|

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function to remove the "Temp Cases" property.

```
// Remove unnecessary property
NowAnalyticsSDK.getAnalyticsService().removeUserProperty("Temp Cases")
```

## NowAnalyticsSDK - setListener\(nowAnalyticsListener: NowAnalyticsListener?\)

Sets a listener on the NowAnalytics' events such as session changes and automatic screen detections.

**Note:** Every time you call this method, the listener is overridden.

<table id="table_zsr_s3p_5qb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

nowAnalytics​Listener

</td><td>

NowAnalytics​Listener

</td><td>

The interface that NowAnalytics notifies for session events.-   onNowAnalyticsScreenDetected: Called when NowAnalytics automatically detects a screen.
-   onNowAnalyticsSessionEnded: Called after a session ends.
-   onNowAnalyticsSessionEnding: Called just before a session is about to finish, allowing you to prevent the session from ending.
-   onNowAnalyticsSessionStarted: Called when a session has started.
-   onNowAnalyticsSessionStarting: Called just before a session is about to start, allowing you to prevent the session from being started.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function to set the NowAnalyticsListener\(\).

```
// From anywhere in the code you can register the delegate
NowAnalyticsSDK.getAnalyticsService().setListener(NowAnalyticsListener())
```

## NowAnalyticsSDK - setTrackingConsent\(consentGiven: Boolean\)

Sets the current user's consent response to analytics tracking.

<table id="table_tq5_2sj_5pb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

consentGiven

</td><td>

Boolean

</td><td>

Flag that indicates the current user's consent for analytics tracking.Valid values:

-   true: User consented to having their data tracked.
-   false: User opted out of having their data tracked.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function to set the current user's consent response to analytics tracking.

```
// Enable tracking consent
NowAnalyticsSDK.getAnalyticsService().setTrackingConsent(true)
```

## NowAnalyticsSDK - setUserId\(userId: String\)

Sets the application-specific user identifier. Pass nil to log the current user out.

|Name|Type|Description|
|----|----|-----------|
|userId|String|Unique application-specific user identifier. This identifier is used to aggregate reports for that user in the dashboard.|

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function to set the application-specific user identifier to "John Doe".

```
// Set User Id for proper identification
NowAnalyticsSDK.getAnalyticsService().setUserId("John Doe")
```

## NowAnalyticsSDK - setUserProperties\(userProperties: MutableMap&lt;String, Any&gt;\)

Sets multiple properties with the specified values for the current user. Properties can be anything that you want to track on the dashboard for a user.

To set the current user, call the [NowAnalyticsSDK - setUserId\(userId: String\)](NowAnalyticsAndroidInterface.md#) function.

<table id="table_wqc_g5j_5pb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

userProperties

</td><td>

MutableMap

</td><td>

Key-value pairs of the user properties to set.Supported value types:

-   Number
-   Strings
-   Date
-   URL
-   Null

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function to set multiple properties for the current user.

```
// Add several properties at once
NowAnalyticsSDK.getAnalyticsService().setUserProperties(
  mutableMapOf(
    "Cases Handled" to 100,
    "Last Login" to Date(),
    "Is Remote" to true,
    "Profile URL" to URL("https://www.servicenow.com")
  )
)
```

## NowAnalyticsSDK - setUserProperty\(propertyName: String, propertyValue: Any\)

Sets the specified property with the specified value for the current user. Properties can be anything that you want to track on the dashboard for a user.

To set the current user, call the [NowAnalyticsSDK - setUserId\(userId: String\)](NowAnalyticsAndroidInterface.md#) function.

<table id="table_fzh_fvj_5pb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

propertyName

</td><td>

String

</td><td>

Name of the user property to set.

</td></tr><tr><td>

value

</td><td>

Any

</td><td>

Value to set the user property to.Supported value types:

-   Number
-   Strings
-   Date
-   URL
-   Null

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function to set the property "Role" to "Admin" for the current user.

```
// Set the "Role" property of the user to "Admin"
NowAnalyticsSDK.getAnalyticsService().setUserProperty("Role", "Admin")
```

## NowAnalyticsSDK - startScreen\(screenName: String\)

Logs the time when the associated screen first appears in the UI.

You typically call this method from the activity's onResume\(\) method.

|Name|Type|Description|
|----|----|-----------|
|named screenName|String|Name of the screen to log the start time for, such as `WelcomeScreen`. This can be anything that you want to define as a screen and display/aggregate on an analytics dashboard.|

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function to set the start time of the display of the "WelcomeScreen".

```
// Mark the appearance starting time of a screen
// This method should be usually called from the onResume() method
NowAnalyticsSDK.getAnalyticsService().startScreen("WelcomeScreen")
```

