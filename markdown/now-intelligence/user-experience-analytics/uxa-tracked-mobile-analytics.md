---
title: Tracked mobile analytics fields for User Experience Analytics
description: User Experience Analytics collects data from mobile applications on your mobile device. These tables list fields that are tracked in the mobile applications. Reports and charts are generated from these fields.
locale: en-US
release: xanadu
product: User Experience Analytics
classification: user-experience-analytics
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Tracked analytics fields and cookies, User privacy, tracking, and consent, Configuring User Experience Analytics, User Experience Analytics, Platform Analytics]
---

# Tracked mobile analytics fields for User Experience Analytics

User Experience Analytics collects data from mobile applications on your mobile device. These tables list fields that are tracked in the mobile applications. Reports and charts are generated from these fields.

For more information about using the data, see [Viewing user analytics](../concept/viewing-user-data.md).

## Collected data according to the mobile app session

|Name|Description|Sample output value|
|----|-----------|-------------------|
|User Id |User Experience Analytics internal user ID \(sequential ID\) |1|
|Hashed User Id |SHA256 hash of the user's ServiceNow sys\_id |f4a9baa650ab13d429b185d12b14fcf5c |
|Session Id |Unique session ID |5a2b73857345abc3546243 |
|Session Index |Sequential index of the specific user's session |5|
|Start Time |Session's start time in UTC format |2023-03-23T23:59:58|
|Session Duration |Session's duration in milliseconds |5165|
|App Version |The application’s version number |3.4.0|
|Device Type |Phone / Tablet |Phone|
|Device |Device’s make and model. Only for mobile and tablet devices.|iPhone X13 Pro|
|ROM Version |The ROM version \(only for Android\) |4.3.9|
|Operating System Version |Version of the device's operating system |iOS 16.5|
|Network connectivity |WiFi / Cellular |WiFi|
|City Location |City level location translated from the user's IP address |Los Angeles, California |

## Collected data for each screen visit

|Name|Description|Sample output value|
|----|-----------|-------------------|
|Screen Name |Name of the screen that data is collected from|Login|
|Start Time |Relative start time within the session |2023-03-23T23:59:58|

## Collected data for screen actions

|Name|Description|Sample output value|
|----|-----------|-------------------|
|Type |Type of UI action \(button tap, list selection, and so on\) |ButtonTap|
|Description |Label describing the UI action |Login|
|StartTime | Time in milliseconds from the session start time |780 |

## Collected data for screen gestures

|Name|Description|Sample output value|
|----|-----------|-------------------|
|GestureType |Type of gesture \(Tap, swipe, and so on\) |Tap |
|Coordinates |The X,Y coordinates of the touch gesture |TAP \(X=100, Y=200\) |
|Responsive |Indicates whether the gesture was responsive |TRUE |
|StartTime |Gesture start time \(in milliseconds\) |925|
|EndTime |Gesture end time \(in milliseconds\) |933|

## Collected data for customer events \(optional\)

These events can be added by calling client-side APIs. 

|Name|Description|Sample output value|
|----|-----------|-------------------|
|Name|Name of the event property \(string\) |PurchaseComplete|
|Time|Value of the event property \(string, Boolean, date, number\) |9456|

## Collected data for event properties

|Name|Description|Sample output value|
|----|-----------|-------------------|
|Property Name |Name of the event property \(string\) |Article Name, Language |
|Property Value |Value of the event property \(string, Boolean, date, number\) |KB0050925|

## Collected data for user properties

|Name|Description|Sample output value|
|----|-----------|-------------------|
|Property Name |Name of the user property \(string\) |English|
|Property Value |Value of the user property \(string, Boolean, date, number\) |5|

**Parent Topic:**[Tracked analytics fields and cookies](../concept/uxa-tracked-fields-and-cookies.md)

