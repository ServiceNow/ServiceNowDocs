---
title: Bind CIs using CI field matching and handling column name differences
description: Bind CIs by matching event Additional information fields with CI attributes. If column names differ, manually create an additional key-value pair to align with the CI table, ensuring accurate CI association.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-05-01"
reading_time_minutes: 1
breadcrumb: [Overriding default binding, Binding alerts to CIs, Event rules, Processing Events, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Bind CIs using CI field matching and handling column name differences

Bind CIs by matching event **Additional information** fields with CI attributes. If column names differ, manually create an additional key-value pair to align with the CI table, ensuring accurate CI association.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

If no match is found using the **Node** field, the system looks at the **Additional information** field in the event record. There may be cases where no match is found because the column names in the event record and the table differ for the same item. In such cases, you can manually create an additional key-value pair with a name matching the table column and add it to the **Additional information** field, ensuring the matching process continues successfully.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Rules** &gt; **Event Rules**.

2.  Select **New** and complete the required fields, or open an existing event rule record to modify it.

3.  Select the **Transform and Compose Alert Output** tab.

4.  Select the **Manual attributes** check box.

5.  In the **Field Name** and **Field Value** fields, enter the corresponding field name and specify the source field from which the value should be populated.

    ![Manual attribute for an alert.](../image/em-ms-iis-webserver-attribute.png)

    Use the add icon \(![Add icon](../image/em-add-icon.png)\) icon to add multiple fields as needed.

6.  Select **Save**.

    The fields are created in the event rules record. However, when any alert is generated from an event using the event rule, the manually added fields appear in the **Additional information** field of the alert.


