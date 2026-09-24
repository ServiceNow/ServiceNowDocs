---
title: Verification checklist
description: Use this table to check the enrollment status, device grouping, policy assignment, and single sign-on across Microsoft Entra and ServiceNow mobile apps.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/ios-device-share-verification.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [iOS device-level configuration, Device-level configuration, Multiple users on a shared device, Mobile instances, Configuring the Mobile Platform, Mobile Platform]
---

# Verification checklist

Use this table to check the enrollment status, device grouping, policy assignment, and single sign-on across Microsoft Entra and ServiceNow mobile apps.

|Check|Where can this occur|Expected behavior|
|-----|--------------------|-----------------|
|Token health|Enrollment program tokens|Status Active, last sync status Success|
|Device assigned|Token &gt; Devices &gt; device properties|Assigned profile is your shared device mode policy; state = Enrolled; supervised = Yes|
|Device grouped|Entra ID &gt; group &gt; Members|Device listed as a Device-type member|
|Configuration applied|Configuration profile &gt; device and user check-in status|Succeeded count matches device count; zero errors and conflicts|
|Filter matching|Device &gt; Monitor &gt; Filter evaluation|Device evaluates as matched|
|No primary user|Device &gt; Overview|Primary user: None, ownership Corporate|
|Shared mode live|Microsoft Authenticator on the device|Shared device mode indicated in the app|
|Single sign-on working|ServiceNow mobile app|Opens signed in with no second credential prompt|

