---
title: Disable password-less authentication
description: Use the glide.login.no\_blank\_password property to prevent users from logging into the NOW platform with blank passwords, or by leaving the Password field empty.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Disable password-less authentication

Use the **glide.login.no\_blank\_password** property to prevent users from logging into the NOW platform with blank passwords, or by leaving the **Password** field empty.

Even if the admin purposefully assigns an empty value or blank password in user records, a user can't log in without providing a value in the **Password** field.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**glide.login.no\_blank\_password**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Configure in Instance Security Center|Yes|
|Purpose|To ensure strong authentication as sometimes the username are easy to guess within an organization.|
|Recommended value|true|
|Functional impact|Operations should not use blank passwords because it is viewed as a critical security risk. However, if there is a valid case for such usage, there is a possibility of an outage. Users with blank passwords wouldn't be able to log in to the instance.|
|Security risk|\(High\) An attacker is able to log in to the instance with the default usernames, or by specific individual/group \(usually firstname.lastname\) without any password. Doing so is viewed as a critical security risk, because it would enable a public user to violate the confidentiality and integrity of the instance data.|

**Parent Topic:**[Authentication](sc-authentication.md)

