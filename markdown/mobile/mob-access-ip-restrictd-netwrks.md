---
title: Mobile access to IP-restricted networks
description: Enable ServiceNow mobile apps to access IP-restricted networks when adaptive authentication is activated on your instance.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Mobile authentication, Configuring the Mobile Platform, Mobile Platform]
---

# Mobile access to IP-restricted networks

Enable ServiceNow mobile apps to access IP-restricted networks when adaptive authentication is activated on your instance.

The adaptive authentication policy framework enforces contextual authentication controls on your ServiceNow instance. For example, administrators can configure policies to allow logins from users only within a trusted range of IP addresses and who are members of a specific role. For more information, see [Adaptive authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/adaptive-authentication.md).

When adaptive authentication is activated and configured on your ServiceNow instance, mobile users must install a separate VPN app on their device to access the instance. To avoid having to install the separate VPN app, you can configure your ServiceNow instance to grant access to mobile users by using the system properties that are described in [Adaptive authentication for mobile apps system properties](../reference/adapt-auth-mob-apps-sys-props.md).

-   **[Configure mobile access for IP-restricted networks](../task/config-mob-acc-iprstrctd-ntwrks.md)**  
Configure mobile access to ServiceNow instances that use adaptive authentication, which restricts access outside a defined IP address range.

**Parent Topic:**[Mobile authentication](mobile-authentication.md)

