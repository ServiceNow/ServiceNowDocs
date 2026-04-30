---
title: Event queue login events
description: The SAML 2.0 integration creates events for login activities.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [SAML 2.0 troubleshooting, SAML, Multi-Provider Single sign-on \(SSO\), Authentication, Access Management]
---

# Event queue login events

The SAML 2.0 integration creates events for login activities.

You can use these events to monitor for login failures and determine if there are any security concerns to address.

|Event name|Description|ID used with event|Event string|
|----------|-----------|------------------|------------|
|saml2.logout.validation.failed|The logout response from the IdP failed validation against your logout request. The event validates the &lt;inResponseTo&gt; element against the session ID \(ID attribute of the &lt;saml2p:LogoutRequest&gt; element\). For example, see the workflow for logout request issued.|Session ID|The string, "SAML2 LogoutResponse validation failed.'|
|external.authentication.succeeded|External authentication successed.| |The string, 'Authentication Successed'|
|external.authentication.succeeded|External authentication succeeded and the user accessed the instance URL.|Session ID &amp; User ID of user who successfully logged in|The URL the user accessed \(which may be a deep link\)|
|external.authentication.failed|The single sign-on requirements are not present or are missing.|Session ID|The missing authentication requirements|
|external.authentication.failed|The user does not exist in the User \[sys\_user\] table.|User ID|The string, 'User does not exist'|
|external.authentication.failed|The user is locked out.|User ID|The string, 'User locked out'|

