---
title: Integrate Dynatrace platform events
description: Integrate Dynatrace with Event Management by adding Dynatrace as an authenticated data source.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrate with push connectors, Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Integrate Dynatrace platform events

Integrate Dynatrace with Event Management by adding Dynatrace as an authenticated data source.

## What authentication is used

There are two methods of authentication:

-   OAuth authentication: Provides enterprise-grade authentication to keep your enterprise environment safe. Authentication is performed using Dynatrace access tokens. For more information, see [Integrate Dynatrace with OAuth authentication](../task/dynatrace-oauth-authentication.md).
-   Basic webhook authentication: Provides a basic standard of authentication, without the need for Dynatrace Active Directory. This authentication can be especially useful for distributed small teams, such as SRE or DevOps teams. For more information, see [Integrate Dynatrace with basic authentication](../task/dynatrace-events-webhook.md).

**Note:** When a problem is reopened in Dynatrace, the original start time is retained and not updated to the time of reopening. This behavior is intentional and reflects how Dynatrace manages the problem lifecycle. Problems reopened within the defined reopening period \(typically 30 minutes\) are treated as a continuation of the original issue. The start time continues to reflect the timestamp of the earliest triggering event, even after reopening.

Do not use the evidence details timestamp as a substitute for the problem start time. The evidence timestamp refers to individual contributing events within the problem. It is part of the Root Cause Analysis \(RCA\) and does not indicate the start or duration of the overall problem.

Starting from the Xanadu release, the base system rules provided with the connector, which you have not previously used \(i.e., neither activated, deactivated, nor modified\), will now have the **Apply additional matching rules** check box set to true. Previously, this check box was disabled. This change allows you to execute more event rules or automation using the same filter conditions for the connector.

**Note:** This feature applies only to active event rules.

