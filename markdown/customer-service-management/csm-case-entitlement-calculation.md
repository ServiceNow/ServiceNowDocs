---
title: Customer service case entitlement calculation
description: When a customer service agent creates a case, the system uses a configurable method to derive the entitlement based on several fields related to the case record.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure entitlements, Product data, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Customer service case entitlement calculation

When a customer service agent creates a case, the system uses a configurable method to derive the entitlement based on several fields related to the case record.

These fields include:

-   Account
-   Consumer
-   Product
-   Asset
-   Contract
-   Case Channel

If the Proactive Customer Service Operations plugin \(com.snc.proactive\_cs\_ops\) is active, the system also considers these fields:

-   Sold Product
-   Install Base

Relative weights are assigned to each field. Entitlements are calculated based on the weight and precedence. The entitlement with the highest score is assigned to the case.

|Field|Weight/Precedence Assigned|
|-----|--------------------------|
|Account / Consumer|1|
|Product|2|
|Asset / Sold Product / Install Base item|3|
|Contract|4|

The entitlement calculation uses the **global.CSManagementUtils** script and the **getFirstEntitlement** method.

