---
title: Domain separation and Omnichannel Callback
description: Domain separation is supported for Omnichannel Callback. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Omnichannel Callback
classification: omnichannel-callback
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Omnichannel Callback reference, Omnichannel Callback, Manage people and work, Conversational Interfaces]
---

# Domain separation and Omnichannel Callback

Domain separation is supported for Omnichannel Callback. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard

-   Includes all aspects of **Basic** level support.
-   Application properties are domain-aware as needed.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=australia&pubname=australia-platform-security&ft:locale=en-US).

## Overview

Domain separation enables you to partition your organization's data and administrative control into separate domains. This lets you isolate data and control access to it, which is particularly important in environments where multiple tenants share a common platform.

## How domain separation works in Omnichannel Callback

Domain separation in Omnichannel Callback works by routing callback requests to domain-specific available agents.

When using domain separation for Omnichannel Callback, keep the following points in mind.

-   Domain separation applies to both the agent and the customer requesting for a callback. This means that agents will only be able to access interactions records that are created under the domain of the user requesting the callback.
-   The agent should be in the same domain as the user to receive a callback request in the workspace.
-   No configuration is required for domain separation for Omnichannel Callback.

## Domain separated tables

The sys\_cs\_callback table is domain separated.

## Use cases

When domain separation is used, a callback request from guest users is routed to the agent with the same domain as the guest user. For custom chat channels, the domain of the provider application is used as a reference to route the callback to the domain-specific agent.

**Parent Topic:**[Omnichannel Callback reference](omnichannel-callback-reference.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=australia&pubname=australia-platform-security&ft:locale=en-US)

