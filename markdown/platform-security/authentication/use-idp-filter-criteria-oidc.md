---
title: Use Identity Provider Attribute as Filter Criteria for OIDC
description: Use the Identity Provider \(IDP\) attribute from the OpenID Connect \(OIDC\) response as a filter criteria for authentication policy.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/authentication/use-idp-filter-criteria-oidc.html
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Attributes for OIDC, Identity Provider Attributes Filter, Filter criteria, Adaptive authentication, Authentication, Access Management]
---

# Use Identity Provider Attribute as Filter Criteria for OIDC

Use the Identity Provider \(IDP\) attribute from the OpenID Connect \(OIDC\) response as a filter criteria for authentication policy.

## Before you begin

Role required: admin

You can create session access policy using policy context \(Pre-Authentication, Post Authentication, multi-factor authentication\) and filter criteria \(Role, Group, IP, Location\) with policy inputs and conditions.

The following procedure shows steps to configure the IdP attribute from the SAML response as a policy input to control authentication in the **Post Authentication Context**, **Multi-factor authentication \(MFA\) Context**, and **Zero Trust - Policy based session access**.

The Okta IDP attributes are as displayed in the following screen shot. You should set the Use in Adaptive Authentication as true to use it in the **Post Authentication Context**, **Multi-factor authentication \(MFA\) Context**, and **Zero Trust - Policy based session access** policies.

**Note:** Policies in the post-authorization, MFA, Zero Trust - Policy based session access execute after the users enter the credentials or SSO response.

## Procedure

1.  Use of IDP attribute in Post Authentication Policy Context.

    Example: Configuring to enable log in from the Okta IDP attributes if the device is trusted.

    1.  Navigate to **All** &gt; **Adaptive Authentication** &gt; **Auth Policy Contexts** &gt; **Post Authentication Policy Context.**.

    2.  Select **Allow Policy** and open the policy record.

    3.  In the Policy Input, create the Policy Input and Policy Condition.

        -   **Policy Input**: Add **Risk Factor**.

            \[Omitted image "post-auth-idp.png"\] Alt text: Allow Policy - Post authentication

        -   **Policy Conditions**: **Risk Factor** greater than `5` and **Authentication Scheme** is `Single Sing-On`.

            \[Omitted image "input-idp-condition.png"\] Alt text: Policy input condition

        Based on this configuration, when the device is trusted from the Okta \(IdP\), then the user is authenticated to the instance.

        For more information on how to create Post Authentication Context with Policy and Condition, see [Post-authentication context](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/authentication/post-auth-context.md).

2.  Use of IDP attribute in MFA Policy Context.

    Example: Configuring to enable MFA from the Okta IDP attributes if the device isn’t trusted.

    1.  Navigate to **All** &gt; **Adaptive Authentication** &gt; **Auth Policy Contexts** &gt; **MFA Authentication Policy Context.**.

    2.  In the Policy Input, create the Policy Input and Policy Condition.

        -   **Policy Input**: Add **Risk Factor**.

            \[Omitted image "input-idp.png"\] Alt text: Policy input

        -   **Policy Conditions**: **Risk Factor** greater than `5` and **Authentication Scheme** is `Single Sing-On`.

            \[Omitted image "mfa-idp-filter.png"\] Alt text: MFA IDP Filter condition

        Based on this configuration, when the device is not-trusted from the Okta \(IdP\), then the user shown a second factor authentication to log in to the instance.

        For more information on how to create MFA Context with Policy and Condition, see [Multi-factor Authentication context](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/authentication/mfa-auth-context.md).

3.  Use of IDP attribute in Zero Trust - Policy based session access.

    Example: Configuring to reduce the privilege of `Itil` role from Okta IDP attributes if the device isn’t trusted.

    1.  Navigate to **All** &gt; **Zero Trust Access** &gt; **Session Access Role Configurations**.

    2.  Create a Session Access role configuration.

    3.  In the Policy Input, create the Policy Input and Policy Condition.

        -   **Policy Input**: Add **Risk Factor** and **Has itil role**.

            \[Omitted image "zta-idp-filter-input.png"\] Alt text: Session Access - IDP Filter

        -   **Policy Conditions**: **Risk Factor** greater than `5` and **Authentication Scheme** is `Single Sing-On`.

            \[Omitted image "zta-idp-filter-condition.png"\] Alt text: Session Access - IDP condition

        Based on this configuration, when the `itil` user using a device that is not-trusted from the Okta \(IdP\), then the user's privileges are reduced for the logged in session.

        For more information on how to create Zero Trust - Policy based session access with Policy and Condition, see [Zero Trust Access \(ZTA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/session-access.md).


