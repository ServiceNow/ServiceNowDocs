---
title: Element definition record form
description: Use the Element definition record form to configure a recovery tier with a set of business applications by using BCM UIB Workspace.
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure element definition, General administration setup for BCM, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Element definition record form

Use the Element definition record form to configure a recovery tier with a set of business applications by using BCM UIB Workspace.

## Element definition record form

For description of the field values, see the table.

<table id="table_k3d_xgj_2nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the element definition. It uses the translated\_text field type, a text field that displays translations based on the language used.

</td></tr><tr><td>

Source Table

</td><td>

Table that stores the record details of the configuration item.

</td></tr><tr><td>

Source Table Fields

</td><td>

Column heads of the source table that you can select for reference.

 The **source\_table\_fields** configuration applies to the **Scope** tab in BCPs and the **Assets** tab in recovery events.

 The purpose of **source\_table\_fields** is to set the columns for the modal based on the asset type. In the **Scope** tab of BCPs, these columns appear when you select **Add primary scope** or **Add related asset**. In the **Assets** tab of recovery events, these columns appear when you select **Add**.

</td></tr><tr><td>

Filter

</td><td>

Add filter condition for the element definition. **Note:** Starting with the Xanadu release, the element definition filter for the Hardware element definition has been updated. You can now add a Windows server asset in the Windows server element definition or a Linux server asset in the Linux server element definition. However, you cannot add the Windows server asset or the Linux server asset in the filter of the Hardware element definition.

</td></tr><tr><td>

Requires data backup

</td><td>

Option to indicate if the primary element requires a data backup. Technology assets require data backup as they pertain to important IT information stored in a system or database.

</td></tr><tr><td>

Resource configuration

</td><td>

Resource configuration for the element definition. Available options are:-   **Location**
-   **Web Server**
-   **Datacenters**
-   **Vendors**

For information on configuring a Resource configuration record, see [Configure Resource Configuration records](../task/conf-resource-for-crisis-map-uib-ws.md).

</td></tr></tbody>
</table>**Parent Topic:**[Configure element definition](../task/configure-element-definition-bia-uib-ws.md)

