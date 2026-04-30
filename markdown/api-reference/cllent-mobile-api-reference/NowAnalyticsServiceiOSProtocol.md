---
title: NowAnalyticsService protocol - iOS
description: The NowAnalyticsService protocol provides functions that enable you to configure analytics properties, user settings, and events for managing the collection of user analytics data.Adds an application event, such as a user reaching a specific level or screen, and enables the setting of custom properties on the event. These events appear on the dashboard in the order that they occurred.Adds a custom action to the current screen. These actions appear in the user dashboard as part of the session data and describes a screen change in an application.Appends the specified item to the specified user property list.Deletes all analytics data associated with the current user. This method also unsets the current active user and opts this device out of future tracking.Increments or decrements the value of the specified numeric property by the specified value.Enables the calling of the methods in the SNAnalytics\(\) API from within a WebView using JavaScript.Deletes the specified property for the current user.Sets a weak reference for a delegate to receive notifications.Sets the application's user ID for the current user. Pass nil to log out the current user.Sets multiple properties with the specified values for the current user. Properties can be anything that you want to track on the dashboard for a user.Sets the specified property with the specified value for the current user. You can define any property that makes sense for your application.Logs the time when the associated screen first appears in the UI.
locale: en-US
release: yokohama
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Mobile SDK API reference - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowAnalyticsService protocol - iOS

The NowAnalyticsService protocol provides functions that enable you to configure analytics properties, user settings, and events for managing the collection of user analytics data.

An object conforming to this protocol is returned by `sharedAnalyticsService`. Use it in your application to perform API calls.

<table id="table_vx2_klw_5pb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

trackingConsent

</td><td>

Boolean

</td><td>

Flag that indicates whether the user has consented to analytics tracking for the associated device. By default, devices are opted-out. Explicitly setting this value to `false` will immediately finish any ongoing session and delete the locally recorded data.Valid values:

-   true: User consented to anlaytics data being tracked on this device.
-   false: User denied data tracking.

</td></tr></tbody>
</table>**Parent Topic:**[Mobile SDK API reference - iOS](../../concept/MobileSDKiOSAPI.md)

## NowAnalyticsService - addEvent\(named eventName: String, with properties: \[String: Any\]?\)

Adds an application event, such as a user reaching a specific level or screen, and enables the setting of custom properties on the event. These events appear on the dashboard in the order that they occurred.

These events appear in your analytics dashboard.

<table id="table_hwl_5vy_spb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

named eventName

</td><td>

String

</td><td>

Name of the event to add.

</td></tr><tr><td>

with properties

</td><td>

Array

</td><td>

Optional. Custom property key-value pairs for the event. Property keys may not contain the dot \('.'\) or dollar \('$'\) signs. They will be trimmed.Supported value types:

-   Date
-   NSNull
-   NSNumber
-   Strings
-   URL

**Note:** The total size of the **eventName**, properties key and value should not exceed 300 bytes \(per event\). Strings are UTF-8 encoded. Events that exceed this limit are ignored.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to add a "Successful Login" event and an "Open Case" event with properties.

```
// Add event with properties
NowAnalytics.sharedAnalyticsService.addEvent(
  named: "Open Case", with: ["Screen Name": "Case",
                             "Case Number": "123",
                             "Case Priority": 5
])
```

## NowAnalyticsService - addScreenAction\(named actionName: String\)

Adds a custom action to the current screen. These actions appear in the user dashboard as part of the session data and describes a screen change in an application.

<table id="table_lxc_hzy_spb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

named actionName

</td><td>

String

</td><td>

Name of the action to add to the screen, such as `MyButtonClick`.Maximum length: 256 UTF-8 bytes

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
// Add event
NowAnalytics.sharedAnalyticsService.addEvent(named: "Successful Login")
```

## NowAnalyticsService - appendToUserProperty\(named propertyName: String, listItem: String\)

Appends the specified item to the specified user property list.

|Name|Type|Description|
|----|----|-----------|
|named propertyName|String|Name of the user property list to append the **listItem** to.|
|listItem|String|List item to append to the property.|

|Type|Description|
|----|-----------|
|None| |

```
// Append handled case to list
NowAnalytics.sharedAnalyticsService.appendToUserProperty(named: "Case Identifiers", listItem: "TASK-1")

