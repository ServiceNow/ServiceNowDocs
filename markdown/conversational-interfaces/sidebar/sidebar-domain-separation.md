---
title: Domain separation and Sidebar
description: Domain separation is supported for Sidebar . Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: xanadu
product: Sidebar
classification: sidebar
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Reference, Sidebar, Conversational Interfaces]
---

# Domain separation and Sidebar

Domain separation is supported for Sidebar. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard

-   Includes all aspects of **Basic** level support.
-   Application properties are domain-aware as needed.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

## Overview of domain separation and Sidebar

To set up domain separation for Sidebar, enable domain separation for your instance. If your instance has multiple domains, you can turn Sidebar on or off for each domain. No special configuration is needed to configure a domain-separated environment with Sidebar. Domain separation for Sidebar is supported only when domains are set up using a parent-child domain hierarchy.

Sidebar discussions are domain separated according to the base record \(task or interaction record\). You can see and create sidebar discussions only if you have access to the task or interaction record.

For example, say INC00001 belongs to the record created in the ACME domain and the Cisco domain doesn't have access to INC00001. Users that belong to the Cisco domain can't interact with Sidebar discussions based on INC00001.

## Sidebar versions for domain separation

To fully utilize domain separation, you must be on both the Vancouver version and August version of the Sidebar store app \(Omni Experience Standard Feature Set\).

If you are a first time Sidebar user in Vancouver \(you did not use Sidebar earlier and are not trued up to the Vancouver store app\) and want to leverage domain separation, Sidebar is inactive by default. Navigate to the Conversational Interfaces settings page for each domain and activate Sidebar manually. Alternatively, you can access the sys\_cs\_collab\_settings table and manually insert a new record for each domain.

There is a known issue with emojis not working as expected when used with domain separation. A workaround for this issue is to go to the Enable Emojis ACE Content block and update the record field with the sys\_cs\_collab\_settings record's sys\_id for the given domain.

## Domain separation with the Sidebar and Microsoft Teams integration

If Sidebar and Microsoft Teams are integrated and configured, activating Sidebar prompts a message stating that the Microsoft Teams integration must be manually turned on and deactivating Sidebar prompts a message stating that the integration with Microsoft Teams will also be turned off.

Domain separation will not work with Microsoft Teams if multiple domains are configured. Pairing a unique Microsoft Teams with each domain is not supported.

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)

