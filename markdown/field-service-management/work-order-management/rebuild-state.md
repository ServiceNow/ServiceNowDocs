---
title: Rebuild state flows
description: Administrators can rebuild state flows when a mismatch between existing and new sys\_ids occurs.
locale: en-US
release: xanadu
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Customizing State flows, Configuring work orders, Setting up work orders and tasks, Configuring Field Service Management, Field Service Management]
---

# Rebuild state flows

Administrators can rebuild state flows when a mismatch between existing and new sys\_ids occurs.

When you use an XML file to import state flows into an instance, the system attempts to match the incoming states with existing states by comparing sys\_ids. Because the sys\_ids of items in a choice list can vary between instances, the system can fail to match the states, even though they’re otherwise identical.

When matching fails, the start and end states of affected records are left empty or contain numeric values. To repair these records, navigate to **State Flows** &gt; **Admin** &gt; **Rebuild State Flows**. This module runs a script that compares the numerical value of each item in the **State** field choice list until it finds a match in the imported state flow record.

An example of when to rebuild a state flow is if you have state flows from another Service Now application, like Customer Service Management, and want to use them for Field Service Management. You would export an XML file from the Customer Service Management state flows, then upload that XML file to the Field Service Management state flows. If there are mismatching states used in Customer Service Management and Field Service Management, then you must rebuild the Field Service Management state flows.

