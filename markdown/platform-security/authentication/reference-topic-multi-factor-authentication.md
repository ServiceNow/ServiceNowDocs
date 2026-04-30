---
title: Reference topic - Multi-factor authentication
description: Reference topic related to the configuration of Multi-factor authentication.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring MFA, supported methods, and workflow, Multi-factor authentication \(MFA\), Authentication, Access Management]
---

# Reference topic - Multi-factor authentication

Reference topic related to the configuration of Multi-factor authentication.

## User Multi-factor Authentications

To access the details about the user's multi-factor authentication, navigate to **All** &gt; **Multi-factor Authentication** &gt; **User Multi-factor Setup**.

|Field|Description|
|-----|-----------|
|User|The username of the user|
|Bypasses remaining|The total number of bypasses that is remaining for the user.|
|Multi-factor secret|The details of the multi-factor secret.|
|Validated|Is the multi-factor validated. Changing the value to **false** invalidates the existing authenticator app setup.|

**Note:** The recently used MFA factors by the users is available in the User Recent Used Factors module. Navigate to **All** &gt; **Multi-factor Authentication** &gt; **User Recent User Factors**. For more information, see [User Recent Used Factors](reference-topic-multi-factor-authentication.md#section_owm_bs2_4bc).

## Multi-factor Browser Fingerprints

To access the details about the user's browser fingerprints, navigate to **All** &gt; **Multi-factor Authentication** &gt; **Multi-factor Browser Fingerprints**.

|Field|Description|
|-----|-----------|
|User|The username of the user|
|Browser|The browser that the user used.|
|Browser Fingerprint|The browser fingerprint details.|
|Browser Fingerprint Cookie|The browser fingerprint cookie details.|
|Browser Fingerprint Cookie Expiry|The browser fingerprint cookie expiry details.|

## User Recent Used Factors

To access the details about the user's recently used factors, navigate to **All** &gt; **Multi-factor Authentication** &gt; **User Recent User Factors**.

|Field|Description|
|-----|-----------|
|User|The username of the user|
|Multi Factor Type|The multi-factor type the user used for log in.|
|Is Recent Factor|The user's recent multi-factor detials.|

