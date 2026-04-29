---
title: Planning dependency update configuration form
description: Use the Planning dependency update configuration form to configure the plan record, its sources, and preferences such as the plan record name, sources, and notification preferences and schedule an auto-update of the related assets in the plans.
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up Planning dependency update configuration, Configuring planning dependency updates, Dependency Configuration records, General administration setup for BCM, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Planning dependency update configuration form

Use the Planning dependency update configuration form to configure the plan record, its sources, and preferences such as the plan record name, sources, and notification preferences and schedule an auto-update of the related assets in the plans.

## Planning dependency update configuration record form

For description of the field values, see the table.

<table id="table_k3d_xgj_2nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the plan record. The related assets are updated based on the primary scope of the plan record.

</td></tr><tr><td>

Active

</td><td>

Option to select the active configurations. Active configurations are used to update the dependencies. Inactive configurations are retired.

</td></tr><tr><td>

Order

</td><td>

Field to identify the first configuration that is fulfilled by the record. The identified configuration is used to update the dependencies. Multiple configurations can be done for the same record.

</td></tr><tr><td class="sub-head" colspan="2">

Target

</td></tr><tr><td>

Target table

</td><td>

Plan \[sn\_bcp\_plan\] table that contains the plan records. These records are updated as per the configuration set up in the Planning dependency update configuration record.

</td></tr><tr><td>

Filter condition

</td><td>

Filter conditions to identify specific records in the target table. These records are updated as per the configuration set up in the Planning dependency update configuration record.

</td></tr><tr><td>

Fields to be updated in the target table

</td><td>

Fields in the target record that can be updated with a specific value.

</td></tr><tr><td>

Auto-update dependencies

</td><td>

Option to update the dependencies automatically. BCM administrators can specify if the updates should be done automatically or if a user review is needed before the update.

</td></tr><tr><td class="sub-head" colspan="2">

Sources

</td></tr><tr><td>

Sources

</td><td>

Applicable sources for adding related assets to the plan. For the business continuity plan record, these sources are used:-   BIA Upstream
-   BIA Downstream
-   CMDB

</td></tr><tr><td>

Source records to consider

</td><td>

Option to select a specific record or all records. When selecting source records from the specified sources, the system retrieves dependencies from either all matching records or only from the most recently matched BIA record.

</td></tr><tr><td class="sub-head" colspan="2">

Notification

</td></tr><tr><td>

Send notification

</td><td>

Option to notify the users or user groups on the updates.

</td></tr><tr><td>

Users/groups in fields

</td><td>

Option to select the users or groups who should receive a notification about the updates. For example, Plan owner and BCM lead are selected to receive the updates.

</td></tr></tbody>
</table>**Parent Topic:**[Set up Planning dependency update configuration](../task/conf-plan-dep-update-confi-module.md)

