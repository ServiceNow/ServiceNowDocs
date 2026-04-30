---
title: Certificate-based authentication
description: Certificate-based authentication lets you mutually authenticate user logins or inbound API requests using certificates from a trusted Certificate Authority \(CA\).
locale: en-US
release: xanadu
product: Certificate-based Authentication
classification: certificate-based-authentication
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Authentication, Access Management]
---

# Certificate-based authentication

Certificate-based authentication lets you mutually authenticate user logins or inbound API requests using certificates from a trusted Certificate Authority \(CA\).

**Note:** Certificate Based Authentication is not supported on the On-Prem and edge encryption enabled instance.

-   **Certificate-based authentication for user interface logins**

    Enable end users to use PIV \(Personal Identity Verification\) or CAC \(Common Access Card\) cards to log in to the ServiceNow AI Platform or Service Portal instead of using a user name and password. To set up mutual authentication for user interface logins, see [Set up Certificate-based authentication](../task/set-up-mutual-auth.md#).

    After Certificate-based authentication is set up, end users can finalize their set up and log in. See [Log in using Certificate-based authentication](../task/ui-login-mutual-auth.md#).

-   **Certificate-based authentication for Inbound web services**

    Authenticate inbound requests to ServiceNow SOAP and REST APIs. To set up mutual authentication for inbound web services, see [Set up Certificate-based authentication](../task/set-up-mutual-auth.md#).


