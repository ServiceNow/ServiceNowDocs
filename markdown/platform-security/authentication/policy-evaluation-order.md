---
title: Policy evaluation order
description: The instance evaluates IFL policies in order and applies the first policy whose conditions match the user.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/policy-evaluation-order.html
release: brazil
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-09-24"
reading_time_minutes: 1
keywords: [policy evaluation order, IFL evaluation, first match, fallback]
breadcrumb: [Policy-based login experience, Authentication Console, Authentication, Access Management]
---

# Policy evaluation order

The instance evaluates IFL policies in order and applies the first policy whose conditions match the user.

## First-match evaluation

IFL policies are evaluated in order. The instance applies the first policy whose conditions match the user and routes the user to the authentication method defined in that policy. Policies are evaluated by their Policy order value, and lower values are executed first. Only active policies are evaluated; inactive policies are skipped.

## Fallback behavior

If no policy matches, the instance uses the default routing:

-   The instance applies default SSO routing, using the user's SSO source or the default identity provider \(IdP\).
-   If no IdP applies, the instance falls back to the local login page.

