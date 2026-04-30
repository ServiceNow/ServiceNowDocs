---
title: Adaptive Authentication for Trusted Mobile Apps
description: Access your ServiceNow from untrusted networks by using the Now Mobile app.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Adaptive authentication, Authentication, Access Management]
---

# Adaptive Authentication for Trusted Mobile Apps

Access your ServiceNow from untrusted networks by using the Now Mobile app.

Adaptive Authentication for Trusted Mobile Apps

Adaptive Authentication for Trusted Mobile Apps enables users to access the ServiceNow instance using the Now Mobile app. The instance is protected behind a trusted IP network boundary.

The following are some of the scenarios where you need access to the instance while you are outside your network.

As an employee, you require access the Now Mobile app and Employee Service Center \(portal\) from outside the network. The Trusted mobile app filter enables you to identify the incoming request originating from a trusted Now Mobile app that is linked to a user account.

As an admin, you can configure the policy. The policy enables users to register their mobile devices and access the instance on a trusted network.

As a user, you can register your mobile device by scanning the QR displayed on the instance. After the registration, you can log in to your instance from the Now Mobile app, using your credentials.

**Note:** To register the mobile device, you must be on a trusted network. After the registration, you can log in to the instance from other networks as well.

## Features

As an admin, you can use the following features:

-   Configure policies by using trusted app filter criteria.
-   Create policy conditions with a new filter criteria for trusted mobile apps.
-   Support all login methods on the trusted mobile app for the users \(Local login, SAML, OIDC, and MFA\).
-   Revoke a trusted device.
-   Add security events for all device registration or revocation actions. The events can be used to notify the user.
-   Support security events for signature failures, cookie validation failures, invalid tokens, invalid headers, or query parameters.
-   Control the maximum number of registered devices.
-   Prevent a new device registration, unless the user removes an existing-paired device.
-   Capture the last time that a device was used.

