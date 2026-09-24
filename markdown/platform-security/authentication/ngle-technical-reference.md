---
title: Policy-based login experience technical reference
description: System properties, affected login routes, policy conditions, authentication methods, and fallback behavior for the next-generation login experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/ngle-technical-reference.html
release: brazil
product: Authentication
classification: authentication
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 1
keywords: [NGLE technical reference, login routes, policy\_based\_login\_experience.enabled]
breadcrumb: [IFL policy field reference, Authentication Console, Authentication, Access Management]
---

# Policy-based login experience technical reference

System properties, affected login routes, policy conditions, authentication methods, and fallback behavior for the next-generation login experience.

## System properties

|Property|Description|Default|
|--------|-----------|-------|
|Enable policy-based login `glide.authenticate.policy_based_login_experience.enabled`|Enables the policy-based login experience. The identifier-first login flow takes effect when this property is enabled and at least one active IFL policy exists.|false|

## Affected login routes

Traditional login pages, such as `login.do` and `oauth_login.do`, remain functional and aren't affected.

**Note:** Enabling the identifier-first login flow for the ServiceNow AI Platform login page does not affect Service Portal login unless the portal is explicitly configured to use it. To know more, see [Enable identifier-first login in Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/identifier-first-login-service-portal.md).

## Policy conditions

IFL policies support the following user-context conditions. When a policy has multiple conditions, all conditions must be met for the policy to match.

-   IP address
-   Role
-   Group

## Fallback sequence

If no IFL policy matches, the instance applies the default routing in this order:

1.  Default SSO routing, using the user's SSO source or the default identity provider \(IdP\).
2.  If no IdP applies, the local login page.

If the instance can't identify the user from the entered identifier, it follows the auto-provisioning routing: if a single IdP supports auto-provisioning, the user is routed to that IdP; if multiple IdPs apply, an IdP selection page is shown; if none apply, the password page is shown to avoid revealing whether the user exists.

