---
title: Run Assignments
description: Run sales territory assignments to assign CRM entities to the most eligible territory. Each territory is checked against its own or cascaded territory conditions related to the CRM entity.​
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Sales Territory Management, Lead and opportunity management apps, Configure, Sales and Order Management]
---

# Run Assignments

Run sales territory assignments to assign CRM entities to the most eligible territory. Each territory is checked against its own or cascaded territory conditions related to the CRM entity.​

## Before you begin

Role required: sales territory admin

-   Complete all prerequisite configuration steps, such as activating the sales territory model, configuring territory levels, and defining territory conditions.

## Procedure

1.  Navigate to **All** &gt; **Sales Territory Management** &gt; **Run Assignments**.

2.  Select an active sales territory model or territory to run assignment rules:

    -   If active sales territory model is selected, all selected sources and their data are evaluated against the complete territory hierarchy. Existing assigned territory will be replaced with the newly evaluated one.
    -   If active territory is selected, only those entities with no assigned territory will be evaluated against the territory condition.
3.  Select one or more source tables to run assignment rules on:

    -   Opportunity \(sn\_opty\_mgmt\_core\_opportunity\)
    -   Lead \(sn\_lead\_mgmt\_core\_lead\)
    -   Consumer \(csm\_consumer\)
    -   Account \(customer\_account\)
4.  Select **Run Assignment Rules**.


## Result

Sales Territory Management is assigned in the CRM entities. All the Sales Territory admins will receive an email notification when the job is completed. The selected sources entities are assigned to a territory if they fulfill the territory conditions.

