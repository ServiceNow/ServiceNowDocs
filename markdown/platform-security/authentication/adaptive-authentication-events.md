---
title: Adaptive authentication events
description: You can use the adaptive authentication events table to know about the events.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Adaptive authentication, Authentication, Access Management]
---

# Adaptive authentication events

You can use the adaptive authentication events table to know about the events.

Following are some of the logs that can be tracked in the adaptive authentication events table:

-   `glide.adaptive.auth.log.success.event`: To know the `success` events for Post Auth, API logins.
-   `glide.adaptive.auth.log.mfa.relax.event`: To know the `mfa_relaxation` events for MFA Context.

**Note:**

-   For Pre-Auth Context, Rest API Access policies of type "`pre_auth`": By default `Failure` events are logged. `Success` events `can't` be logged.
-   For Post Auth Context, Rest API Access policies of type other than "`pre_auth`": By default `Failure` events or logged. For `Success` events to log, you need to enable the `glide.adaptive.auth.log.success.event` property.
-   For MFA: By default `MFA Enforcement` events are logged.
-   For MFA Relaxation events to log, you need to enable the `glide.adaptive.auth.log.mfa.relax.event` property. `MFA Relaxation` would log the same event as `MFA Enforcement`, but with the `Result` Field populated with `False`.

