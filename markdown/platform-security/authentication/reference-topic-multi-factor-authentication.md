---
title: Multi-factor Authentication references
description: Lists each user's multi-factor authentication setup, browser fingerprints, and recently used factors.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/authentication/reference-topic-multi-factor-authentication.html
release: australia
product: Authentication
classification: authentication
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configuring MFA, Multi-factor authentication, Authentication, Access Management]
---

# Multi-factor Authentication references

Lists each user's multi-factor authentication setup, browser fingerprints, and recently used factors.

## User multi-factor authentications

To access the details about the user's MFA, navigate to **All** &gt; **Multi-factor Authentication** &gt; **User Multi-factor Setup**.

|Field|Description|
|-----|-----------|
|User|The username of the user|
|Bypasses remaining|The total number of bypasses remaining for the user.|
|Multi-factor secret|The details of the multi-factor secret.|
|Validated|Validation status of the multi-factor setup. Changing the value to **false** invalidates the existing authenticator app setup.|

**Note:** The recently used MFA factors for users are available in the User Recent Used Factors module. Navigate to **All** &gt; **Multi-factor Authentication** &gt; **User Recent Used Factors**. For more information, see [User recent used factors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/authentication/reference-topic-multi-factor-authentication.md).

## Multi-factor browser fingerprints

To access the details about the user's browser fingerprints, navigate to **All** &gt; **Multi-factor Authentication** &gt; **Multi-factor Browser Fingerprints**.

|Field|Description|
|-----|-----------|
|User|The username of the user|
|Browser|The browser that the user used.|
|Browser Fingerprint|The browser fingerprint details.|
|Browser Fingerprint Cookie|The browser fingerprint cookie details.|
|Browser Fingerprint Cookie Expiry|The browser fingerprint cookie expiry details.|

## User recent used factors

To access the details about the user's recently used factors, navigate to **All** &gt; **Multi-factor Authentication** &gt; **User Recent Used Factors**.

|Field|Description|
|-----|-----------|
|User|The username of the user|
|Multi Factor Type|The multi-factor type the user used to log in.|
|Is Recent Factor|The user's recent multi-factor details.|

