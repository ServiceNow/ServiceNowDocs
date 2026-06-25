---
title: Mobile access to IP-restricted networks
description: Enable ServiceNow mobile apps to access IP-restricted networks when adaptive authentication is activated on your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/mobile/mob-access-ip-restrictd-netwrks.html
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Mobile authentication, Configuring the Mobile Platform, Mobile Platform]
---

# Mobile access to IP-restricted networks

Enable ServiceNow mobile apps to access IP-restricted networks when adaptive authentication is activated on your instance.

The adaptive authentication policy framework enforces contextual authentication controls on your ServiceNow instance. For example, administrators can configure policies to allow logins from users only within a trusted range of IP addresses and who are members of a specific role. For more information, see Adaptive authentication.

When adaptive authentication is activated and configured on your ServiceNow instance, mobile users must install a separate VPN app on their device to access the instance. To avoid having to install the separate VPN app, you can configure your ServiceNow instance to grant access to mobile users by using the system properties that are described in [Adaptive authentication for mobile apps system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/mobile/adapt-auth-mob-apps-sys-props.md).

