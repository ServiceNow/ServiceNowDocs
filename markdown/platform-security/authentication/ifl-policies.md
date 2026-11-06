---
title: Identifier-first login policies
description: Identifier-first login is the framework the policy-based login experience currently uses. Identifier-first login policies, evaluated through the policy-based login experience, determine how the instance routes a user to an authentication method after the user enters an identifier.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/authentication/ifl-policies.html
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-11-06"
reading_time_minutes: 2
keywords: [identifier-first login policies, authentication policy conditions]
breadcrumb: [Policy-based login experience, Authentication Console, Authentication, Access Management]
---

# Identifier-first login policies

Identifier-first login is the framework the policy-based login experience currently uses. Identifier-first login policies, evaluated through the policy-based login experience, determine how the instance routes a user to an authentication method after the user enters an identifier.

## Identifier-first login policies for ServiceNow AI Platform

An identifier-first login policy controls how login is determined. After a user enters an identifier, the instance evaluates the active identifier-first login policies and uses the first matching policy to determine which login method is prompted to the user, based on the policy conditions. The login method is either SSO login or Use Password — for example, to a specific SSO provider or to password-based authentication.

Identifier-first login policies are part of the policy-based login experience \(PBLE\). For identifier-first login to work, PBLE must be enabled with the **glide.authenticate.policy\_based\_login\_experience.enabled** system property, the Enable policy-based login setting must be turned on in the Authentication Console, and at least one identifier-first login policy must be active. This setting determines the first authentication factor during user login.

## Identifier-first login policies for Service Portal

When a user signs in through a Service Portal, the Service Portal uses an identifier-first login authentication method where the authentication path is determined by the username or email entered. The path is evaluated against configured identifier-first login policies. Identifier-first login takes precedence over any identity provider or local login options configured for the portal. To know more, see .

## Identifier-first login policies for Now Mobile

When a user signs in through the Now Mobile app, the identifier-first login flow evaluates the same active identifier-first login policies and routes the user to the resulting authentication method. The policies, conditions, and evaluation order are the same as for browser-based logins; the app presents the identifier-first login page and the routed authentication method within the mobile sign-in experience.

Identifier-first login for the Now Mobile app is opt-in. To turn it on, enter `ifl_login.do` as the Login URL in the corresponding OAuth entity record.

**Note:** If **Force local login** is enabled for the mobile app, identifier-first login behavior at login isn't effective in mobile authentication. For more information about force local login, see [KB1560809](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1560809).

## Components of an identifier-first login policy

Each identifier-first login policy defines:

-   Policy order: the order in which the policy is evaluated. Lower values are evaluated first.
-   Conditions: the conditions that determine when the policy applies.
-   Authentication method: SSO login or Use Password, the login method prompted to the user.
-   Policy status: only active policies are evaluated.

For how policies are evaluated, see [Policy evaluation order](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/authentication/policy-evaluation-order.md).

