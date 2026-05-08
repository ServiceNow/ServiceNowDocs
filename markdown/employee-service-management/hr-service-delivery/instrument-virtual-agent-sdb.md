---
title: Configure the Virtual Agent topics
description: Configure the Virtual Agent \(VA\) topics for HR Success Dashboard indicators to display data correctly in case you have topics other than the base system topics.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure HR Success Dashboard indicators, HR Success Dashboard indicators, HR Service Delivery, Employee Service Management]
---

# Configure the Virtual Agent topics

Configure the Virtual Agent \(VA\) topics for HR Success Dashboard indicators to display data correctly in case you have topics other than the base system topics.

## Before you begin

Role required: admin

## About this task

Map the topics with deflection patterns of the **HR VA Default** deflection tracker. Deflection tracker helps analyse the performance of a conversation and how helpful Virtual Agent topics are for users.

## Procedure

1.  Navigate to **All &gt; Virtual Agent &gt; Designer**.

2.  Select the HR topic for which you want to add the deflection tracker.

3.  Enable the flow chart view by disabling the **Table View** toggle switch.

4.  Drag and drop the **Deflection** node from the **Utilities** section to the place in the flowchart where you want to add the deflection pattern.

5.  Enter the following details in the Deflection Properties pane on the right.

    |Field|Value|
    |-----|-----|
    |Deflection Configuration|HR VA Default|
    |Deflection Pattern|**HR VA-Self-Resolving:** When the node in the topic indicates that Virtual Agent is able to resolve the user problem completely without creating an IT ticket \(incident or request\) and consequently contributing to the Self-solved KPIs.|
    |Activity Table|Table where the deflection activity occurs. This table is associated with the primary activity table. For more information, see Create deflection configurations and patterns.|
    |Activity Ids|List of comma-separated activity system IDs.|

6.  Select **Save**.


## What to do next

Set up the fulfillment automation level of the HR catalog items, see Set fulfillment automation level of catalog item.

You may also configure the dashboard indicators KPIs, add contributing indicators, or update the More information card, as required.

1.  For more information on configuring the Success Dashboard indicators KPIs, see Configure Success Dashboard indicators KPIs.
2.  For more information on adding contributing indicators, see Add contributing indicators.
3.  For more information on updating the More information card, see Update more information cards.

**Related topics**  


[bundle-convint.deflections-virtual-agent]

[bundle-convint.set-up-deflection-settings-va]

