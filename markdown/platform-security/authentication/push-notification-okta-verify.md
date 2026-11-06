---
title: Push notification - Okta Verify
description: The Okta Verify app push notification enables users to securely approve authentication requests directly on their enrolled mobile devices.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/authentication/push-notification-okta-verify.html
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [Okta verify, push notification, MFA, multi-factor authentication, user experience, security, network dependency, device compatibility, ServiceNow]
breadcrumb: [Authentication factor configuration for AI voice agents, Authentication factors, Authentication, Access Management]
---

# Push notification - Okta Verify

The **Okta Verify** app push notification enables users to securely approve authentication requests directly on their enrolled mobile devices.

During authentication, users receive a push notification through the **Okta Verify** app, enabling them to review request details and approve access without manually entering a verification code.

## Use case

**Okta Verify** push notification is a second factor option for ServiceNow AI Platform authentication flows, providing additional security. Push notification - Okta Verify factor can also be used for step-up authentication. For more information, see [Step-up authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/authentication/step-up-authentication.md).

## Key strengths

The **Okta Verify** push notification method offers the following advantages:

-   Users approve authentication without entering a verification code.
-   Resilient against various attack vectors, reinforcing the authentication process.

## Important considerations

While **Okta Verify** push notification is a secure and convenient authentication method, there are few considerations to keep in mind:

-   Connectivity: requires a reliable internet connection and a compatible mobile device.
-   User Vigilance: Users should carefully review each authentication prompt to help prevent unintended approvals.
-   Device Security: Registered devices must be protected with screen locks or biometric safeguards to help prevent unauthorized access.
-   Device Re-enrollment: If a device is replaced or reset, users must re-enroll to maintain uninterrupted authentication.

**Okta Verify** push notification enhances organizational security while providing an authentication experience. For detailed configuration instructions, see [Configure Push notification - Okta Verify](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/authentication/configure-okta-verify-push-notification.md).

