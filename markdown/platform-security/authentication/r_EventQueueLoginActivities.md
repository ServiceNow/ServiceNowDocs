---
title: Monitor the event queue for login activities
description: Every single sign-on integration creates events for login activities.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [SAML 2.0 troubleshooting, SAML, Multi-Provider single sign-on \(SSO\), Authentication, Access Management]
---

# Monitor the event queue for login activities

Every single sign-on integration creates events for login activities.

You can use these events to monitor for login failures and determine if there are any security concerns to address.

|Event Name|Description|Record|Parameter 1|Parameter 2|
|----------|-----------|------|-----------|-----------|
|**external.authentication.succeeded**|External authentication succeeded and the user accessed the instance URL.|Session ID|User ID of user who successfully logged in|The URL the user accessed \(which may be a deep link\)|
|**external.authentication.failed**|The single sign-on requirements are not present or are missing.| |Session ID|The missing authentication requirements|
|**external.authentication.failed**|The user does not exist in the User `[sys_user]` table| |User ID|The string, "User does not exist"|
|**external.authentication.failed**|The user is locked out.| |User ID|The string, "User locked out."|

