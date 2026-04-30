---
title: Push notification - Okta Verify
description: The Okta Verify app push notification enables users to securely approve authentication requests directly on their enrolled mobile devices.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-11-13"
reading_time_minutes: 1
keywords: [Okta verify, push notification, MFA, multi-factor authentication, user experience, security, network dependency, device compatibility, ServiceNow]
breadcrumb: [Configure authentication factors, Authentication factors, Authentication, Access Management]
---

# Push notification - Okta Verify

The **Okta Verify** app push notification enables users to securely approve authentication requests directly on their enrolled mobile devices.

During authentication, users receive a push notification via the **Okta Verify** app, enabling them to review request details and approve access without manually entering a verification code.

## Use case

**Okta Verify** push notification is recommended as a robust and convenient second factor for ServiceNow AI Platform authentication flows, providing enhanced security and a seamless user experience.

## Key strengths

The **Okta Verify** push notification method offers the following advantages:

-   A streamlined process enables quick and easy authentication.
-   Resilient against various attack vectors, reinforcing the authentication process.

## Important considerations

While **Okta Verify** push notification is a secure and convenient authentication method, there are few considerations to keep in mind:

-   Connectivity: Requires a reliable internet connection and a compatible mobile device.
-   User Vigilance: Users should carefully review each authentication prompt to help prevent unintended approvals.
-   Device Security: Registered devices must be protected with screen locks or biometric safeguards to help prevent unauthorized access.
-   Device Re-enrollment: If a device is replaced or reset, users must re-enroll to maintain uninterrupted authentication.

**Okta Verify** push notification enhances organizational security while providing a convenient authentication experience. For detailed configuration instructions, see [Configure push notification \(Okta Verify\)](../task/configure-okta-verify-push-notification.md).

