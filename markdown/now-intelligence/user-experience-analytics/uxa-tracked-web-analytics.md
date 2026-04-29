---
title: Tracked web analytics fields for Usage Insights
description: Usage Insights collects data from web applications. These tables list the fields that are tracked. Reports and charts are generated from these fields.
locale: en-US
release: australia
product: User Experience Analytics
classification: user-experience-analytics
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Tracked analytics fields and cookies, User privacy, tracking, and consent, Configuring Usage Insights, Usage Insights, Platform Analytics]
---

# Tracked web analytics fields for Usage Insights

Usage Insights collects data from web applications. These tables list the fields that are tracked. Reports and charts are generated from these fields.

For more information about using the data, see [Viewing user analytics](../concept/viewing-user-data.md).

## Collected data according to web session

<table id="table_uy5_yph_qhc"><tbody><tr><td>

Name

</td><td>

Description

</td><td>

Sample output value

</td></tr><tr><td>

UserID 

</td><td>

Usage Insights internal user ID \(sequential ID\) 

</td><td>

1

</td></tr><tr><td>

Hashed user ID

</td><td>

SHA256 hash of the user's ServiceNow® sys\_id 

</td><td>

f4a9baa650ab13d429abacf9f8c78d14fcf5c 

</td></tr><tr><td>

AppSysId

</td><td>

Application sys\_id

</td><td>

e5d8a2df53112110a40fddeeff7b1243

</td></tr><tr><td>

SDKversion

</td><td>

SDK version

</td><td>

 

</td></tr><tr><td>

Channel

</td><td>

Channel of the app \(web, mobile, CoreUI\)

</td><td>

web

</td></tr><tr><td>

InstanceId

</td><td>

Instance ID

</td><td>

 

</td></tr><tr><td>

Instance Family Release

</td><td>

Family release of the instance

</td><td>

Zurich

</td></tr><tr><td>

InstancePurpose

</td><td>

Purpose of the instance \(prod, sub-prod\)

</td><td>

production

</td></tr><tr><td>

Patch release

</td><td>

Release patch number

</td><td>

Zurich p4

</td></tr><tr><td>

Domain ID

</td><td>

User's domain ID

</td><td>

 

</td></tr><tr><td>

Account Number

</td><td>

Customer's account number

</td><td>

 

</td></tr><tr><td>

SessionId 

</td><td>

Unique session ID 

</td><td>

 

</td></tr><tr><td>

DeviceType 

</td><td>

Phone / Tablet / Desktop 

</td><td>

Phone

</td></tr><tr><td>

DeviceID

</td><td>

Device ID

</td><td>

 

</td></tr><tr><td>

Device Resolution

</td><td>

Resolution of the device

</td><td>

112X123

</td></tr><tr><td>

OSType 

</td><td>

Device's operating system 

</td><td>

iOS

</td></tr><tr><td>

OSVersion 

</td><td>

Version of the OS 

</td><td>

16.5

</td></tr><tr><td>

Country Code

</td><td>

Country Code

</td><td>

ISR

</td></tr><tr><td>

City-Level Location 

</td><td>

City location is translated from the end user's IP address. IPs aren't stored on the database. The IPs are only used to provide a city-level location approximation. 

</td><td>

Los Angeles, California

</td></tr><tr><td>

Browser Type 

</td><td>

Type of web browser 

</td><td>

Chrome

</td></tr><tr><td>

Browser Version 

</td><td>

Version of web browser

</td><td>

\(Chrome\) 30.0

</td></tr><tr><td>

Local time

</td><td>

The local time of the user

</td><td>

1:30

</td></tr><tr><td>

Locale 

</td><td>

User locale string 

</td><td>

EN-US

</td></tr><tr><td>

Tracking Level

</td><td>

Which consent type the user has

</td><td>

basic tracking

</td></tr></tbody>
</table>## Collected data for each page visit

|Name|Description|Sample output value|
|----|-----------|-------------------|
|Description|Additional information about the data collected in a page visit|Home page|
|PageId|The page's unique identifier |home|
|StartTime|Relative start time within the session|2023-03-23T23:59:58|

## Collected data for customer events- optional

|Name|Description|Sample output value|
|You can add these events by calling client-side APIs. | | |
|----|-----------|-------------------|
|------------------------------------------------------|---|---|
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

