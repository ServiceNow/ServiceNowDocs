---
title: Reset Multi-factor Authentication \(MFA\) for users
description: Administrators can reset MFA for users who deleted the app, lost access to the device, or have no alternative MFA associated with their device.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure MFA, Multi-factor authentication, Authentication, Access Management]
---

# Reset Multi-factor Authentication \(MFA\) for users

Administrators can reset MFA for users who deleted the app, lost access to the device, or have no alternative MFA associated with their device.

## Before you begin

Role required: admin

The following procedure describes how a ServiceNow® administrator can reset the MFA validation to unblock users and enable them to re-register MFA.

## Procedure

1.  Navigate to **All** &gt; **Multi-factor Authentication** &gt; **User Multi-factor Setup**.

2.  Search for the user that you want to unblock.

3.  Set the Validate to **false**.

4.  Navigate to **All** &gt; **Multi-factor Authentication** &gt; **Web Authentication** &gt; **User Public Credentials \(sys\_user\_public\_credential**.

5.  Search for the user that you want to unblock.

6.  Delete all the records for this user.

7.  Navigate to **All** &gt; **Multi-factor Authentication** &gt; **User Recent User Factors**.

8.  Search for the same user.

9.  Delete all the records for this user.


## Result

When the unblocked user enters the credentials and logs in, the **Enable multi-factor authentication \(MFA\)** page is displayed. The user can follow the steps on the page to re-register MFA.

