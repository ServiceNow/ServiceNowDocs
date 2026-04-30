---
title: Enterprise mobility management \(EMM\)
description: Use an EMM suite to distribute ServiceNow mobile apps or the ServiceNow Classic mobile app.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring the Mobile Platform, Mobile Platform]
---

# Enterprise mobility management \(EMM\)

Use an EMM suite to distribute ServiceNow mobile apps or the ServiceNow Classic mobile app.

## Enterprise mobility management \(EMM\)

Apply your corporate app protection policies to ServiceNow mobile apps by either using your EMM suite, or, with an embedded mobile application management \(MAM\) SDK for personal devices. ServiceNow only supports Intune and BlackBerry SDKs.

## AppConfig

AppConfig is a standard approach for configuring mobile apps using key-value pairs. AppConfig was created by leading EMM providers like MobileIron, SAP, IBM, and VMWare. For more information on application configuration, please read your MDM product documentation. ServiceNow supports two app configurations:

-   Pre-configure the default instance
-   Change the default browser

For details on these configurations, see [AppConfig for Mobile Apps](../reference/appconfig.md).

## Mobile application management \(MAM\) integration

Use Microsoft Intune or BlackBerry Dynamics to secure and protect sensitive information in mobile applications, even in cases where customers use their own mobile devices. For more detail on MAM integration, see [Mobile application management \(MAM\) integration](sg-mam.md).

## Unsupported MDM/MAM features

The following MDM and MAM features are not supported by ServiceNow.

-   Application distribution
-   App protection policies
-   GA \(general availability\) binary files \(ipa and apk\) will not be distributed.
-   App wrapping and/or resigning are not allowed.
-   Troubleshooting mobile gateway or proxy rules.
-   App Config is supported for on-prem MDM but creating plist file is not supported.

