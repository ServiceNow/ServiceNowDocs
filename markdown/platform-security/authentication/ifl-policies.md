---
title: IFL policies
description: Identifier-first login \(IFL\) is the framework the policy-based login experience currently uses. IFL policies, evaluated through the policy-based login experience, determine how the instance routes a user to an authentication method after the user enters an identifier.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/ifl-policies.html
release: brazil
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-09-24"
reading_time_minutes: 1
keywords: [IFL policies, identifier-first login policies, authentication policy conditions]
breadcrumb: [Policy-based login experience, Authentication Console, Authentication, Access Management]
---

# IFL policies

Identifier-first login \(IFL\) is the framework the policy-based login experience currently uses. IFL policies, evaluated through the policy-based login experience, determine how the instance routes a user to an authentication method after the user enters an identifier.

## IFL policies for ServiceNow AI Platform

An IFL policy maps a set of conditions to an authentication method. After a user enters an identifier, the instance evaluates the active IFL policies and uses the first matching policy to route the user — for example, to a specific SSO provider or to password-based authentication.

## IFL policies for Service Portal

When a user signs in through a Service Portal, the Service Portal uses an identifier-first login \(IFL\) authentication method where the authentication path is determined by the username or email entered. The path is evaluated against configured IFL policies. IFL takes precedence over any identity provider or local login options configured for the portal. To know more, see [Enable identifier-first login in Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/identifier-first-login-service-portal.md).

## IFL policies for Now Mobile

When a user signs in through the Now Mobile app, the identifier-first login flow evaluates the same active IFL policies and routes the user to the resulting authentication method. The policies, conditions, and evaluation order are the same as for browser-based logins; the app presents the identifier-first login page and the routed authentication method within the mobile sign-in experience.

## Components of an IFL Policy

Each IFL policy defines:

-   An evaluation order \(priority\).
-   The matching conditions.
-   The associated authentication method \(an SSO provider or password-based authentication\).

For how policies are evaluated, see [Policy evaluation order](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/policy-evaluation-order.md).

