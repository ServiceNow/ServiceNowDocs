---
title: Exploring Continuous Authentication
description: ServiceNow's continuous authentication \(CA\) enables you to re-verify and authenticate a user if they access resources that are protected by you.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [CA, Continuous authentication, continuous auth, zero trust access, ZTA]
breadcrumb: [Continuous Authentication \(CA\), Zero Trust Access, Access Management]
---

# Exploring Continuous Authentication

ServiceNow's continuous authentication \(CA\) enables you to re-verify and authenticate a user if they access resources that are protected by you.

ServiceNow's continuous authentication is a security mechanism designed to verify a user's identity not just at the initial login, but throughout the user's entire session. CA is built on ServiceNow's zero trust access security architecture that aims to enhance security by ensuring that the user remains who they claim to be, even after the initial authentication process.

CA works on the following zero trust access principles:

-   **Verify explicitly**: No implicit trust for any user, device, or system within a network, regardless of location. Every user and device must be explicitly authenticated and authorized, regardless of location or past access.
-   **Use least privilege access**: Grant only the minimum access or permissions needed to perform specific tasks and limit potential damage from compromised accounts or systems."
-   **Assume breach**: Instead of relying only on prevention, assume breach and focus on proactive detection, containment, and response.

CA provides the ability to enforce step-up authentication or re-authentication based on the data users are accessing and activities they are performing​. It be opted by administrators for creating security policies at a table or data class level.

You can enforce step-up authentication \(MFA\) or re-authentication \(SSO - SAML or OIDC\) within a logged-in session whenever there is an attempt by the user to access Personally Identifiable Information \(PII\) and sensitive data.

**Note:** You must install the **Zero Trust - Continuous Authentication** \(`com.snc.zero_trust_continuous_authentication`\) for opting CA which requires a license.

## Benefits

Following are the some of the benefits of using CA:

-   **Enhanced Security**: By continuously verifying the user's identity, the system can detect and respond to potential security threats more quickly.
-   **Reduced Risk of Account Takeover**: Even if an attacker gains access to a user's session, continuous authentication can help prevent them from accessing confidential data.

## Use cases

Following are some of the use cases for using CA:

-   Enforce re-authentication before allowing access to sensitive data using different policies.
-   Enforce periodic re-authentication or step-up authentication using different policies:
    -   Use re-authentication that can include IdP's MFA, IdP's SSO.
    -   Use step up authentication with ServiceNow's MFA.

## Roles in CA

CA has the following roles:

-   CA Admin \(ca\_admin\): Ability to create, edit, and view CA policies. Configure CA properties and view dashboards \(Metrics\) of CA.
-   Policy Admin \(ca\_policy\_admin\): Ability to create, edit, and view CA policies..
-   Auditor \(ca\_auditor\): Ability to view dashboards \(Metrics\) of CA. And policies, and logs of CA.

To configure CA you must elevate your role to **ca\_admin** and perform the policy configurations.

**Note:** All these 3 roles are elevated roles.

## Modules in CA

Following are the different modules within CA:

-   [Policies](ca-policies.md): View the different continuous authentication policies that are created.
-   [Metrics](ca-metrics.md): View the different metrics for continuous authentication for KPI purposes and understand the usage of CA within your organization.
-   [System Properties](ca-system-properties.md): Use system properties to enable and customize continuous authentication \(CA\) to meet your zero trust access security requirements.

**Related topics**  


[Policies](ca-policies.md)

[Metrics](ca-metrics.md)

[System properties](ca-system-properties.md)

[Pre-work for Continuous Authentication](pre-work-ca.md)

[Activating Continuous Authentication](../task/activate-continuous-authentication.md)

[Configuring Continuous Authentication](../task/configure-ca.md)

[High Assurance session with Continuous Authentication](high-assurance-ca.md)

