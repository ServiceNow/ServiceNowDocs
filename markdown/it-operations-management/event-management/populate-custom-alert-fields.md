---
title: Custom alert fields
description: You can populate custom alert fields with data contained in Additional information field of the event.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Processing Events, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Custom alert fields

You can populate custom alert fields with data contained in **Additional information** field of the event.

Valuable data contained in **Additional information** fields of events can be useful, for example, for reporting. Alert fields are automatically populated from fields that have the same name in the event. This behavior holds true for **Additional information** event fields and for **Additional information** fields that Event Rule adds. Therefore, to populate a custom alert field with the value in **Additional information** fields, use the custom field name in the **Additional information** field. You can also use Event Rules for this purpose. Values in the **Additional information** field of an Event that are not in JSON key/value format are normalized to JSON format when the event is processed. For more information, see [Configure an event rule to customize alert content](../task/t_EMComposeOuput.md).

The short description field of an alert is automatically written using the type, node, and description of the alert. To prevent the short description field from being over-written, open the **sys\_properties** table, locate the **evt\_mgmt.override\_alert\_short\_description** property, change the value to `false`, and then click **Update**.

Depending on permissions, you may only be able to create fields with the **user\_** prefix. If so, use Event Rules to create an **Additional information** field with the same name. To prevent some fields to be copied to the alert field, use the **evt\_mgmt.alert\_black\_list\_fields** property and add the field names that must be excluded. By default, the fields that are not copied are:

-   message\_key
-   category
-   additional\_info
-   sys\_updated\_on
-   sys\_updated\_by
-   sys\_created\_by
-   sys\_created\_on
-   sys\_mod\_count
-   sys\_id

**Parent Topic:**[Processing Events](processing-events.md)

