---
title: Working with Webhooks
description: A webhook is an HTTP request, triggered by an event in the source system \(TISC\) and sent to a destination system \(where the endpoint URL is present\), with a payload of event data.
locale: en-US
release: xanadu
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2024-08-12"
reading_time_minutes: 1
breadcrumb: [Administration, Threat Intelligence Security Center, Security Operations]
---

# Working with Webhooks

A webhook is an HTTP request, triggered by an event in the source system \(TISC\) and sent to a destination system \(where the endpoint URL is present\), with a payload of event data.

These webhooks in Threat Intelligence Security Center are useful to notify the destination application whenever the events occurs.

In TISC, you can do the following:

-   Configure Webhooks
-   Manage Triggers
-   Retry mechanism
-   Perform validation
-   Manage subscriptions

-   **[System properties for Webhooks](tisc-sysprops-retry.md)**  
The system properties for webhooks are explained below.
-   **[Configure webhooks](setup-webhooks.md)**  
Configure a webhook to subscribe to events in Threat Intelligence Security Center.
-   **[Webhook Triggers](tisc-triggers.md)**  
Webhook triggers are used to filter the threat intelligence entities that needs to be tracked for any event changes such as Create, Update, and Delete.

