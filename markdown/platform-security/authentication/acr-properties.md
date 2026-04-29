---
title: Account recovery properties
description: Use system properties to configure Account Recovery \(ACR\) on your instance.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Account recovery \(ACR\), Multi-Provider SSO configurations, Multi-Provider single sign-on \(SSO\), Authentication, Access Management]
---

# Account recovery properties

Use system properties to configure Account Recovery \(ACR\) on your instance.

Access the account recovery properties on your instance by navigating to **Multi-Provider SSO** &gt; **Account Recovery** &gt; **Properties**.

|Property|Description|
|--------|-----------|
|Enable account recovery feature \[glide.sso.acr.enabled\]|Whether the account recovery feature is enabled on your instance. This property is enabled by default.|
|Enable debug logging for account recovery \[glide.sso.acr.debug.log.enabled\]|Whether your instance includes account recovery information in debug logging. This property is disabled by default.|
|ACR user session timeout \(in minutes\) \[glide.sso.acr.ui.session.timeout\]|Minutes of inactivity before your instance terminates an account recovery user session. This property has a default value of 30.|

