---
title: Team-based integration properties
description: Team-based integration system properties enable you to customize the assignment group functionality for existing and new customers for event rules and event field mapping.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Event Management reference, Event Management, ITOM Health, IT Operations Management]
---

# Team-based integration properties

Team-based integration system properties enable you to customize the assignment group functionality for existing and new customers for event rules and event field mapping.

<table id="table_e5g_lsy_nxb"><thead><tr><th align="left">

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

evt\_mgmt.alert\_auto\_assignment\_field

</td><td>

The property determines automatic alert assignment through an ordered list of comma-separated fields. The default value of this property is cmdb\_ci.support\_group, IntegrationGroup. The assignment group value is taken from the **Support group** field \(cmdb\_ci.support\_group\) of the alert's CI. If this field is empty, the value is taken from the IntegrationGroup value in the **Assignment group** field in the Connector instances table \[em\_connector\_instance\].

For upgraded instances from previous family releases, the value is empty to avoid any impact on production instances. -   **Type**: String
-   **Default value**:
    -   Empty - for upgraded customers
    -   cmdb\_ci.support\_group, IntegrationGroup - for new customers

**Note:** When you use an alert field in this property value such as an alert field in the **Additional Info** field, an alert tag, or a new alert field, the value of the **Assignment group** field must be the group sys\_id. For example, `{"Alert field name":"<sys_id of the desired sys_user_group record>"}.`.

</td></tr><tr><td>

evt\_mgmt.enable\_group\_level\_event\_rules

</td><td>

Activates team-based functionality for executing event rules and event field-mapping rules. Global rules take precedence over specific team-based rules.

-   **Type**: Boolean
-   **Default value**:
    -   False - for upgraded customers
    -   True - for new customers

</td></tr></tbody>
</table>**Parent Topic:**[Event Management reference](event-management-reference.md)

