---
title: Managing unlock timeout after failed logins \[Updated in Security Center 1.3\]
description: Two script actions are available that enable a site administrator to manage the number of times a user can provide an incorrect password before being locked out from the ServiceNow AI Platform. You can enable either of these script actions to manage failed login attempts.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-02-01"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Managing unlock timeout after failed logins \[Updated in Security Center 1.3\]

Two script actions are available that enable a site administrator to manage the number of times a user can provide an incorrect password before being locked out from the ServiceNow AI Platform. You can enable either of these script actions to manage failed login attempts.

## More information

|Attribute|Description|
|---------|-----------|
|Property/Plugin Name|N/A|
|Configuration type|System Policy &gt; Script Actions|
|Category|[Authentication](sc-authentication.md)|
|Purpose|To enforce strict policy for failed login attempts to avoid brute forcing of credentials.|
|Recommended value|Active|
|Security risk rating|7.3|
|Functional Impact|This remediation would enable administrator of the instance to monitor and report any malicious user access. No functionality impact, only User experience change.|
|Security risk|\(Moderate\) Apply a defined logging and auditing strategy so that you can identify and act on suspicious activity in a timely manner.|

## Steps to configure

1.  Navigate to **System Policy** &gt; **Script Actions.**
2.  Search for the name **\*SNC User**.
3.  To enable management of failed login attempts, change the Active state of either the **SNC User Lockout Check with Auto Unlock** or **SNC User Lockout Check** scripts actions from **false** to **true**.
4.  To reset the failed login counter after a successful login, you can activate the **SNC User Clear** script action.

**Parent Topic:**[Authentication](sc-authentication.md)

