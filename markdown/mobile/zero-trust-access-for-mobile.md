---
title: Securing your ServiceNow mobile instance with Zero Trust Access
description: Limit end-user access to your ServiceNow instance by opting in to Zero Trust Access. This adjusts user roles and permissions according to security policies defined by the admin based on factors such as IP address, location, and identity provider attributes.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Mobile authentication, Configuring the Mobile Platform, Mobile Platform]
---

# Securing your ServiceNow mobile instance with Zero Trust Access

Limit end-user access to your ServiceNow® instance by opting in to Zero Trust Access. This adjusts user roles and permissions according to security policies defined by the admin based on factors such as IP address, location, and identity provider attributes.

Session states can either be relegated with limited user access or restored with full user access. If a user’s mobile session when logging in to their mobile app meets the security policy conditions set by Zero Trust Access, a banner appears that explains that the user’s access may be limited. This can help protect against unauthorized access and data breaches, even when high-privileged users access applications from untrusted devices or locations.

For more information, see [Zero Trust Access](https://www.servicenow.com/docs/access?context=session-access&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

![Banner notifying the user that their access may be limited because they are not on a trusted network.](../image/mobile-zero-trust-access.png)

