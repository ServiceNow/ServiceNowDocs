---
title: Policy-based login experience
description: The policy-based login experience routes each user to the appropriate authentication method based on administrator-defined policies, using an identifier-first login \(IFL\) flow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/next-gen-login-experience.html
release: brazil
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 5
keywords: [next-generation login experience, identifier first login, IFL, policy-based login, PBLE, authentication]
breadcrumb: [Authentication Console, Authentication, Access Management]
---

# Policy-based login experience

The policy-based login experience routes each user to the appropriate authentication method based on administrator-defined policies, using an identifier-first login \(IFL\) flow.

The policy-based login experience is a framework for personalizing how users sign in. Traditionally, the login page presents every authentication option to every user. The framework replaces that one-size-fits-all page with a routed login: administrator-defined policies decide which authentication method each user is sent to, such as a single sign-on \(SSO\) provider or password-based authentication.

As a framework, the policy-based login experience defines the goal — evaluate policies and route the user — independently of any single implementation. The way that routing is presented to the user can evolve from release to release.

The policy-based login experience introduces an identifier-first login \(IFL\) flow, where an user while accessing the login page, they first enter an identifier such as a username or email address. Instead of presenting every option, the instance evaluates administrator-defined policies and routes each user to the right authentication method — an SSO provider, the local password page, or a password-less flow — without requiring the user to choose.

You manage the policy-based login experience in the Authentication Console. To know more, see [Authentication Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/authentication-console.md).

## Identifier-first login policies

The central object in the experience is the identifier-first login \(IFL\) policy. Each policy maps a set of conditions to an authentication method. After a user enters an identifier, the instance evaluates the active policies and uses the first matching policy to route the user. A policy brings together three things:

-   Conditions — the criteria that determine when the policy applies.
-   Authentication method — where the user is routed when the policy matches.
-   Evaluation order — the priority of the policy relative to other policies.

For more about policies, see IFL policies. For field descriptions used when building a policy, see [IFL policy field reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/ngle-console-field-reference.md).

## How identifier-first login works

The identifier-first login flow operates in the following sequence:

1.  The user navigates to the ServiceNow login page.
2.  The platform evaluates any configured auto-redirect policies based on non-user attributes such as IP address. If a policy matches, the user is redirected immediately.
3.  The user enters their identifier — username or email address.

    **Note:** The identifier can be any `sys_user` field. The user\_name field is available, and the additional field can be configured in the `glide.authenticate.multisso.login_locate.user_field` property. This property is currently available on the SSO properties page.

4.  The platform looks up the identifier in the `sys_user` table and evaluates IFL policies in order of priority.
5.  The first matching policy determines the authentication method:
    -   **SSO login**

        Routes the user to an organization identity provider. Available only when the Multi-Provider SSO plugin is installed and at least one identity provider is configured.

    -   **Password-based authentication**

        Routes the user to log in with a username and password managed within the platform.

6.  If no policy matches, the platform applies fallback logic:
    -   If the user exists in the system, the platform checks for a user-level or company-level SSO source, then the default identity provider.
    -   If the user does not exist, the platform checks for identity providers with auto-provisioning enabled. If one such provider exists, the user is redirected to it. If multiple exist, the user is shown the provider selection page. If none exist, the user is directed to the local password page.

When the user is redirected to an SSO provider, the identifier entered on the IFL page is passed as a `login_hint` query parameter to pre-populate the username field on the provider login page, where supported.

## Traditional login versus identifier-first login

The following table compares the traditional login experience with the identifier-first login experience:

|Traditional login|Identifier-first login|
|-----------------|----------------------|
|All authentication options are shown on the login page.|Only the relevant authentication method is presented, based on the user's identity.|
|Single auto-redirect to one identity provider for the whole instance.|Policy-driven routing supports multiple identity providers across different user personas.|
|User must identify and select the correct login method.|Platform routes the user automatically after identifier entry.|

## Policy conditions

Because the user's identity is known once the identifier is entered, a policy can match on user-context attributes. The console supports the following condition attributes:

-   IP address
-   Role
-   Group

When a policy uses more than one condition, all of the conditions must be met for the policy to match.

## Authentication methods

Each policy specifies the authentication method to apply when the policy matches. The method routes the matched user to one of the following:

-   **SSO login**

    Routes the user to an organization identity provider. Available only when the Multi-Provider SSO plugin is installed and at least one identity provider is configured.

-   **Password-based authentication**

    Routes the user to log in with a username and password managed within the platform.


## Getting started

The policy-based login experience takes effect when it's enabled and at least one active IFL policy exists. To set it up:

1.  Enable the experience in the Authentication Console. See [Activate the policy-based login experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/activate-authentication-console.md).
2.  Create at least one IFL policy. See [Create an IFL policy for password authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/create-ifl-policy-password.md) or [Create an IFL policy for SSO authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/create-ifl-policy-sso.md).

**Note:** Traditional login pages, such as `login.do` and `oauth_login.do`, remain functional and aren't affected by this feature.

## How policies are evaluated

The instance evaluates IFL policies in order and applies the first policy whose conditions match the user. Use the evaluation order to control which policies are checked first. Only active policies participate in evaluation; a deactivated policy is retained but skipped. For a fuller explanation, see [Policy evaluation order](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/policy-evaluation-order.md).

## What happens when no policy matches

If no active policy matches the user, the instance applies the default routing: it uses the user's SSO source or the default identity provider \(IdP\), and falls back to the local login page if no IdP applies. If the instance can't identify the user from the entered identifier, it follows auto-provisioning routing rather than revealing whether the user exists.

