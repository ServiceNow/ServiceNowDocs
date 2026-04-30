---
title: NowAnalyticsServiceDelegate protocol - iOS
description: The NowAnalyticsServiceDelegate protocol provides callback functions that provide information about the starting and ending of a user session and screen change detection.Notifies when a screen change is detected. The screen name is detected from the navigation bar. If that is not possible, it is the viewController subclass name.Notifies when the specified session has ended.Notifies when the specified session has started.Notifies when the specified session is about to end.Notifies whether the specified session is about to start.
locale: en-US
release: yokohama
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Mobile SDK API reference - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowAnalyticsServiceDelegate protocol - iOS

The NowAnalyticsServiceDelegate protocol provides callback functions that provide information about the starting and ending of a user session and screen change detection.

**Parent Topic:**[Mobile SDK API reference - iOS](../../concept/MobileSDKiOSAPI.md)

## NowAnalyticsServiceDelegate - nowAnalyticsDidDetectScreen\( \_ sessionId: String\)

Notifies when a screen change is detected. The screen name is detected from the navigation bar. If that is not possible, it is the viewController subclass name.

|Name|Type|Description|
|----|----|-----------|
|screenName|String|Name of the screen to detect whether there is any change.|

|Type|Description|
|----|-----------|
|String|Custom name to use to override the passed screenName.|

This example shows how to define a delegate class for NowAnalyticsServiceDelegate.

```
import NowAnalytics

// Initialize the Analytics SDK
NowAnalytics.configure(for: URL(string: "https://my.instance.service-now.com")!)

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

## NowAnalyticsServiceDelegate - nowAnalyticsSessionDidEnd\( \_ sessionId: String\)

Notifies when the specified session has ended.

This is a callback function that gets called when the specified session actually ends.

|Name|Type|Description|
|----|----|-----------|
|sessionId|String|Unique identifier of the session to check.|

|Type|Description|
|----|-----------|
|None| |

This example shows how to define a delegate class for NowAnalyticsServiceDelegate.

```
import NowAnalytics

// Initialize the Analytics SDK
NowAnalytics.configure(for: URL(string: "https://my.instance.service-now.com")!)

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

## NowAnalyticsServiceDelegate - nowAnalyticsSessionDidStart\( \_ sessionId: String\)

Notifies when the specified session has started.

This is a callback function that gets called when the specified session actually starts.

|Name|Type|Description|
|----|----|-----------|
|sessionId|String|Unique identifier of the session to check.|

<table id="table_otx_m2v_1qb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates that the session is starting.Valid values:

-   true: Session is starting
-   false: Session is not starting

</td></tr></tbody>
</table>This example shows how to define a delegate class for NowAnalyticsServiceDelegate.

```
import NowAnalytics

// Initialize the Analytics SDK
NowAnalytics.configure(for: URL(string: "https://my.instance.service-now.com")!)

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

## NowAnalyticsServiceDelegate - nowAnalyticsSessionShouldEnd\( \_ sessionId: String\)

Notifies when the specified session is about to end.

This is a callback function that gets called when the specified session is about to end.

|Name|Type|Description|
|----|----|-----------|
|sessionId|String|Unique identifier of the session to check.|

<table id="table_mrd_pcv_1qb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates that the session is ending.Valid values:

-   true: Session is ending
-   false: Session is not ending

</td></tr></tbody>
</table>This example shows how to define a delegate class for NowAnalyticsServiceDelegate.

```
import NowAnalytics

// Initialize the Analytics SDK
NowAnalytics.configure(for: URL(string: "https://my.instance.service-now.com")!)

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

## NowAnalyticsServiceDelegate - nowAnalyticsSessionShouldStart\( \_ sessionId: String\)

Notifies whether the specified session is about to start.

This is a callback function that gets called when the specified session is about to start.

|Name|Type|Description|
|----|----|-----------|
|sessionId|String|Unique identifier of the session to check.|

|Type|Description|
|----|-----------|
|None| |

This example shows how to define a delegate class for NowAnalyticsServiceDelegate.

```
import NowAnalytics

// Initialize the Analytics SDK
NowAnalytics.configure(for: URL(string: "https://my.instance.service-now.com")!)

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

