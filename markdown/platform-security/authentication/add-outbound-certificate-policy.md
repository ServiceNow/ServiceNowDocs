---
title: Add an outbound certificate policy
description: Add an outbound certificate policy to control how the instance validates a specific domain's SSL/TLS certificate's on outbound connections, adjusting individual validation checks for that domain.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/add-outbound-certificate-policy.html
release: brazil
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-09-24"
reading_time_minutes: 2
keywords: [outbound certificate policy, certificate validation, SSL, TLS]
breadcrumb: [Outbound certificate policies, Authentication, Access Management]
---

# Add an outbound certificate policy

Add an outbound certificate policy to control how the instance validates a specific domain's SSL/TLS certificate's on outbound connections, adjusting individual validation checks for that domain.

## Before you begin

Role required: `outbound_http_request_admin` or `admin`

The feature is enabled. A policy has no effect until the `com.glide.communications.httpclient.outbound_cert_policy.enabled` property is set to `true`.

## About this task

An outbound certificate policy overrides the global SSL/TLS validation settings for a single domain. domains without a policy continue to use the global settings.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Outbound HTTPS Security Policies**.

    The Outbound Certificate Policies table opens.

2.  Select **New**.

3.  In the **Name** field, enter the domain the policy applies to.

    Enter an exact domain, such as `www.api.partner.com`, or a wildcard pattern, such as `*.partner.com`. A wildcard must contain at least two domain components; overly broad patterns such as a bare `*` or `*.com` are rejected when you save. When an outbound connection is made, the instance applies the most specific matching policy: an exact-domain policy takes priority over a wildcard policy, and a domain with no matching policy falls back to the global validation settings.

4.  Set the three validation checks for the domain.

    Each check is enabled by default; clear a check to skip it for this domain. These three fields control how the instance validates the domain's certificate on outbound connections. Leaving a check enabled enforces it; clearing a check skips it for the domain, which lowers the protection for connections to that domain.

    -   **Hostname verification**

        Validates that the domain's certificate was issued for the domain being connected to. When cleared, the instance accepts a certificate whose hostname does not match the domain. Clear this check only when a domain presents a certificate with a mismatched hostname that you have confirmed is safe.

    -   **Certificate chain validation**

        Validates the domain's certificate chain against the platform trust store. When cleared, the instance accepts a certificate whose chain can't be validated. Clear this check only for a domain whose chain can't be validated by design — for example, a self-signed certificate in a development environment.

    -   **Revocation check \(OCSP/CRL\)**

        Verifies the domain's certificate has not been revoked, using OCSP or a certificate revocation list. When cleared, the instance does not check revocation status. Clear this check only when revocation status can't be retrieved and you have confirmed the certificate is valid.

5.  Select **Submit**.


## Result

Outbound connections to the domain now use the validation checks defined in the policy instead of the global settings. To change which checks a domain skips, open its policy and update the checks. To return a domain to the global settings, delete its policy.

## What to do next

A policy changes certificate validation for the domain across all outbound connection types that the instance makes to that domain, including:

-   REST messages — the policy applies to the outbound HTTP and HTTPS requests the message makes.
-   SOAP messages — the policy applies to the SOAP endpoint's certificate validation.
-   REST and SOAP steps in Flow Designer.
-   Synchronous and asynchronous HTTP client calls.

Review any integrations that connect to the domain to confirm the change in validation behavior is expected. Clearing a check affects every outbound connection to the domain, not only the integration you created the policy for.

