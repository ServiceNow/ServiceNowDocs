---
title: Outbound certificate policies
description: Outbound certificate policies let you control how the instance validates a specific domain's \(FQDN\)\) SSL/TLS certificate on outbound connections. Use these policies instead of applying global validation settings to every host.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/outbound-certificate-policies.html
release: brazil
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-09-24"
reading_time_minutes: 3
keywords: [outbound certificate policy, certificate validation, SSL, TLS, wildcard, domain separation]
breadcrumb: [Authentication, Access Management]
---

# Outbound certificate policies

Outbound certificate policies let you control how the instance validates a specific domain's \(FQDN\)\) SSL/TLS certificate on outbound connections. Use these policies instead of applying global validation settings to every host.

By default, the instance validates a domain's SSL/TLS certificate the same way for every outbound connection, using global validation settings. An outbound certificate policy lets you change that behavior for a single domain. For example, you can skip a specific validation check for a domain with a known certificate issue while every other domain keeps the global settings.

Each policy controls three validation checks for the domain it applies to:

-   Hostname verification
-   Certificate chain validation
-   Revocation checking \(OCSP/CRL\)

**Note:**

-   All three are enabled by default, so a policy is secure by default.
-   Outbound certificate policies are opt-in Feature and is inactive by default. The REST/SOAP calls with mTLS functionality aren't affected.
-   Each endpoint/host can have only one active Outbound certificate policy on the instance. If a policy already exists for the host, update it as needed instead of creating a duplicate policy in a different scope.

Managing policies requires the `outbound_http_request_admin` role, and policies take effect only when the `com.glide.communications.httpclient.outbound_cert_policy.enabled` property is set to `true`.

## How a policy is matched to a domain

When the instance makes an outbound connection, it resolves the certificate policy for the domain using a three-tier, fallback-aware lookup. Here are the matching scenarios:

|Scenario|Behavior|
|--------|--------|
|Exact match|A policy whose pattern exactly matches the domain \(for example, `www.api.partner.com`\) takes priority.|
|Wildcard match|If no exact match exists, a wildcard policy \(for example, `*.partner.com`\) applies. Selects the most specific matching.|
|Global fallback|If no policy matches the domain, the instance uses the global validation settings.|

Because domains without a matching policy fall back to the global settings, existing connections are unaffected until you add a policy for a domain.

## Integrations affected by a policy

An outbound certificate policy changes certificate validation for every outbound connection the instance makes to the matching domain — not only the integration you created the policy for. When a policy relaxes a check, all of the following outbound connection types to that domain use the relaxed validation. When a policy enforces a check, they all enforce it:

-   REST messages — the policy applies to the outbound HTTP and HTTPS requests the message makes.
-   SOAP messages — the policy applies to the SOAP endpoint's certificate validation.
-   REST and SOAP steps in Flow Designer.
-   Synchronous and asynchronous HTTP client calls.

**Note:**

-   The REST/SOAP calls with mTLS aren't affected - Synchronous and asynchronous calls via internal HTTP client aren't affected.
-   Any calls via mid server aren't affected.

Before you create or change a policy, review the integrations that connect to the domain so that the change in validation behavior is expected across all of them.

## Wild card patterns

A policy pattern can use a wildcard to apply to all sub-domains of a domain — for example, `*.partner.com`. To prevent a single policy from weakening validation across too many domains, the instance rejects overly broad wildcard patterns when you save a policy:

-   A bare wildcard \(`*`\) and a top-level wildcard \(`*.com`\) are rejected.
-   A wildcard pattern must contain at least two domain components — for example, `*.partner.com`.

These constraints prevent an instance-wide validation bypass through a single overly broad pattern.

## Security considerations

Turning off a validation check for a domain reduces the protection that SSL/TLS validation provides for connections to that domain. Use outbound certificate policies deliberately:

-   Turn off only the specific checks a domain requires, and leave the others enabled. A policy is secure by default — every check starts enabled.
-   Use the most specific pattern that solves the problem. Prefer an exact domain over a wildcard.
-   Treat a relaxed check as a temporary measure while a domain's certificate issue is resolved, and review your policies regularly.
-   Restrict who can create and change policies — requires the `outbound_http_request_admin` or `admin` role.

## Known limitation

When creating an Outbound certificate policy for a host in the UI, you can create multiple policies for the same host across different scopes. However, the system applies only the first policy created for that domain. To avoid confusion, update the existing policy if changes are needed instead of creating a new one.

