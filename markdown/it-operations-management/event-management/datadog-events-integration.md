---
title: Integrate Datadog platform events
description: Integrate Datadog with Event Management by adding a standard webhook in the Datadog console.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Integrate with push connectors, Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Integrate Datadog platform events

Integrate Datadog with Event Management by adding a standard webhook in the Datadog console.

## What authentication is used

There are two methods of authentication:

-   OAuth authentication: Provides enterprise-grade authentication to keep your enterprise environment safe. Authentication is performed using Datadog Monitor V1 or V2 access tokens. For more information, see [Integrate Datadog with OAuth authentication](../task/datadog-oauth-authentication.md).
-   Basic webhook authentication: Provides a basic standard of authentication, without the need for Datadog Active Directory. This authentication can be especially useful for distributed small teams, such as SRE or DevOps teams. For more information, see [Integrate Datadog with basic authentication](../task/datadog-events-webhook.md).

Starting from the Xanadu release, the OOTB \(Out-Of-The-Box\) event rules provided with the connector, which you have not previously used \(i.e., neither activated, deactivated, nor modified\), will now have the **Apply additional matching rules** check box set to true. Previously, this check box was disabled. This change allows you to execute more event rules or automation using the same filter conditions for the events.

**Note:** This feature applies only to active event rules.

