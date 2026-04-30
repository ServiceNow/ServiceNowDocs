---
title: Session Access Audits
description: The Session Access Audits displays the Session Access logs and information related to a user's session.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Zero Trust Access system properties, Zero Trust Access, Access Management]
---

# Session Access Audits

The Session Access Audits displays the Session Access logs and information related to a user's session.

## Audits

The Session Access audit displays audit information as follows:

**Note:** Use the `glide.authenticate.session_access.log_audit_event` property to populate the audit information.

![Session Access Audits](../images/session-access-audit.png)

|Field|Description|
|-----|-----------|
|User|Details of the user.|
|Session ID|Details about the session displayed as a unique ID.|
|Mobile Client|The mobile client details. **ServiceNow Agent** \(Now Agent\) and **ServiceNow Request** \(Now Mobile\).|
|Session Access Policies Applied|The Session Access policy that is applied.|
|Roles to Remove|Roles that were removed from the user while logging.|
|Limit To Roles|Roles that were limited to the user while logging.|
|Group List to Remove Roles|Information about the group that has removed roles for the user.|
|Group List to Limit Roles|Information about the group that has limited roles for the user.|
|Mobile Client|Details of the user logged-in through mobile with reduced or removed access.|
|IDP Attribute|The IDP that was used for that session.|
|IP Address|Details of the IP address used by the user to log in.|
|Created|Details of the created user record's date and time.|

