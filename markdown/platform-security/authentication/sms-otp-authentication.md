---
title: SMS One-time passcode \(OTP\) authentication
description: SMS one-time password \(OTP\) authentication is a method used to verify user identity by sending a temporary, numeric code to the user's registered mobile number. The user enters this code to complete authentication.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-11-13"
reading_time_minutes: 1
keywords: [SMS One-time Passcode, OTP, authentication, ServiceNow, secondary factor, identity verification, medium-risk scenarios, SIM-swapping, interception, delays, mobile network availability]
breadcrumb: [Configure authentication factors, Authentication factors, Authentication, Access Management]
---

# SMS One-time passcode \(OTP\) authentication

SMS one-time password \(OTP\) authentication is a method used to verify user identity by sending a temporary, numeric code to the user's registered mobile number. The user enters this code to complete authentication.

## Use case

-   Serves as a secondary authentication factor, particularly for users without authenticator apps.
-   Recommended for medium-risk scenarios, such as verifying changes to profile information and approving login attempts.

## Key strengths

The SMS OTP method offers the following advantages:

-   Familiar and easy for users to adopt
-   No additional app installation required
-   Simple to deploy and integrate

## Important considerations

While SMS method is a convenient authentication method, there are several considerations to keep in mind:

-   Vulnerable to SIM-swapping, interception, and delivery delays.
-   Reliant on mobile network availability.
-   Not recommended as the sole authentication factor for high-risk or sensitive operations.

SMS OTP can enhance overall security when used appropriately. For detailed configuration instructions, see [Multi-factor authentication Providers](multi-factor-authentication-providers.md).