```

## NowAnalyticsService - deleteCurrentUserData\(completion: @escaping \(\(\_ success: Bool\) -&gt; Void\)\)

Deletes all analytics data associated with the current user. This method also unsets the current active user and opts this device out of future tracking.

To set the current user, use the [setUserId\(\)](NowAnalyticsServiceiOSProtocol.md#) method.

<table id="table_akt_yry_spb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr id="mobilesdkiOS-completion_data_dataerror-row"><td>

completion

</td><td>

@escaping \(\(\_ success: Bool\) -&gt; Void\)

</td><td>

Completion handler to execute after the analytics data is deleted. Return values for the completion handler:

-   Success: Returns a Boolean value of true.
-   Failure: Void - Failure may occur if the Appsee servers cannot be reached, as when there is no connectivity. If failure occurs, retry the method.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
// Delete user data
NowAnalytics.sharedAnalyticsService.deleteCurrentUserData(completion: { (success) -> Void in
  if success {
    // deletion succeeded
  } else {
    // deletion failed
  }
})
```

## NowAnalyticsService - incUserProperty\(named propertyName: String, by value: Int\)

Increments or decrements the value of the specified numeric property by the specified value.

|Name|Type|Description|
|----|----|-----------|
|named propertyName|String|Name of the user property to increment.|
|by value|Integer|Value to increment the property by. Enter a negative value to decrement the value.|

|Type|Description|
|----|-----------|
|None| |

```
// Increment the "Cases Handled" count
NowAnalytics.sharedAnalyticsService.incUserProperty(named: "Cases Handled", by: 2)
```

## NowAnalyticsService - installJavascriptInterface\(into webView: WKWebView\)

Enables the calling of the methods in the SNAnalytics\(\) API from within a WebView using JavaScript.

