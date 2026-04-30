---
title: Tracked web analytics fields for User Experience Analytics
description: User Experience Analytics collects data from web applications. These tables list the fields that are tracked. Reports and charts are generated from these fields.
locale: en-US
release: xanadu
product: User Experience Analytics
classification: user-experience-analytics
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Tracked analytics fields and cookies, User privacy, tracking, and consent, Configuring User Experience Analytics, User Experience Analytics, Platform Analytics]
---

# Tracked web analytics fields for User Experience Analytics

User Experience Analytics collects data from web applications. These tables list the fields that are tracked. Reports and charts are generated from these fields.

For more information about using the data, see [Viewing user analytics](../concept/viewing-user-data.md).

## Collected data according to web session

|Name|Description|Sample output value|
|----|-----------|-------------------|
|UserID |User Experience Analytics internal user ID \(sequential ID\) |1|
|Hashed User Id |SHA256 hash of the user's ServiceNow sys\_id |f4a9baa650ab13d429abacf9f8c78d14fcf5c |
|SessionId |Unique session ID | |
|SessionIndex |Sequential index of the specific user's session |5|
|StartTime |Session's start time in UTC format |2023-03-23T23:59:58|
|Session Duration |Session's duration in milliseconds |5165|
|DeviceType |Phone / Tablet / Desktop |Phone|
|Device |Device’s make and model. Only for mobile and tablet devices.|iPhone 12|
|OSType |Device's operating system |iOS|
|OSVersion |Version of the OS |16.5|
|City-Level Location |City location is translated from the end user's IP address. IPs aren't stored on the database. The IPs are only used to provide a city-level location approximation. |Los Angeles, California|
|Browser Type |Type of the web browser |Chrome|
|Browser Version |Version of the web browser|\(Chrome\) 30.0|
|Locale |User locale string |EN-US|

## Collected data for each page visit

|Name|Description|Sample output value|
|----|-----------|-------------------|
|Description|Additional information about the data collected in a page visit|Home Page|
|PageId|The page's unique identifier |home|
|StartTime|Relative start time within the session|2023-03-23T23:59:58|

## Collected data for customer events \(optional\)

These events can be added by calling client-side APIs. 

|Name|Description|Sample output value|
|----|-----------|-------------------|
|Name|Name of the event |Submit Catalog Request|
|Time|Event time \(in milliseconds\) from the beginning of the session\) |945|

## Collected data for event properties

|Name|Description|Sample output value|
|----|-----------|-------------------|
|PageId|ID of the current page |home|
|Property Name &amp; Value |Key value collection of property names and values |\{"Version" : "1.0", “Active” : “false”\} |

## Collected data for optional properties

|Name|Description|Sample output value|
|----|-----------|-------------------|
|Property Name &amp; Value |Key value collection of property names and values |\{“Language” : “English”\} |

**Parent Topic:**[Tracked analytics fields and cookies](../concept/uxa-tracked-fields-and-cookies.md)

