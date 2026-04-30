---
title: Tracked mobile analytics fields for User Experience Analytics
description: User Experience Analytics collects data from mobile applications on your mobile device. These tables list fields that are tracked in the mobile applications. Reports and charts are generated from these fields.
locale: en-US
release: yokohama
product: User Experience Analytics
classification: user-experience-analytics
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Tracked analytics fields and cookies, User privacy, tracking, and consent, Configuring User Experience Analytics, User Experience Analytics, Platform Analytics]
---

# Tracked mobile analytics fields for User Experience Analytics

User Experience Analytics collects data from mobile applications on your mobile device. These tables list fields that are tracked in the mobile applications. Reports and charts are generated from these fields.

For more information about using the data, see [Viewing user analytics](../concept/viewing-user-data.md).

## Collected data according to the mobile app session

|Name|Description|Sample output value|
|----|-----------|-------------------|
|User ID|User Experience Analytics internal user ID \(sequential ID\) |1|
|Hashed User ID|SHA256 hash of the user's ServiceNow sys\_id |f4a9baa650ab13d429b185d12b14fcf5c |
|Session ID|Unique session ID |5a2b73857345abc3546243 |
|Session Index |Sequential index of the specific user's session |5|
|Start Time |Session's start time in UTC format |2023-03-23T23:59:58|
|Session Duration |Session's duration in milliseconds |5165|
|App Version |The application’s version number |3.4.0|
|Device Type |Phone / Tablet |Phone|
|Device |Device’s make and model. Only for mobile and tablet devices.|iPhone X13 Pro|
|ROM Version |The ROM version \(only for Android\) |4.3.9|
|Operating System Version |Version of the device's operating system |iOS 16.5|
|Network connectivity |WiFi / Cellular |WiFi|
|UserID |User Experience Analytics internal user ID \(sequential ID\) |1|
|Hashed User ID|SHA256 hash of the user's ServiceNow sys\_id |f4a9baa650ab13d429abacf9f8c78d14fcf5c |
|AppSysId|Application sys\_id|e5d8a2df53112110a40fddeeff7b1243|
|AppVersion|Application version|1.2|
|SDKversion|SDK version| |
|Connectivity|Connectivity Type \(WiFi / system\)|WiFi|
|Channel|Channel of the app \(web, mobile, CoreUI\)|web|
|InstanceId|Instance ID| |
|Instance Family Release|Family release of the instance|Zurich|
|InstancePurpose|Purpose of the instance \(prod, sub-prod\)|production|
|Patch release|The patch number of the release|Zurich p4|
|Domain ID|The user's domain ID| |
|Account Number|The customer's account number| |
|SessionId |Unique session ID | |
|DeviceType |Phone / Tablet / Desktop |Phone|
|DeviceID|Device ID| |
|Device Code|Device’s model. Only for mobile and tablet devices.|iPhone 12|
|Device Resolution|Resolution of the device|112X123|
|OSType |Device's operating system |iOS|
|OSVersion |Version of the OS |16.5|
|Country Code|Country Code|ISR|
|City-Level Location |City location is translated from the end user's IP address. IPs aren't stored on the database. The IPs are only used to provide a city-level location approximation. |Los Angeles, California|
|Local time|The local time of the user|1:30|
|Locale |User locale string |EN-US|
|Tracking Level|Which consent type the user has|basic Tracking|

## Collected data for each screen visit

|Name|Description|Sample output value|
|----|-----------|-------------------|
|Screen Name |Name of the screen that data is collected from|Login|
|Start Time |Relative start time within the session |2023-03-23T23:59:58|

## Collected data for customer events- optional

You can add these events by calling client-side APIs. 

|Name|Description|Sample output value|
|----|-----------|-------------------|
|Name|Name of the event |Submit Catalog Request|
|Time|Event time \(in milliseconds\) from the beginning of the session|945|

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