This method returns an [SNMobileAnalytics](../../../SNMobileAnalytics/concept/SNMobileAnalytics.md#) object that is available in JavaScript, which exposes the native methods.

|Name|Type|Description|
|----|----|-----------|
|webView|WKWebView|Web view object in which to inject the JavaScript interface.|

|Type|Description|
|----|-----------|
|Object|[SNMobileAnalytics](../../../SNMobileAnalytics/concept/SNMobileAnalytics.md#)|

```
// Register JS object inside the web page
// This will create an object named 'SNMobileAnalytics' on JS that will have the following methods:
// SNMobileAnalytics.setUserId(userId)                  example: SNMobileAnalytics.setUserId("John Doe")
// SNMobileAnalytics.startScreen(screenName)            example: SNMobileAnalytics.startScreen("WelcomeScreen")
// SNMobileAnalytics.addScreenAction(actionName)        example: SNMobileAnalytics.addScreenAction("MyButtonClick")
// SNMobileAnalytics.addEvent(eventName, properties)    example: SNMobileAnalytics.addEvent("Successful Login")
//                                                               SNMobileAnalytics.addEvent("Successful Login", JSON.stringify({"Screen Name": "Case", "Case Number": "123", "Case Priority": 5}))
NowAnalytics.sharedAnalyticsService.installJavascriptInterface(into: webView)

```

## NowAnalyticsService - removeUserProperty\(named propertyName: String\)

Deletes the specified property for the current user.

To set the current user, use the [setUserId\(\)](NowAnalyticsServiceiOSProtocol.md#) method.

|Name|Type|Description|
|----|----|-----------|
|named propertyName|String|Name of the user property to delete.|

|Type|Description|
|----|-----------|
|None| |

```
// Remove unnecessary property
NowAnalytics.sharedAnalyticsService.removeUserProperty(named: "Temp Cases")

```

## NowAnalyticsService - setDelegate\(\_ delegate: NowAnalyticsServiceDelegate?\)

Sets a weak reference for a delegate to receive notifications.

<table id="table_d42_j31_tpb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

delegate

</td><td>

[NowAnalyticsServiceDelegate](../../NowAnalyticsServiceDelegate/concept/NowAnalyticsServiceDeliOSProtocol.md#)

</td><td>

Optional. Object that contains the reference to the delegate class.```
// Register delegate
private var analyticsDelegate = NowAnalyticsDelegate()  // Keep ref of delegate
NowAnalytics.sharedAnalyticsService.setDelegate(analyticsDelegate)
```

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

This example shows how to define a delegate class for NowAnalyticsServiceDelegate.

```
// Define a delegate class for NowAnalyticsServiceDelegate
class NowAnalyticsDelegate: NowAnalytics.NowAnalyticsServiceDelegate {
  func nowAnalyticsSessionShouldStart() -> Bool {
    // Session is about to start, return true to allow session to start
    return true
  }

  func nowAnalyticsSessionDidStart(_ sessionId: String) {
    // Session was started
  }

  func nowAnalyticsSessionShouldEnd(_ sessionId: String) -> Bool {
    // Session is about to end, return true to allow session to end
    return true
  }

  func nowAnalyticsSessionDidEnd(_ sessionId: String) {
    // Session was ended
  }

  func nowAnalyticsDidDetectScreen(_ screenName: String) -> String? {
    // Example of skipping specific screen detection
    if (screenName == "LoginViewController") {
      return nil
    }

    // Example of appending a prefix for every screen detected
    return "MyApp_" + screenName
  }
}

// Register delegate
private var analyticsDelegate = NowAnalyticsDelegate()  // Keep ref of delegate
NowAnalytics.sharedAnalyticsService.setDelegate(analyticsDelegate)
```

## NowAnalyticsService - setUserId\(\_ userId: String?\)

Sets the application's user ID for the current user. Pass nil to log out the current user.

<table id="table_r2r_x1z_spb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

userId

</td><td>

String

</td><td>

Optional. Application-specific user identifier.To log the current user out, pass `nil`.

The user ID must not contain HTML tags or any personal data such as name, email, or phone number.

Maximum length: 256 UTF-8 bytes

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
// Add several properties at once
NowAnalytics.sharedAnalyticsService.setUserProperties([
  "Cases Handled": 100,
  "Last Login": Date(),
  "Is Remote": true,
  "Profile URL": URL(string: "https://www.servicenow.com")!
])
```

## NowAnalyticsService - setUserProperties\(\_ userProperties: \[String: Any\]\)

Sets multiple properties with the specified values for the current user. Properties can be anything that you want to track on the dashboard for a user.

You must call the [setUserId\(\)](NowAnalyticsServiceiOSProtocol.md#) function before calling this function.

<table id="table_o5w_vfz_spb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

userProperties

</td><td>

Array

</td><td>

Key-value pairs of the user properties to set.Supported value types:

-   NSNumber
-   Strings
-   Date
-   URL
-   NSNull

Key may not contain dots \('.'\) or dollar \('$'\) signs.

Maximum length:

-   key: 256 characters
-   value: 1,000 characters

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
import NowAnalytics

// Initialize the Analytics SDK
NowAnalytics.configure(for: URL(string: "https://my.instance.service-now.com")!)

// Enable tracking consent
NowAnalytics.sharedAnalyticsService.trackingConsent = true

// Set User Id for proper identification
NowAnalytics.sharedAnalyticsService.setUserId("John Doe")

// Set the "Role" property of the user to "Admin"
NowAnalytics.sharedAnalyticsService.setUserProperty(named: "Role", with: "Admin")

// Add several properties at once
NowAnalytics.sharedAnalyticsService.setUserProperties([
    "Cases Handled": 100,
    "Last Login": Date(),
    "Is Remote": true,
    "Profile URL": URL(string: "https://www.servicenow.com")!
])
```

## NowAnalyticsService - setUserProperty\(named propertyName: String, with value: Any?\)

Sets the specified property with the specified value for the current user. You can define any property that makes sense for your application.

You must call the [setUserId\(\)](NowAnalyticsServiceiOSProtocol.md#) function before calling this function.

<table id="table_idn_sdz_spb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

named propertyName

</td><td>

String

</td><td>

Name of the user property to set. May not contain dots \('.'\) or dollar \('$'\) signs.Maximum length: 256 characters

</td></tr><tr><td>

with value

</td><td>

Any

</td><td>

Value to set the user property to.Supported value types:

-   Date
-   NSNull
-   NSNumber
-   Strings
-   URL

Maximum length: 1,000 characters

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
// Set the "Role" property of the user to "Admin"
NowAnalytics.sharedAnalyticsService.setUserProperty(named: "Role", with: "Admin")
```

## NowAnalyticsService - startScreen\(named screenName: String\)

Logs the time when the associated screen first appears in the UI.

Call this method after the viewDidAppear\(\_:\) method.

<table id="table_vw5_fyy_spb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

named screenName

</td><td>

String

</td><td>

Name of the screen to log the start time for, such as `WelcomeScreen`. This can be anything that you want to define as a screen and display/aggregate on an analytics dashboard.Maximum length: 256 UTF-8 bytes

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
// Mark the appearance starting time of a screen
// This method should be usually called from the viewDidAppear
NowAnalytics.sharedAnalyticsService.startScreen(named: "WelcomeScreen")

```

