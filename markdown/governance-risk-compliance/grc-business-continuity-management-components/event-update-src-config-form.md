---
title: Event dependency source configuration form
description: Use the Event dependency source configuration form to add the event dependency details such as the event record name, its target records, and sources in the BCM application.
locale: en-US
release: yokohama
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure Event dependency source configuration record, Configuring sources for adding event dependencies, Dependency Configuration records, General administration setup for BCM, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Event dependency source configuration form

Use the Event dependency source configuration form to add the event dependency details such as the event record name, its target records, and sources in the BCM application.

## Event dependency source configuration record form

For description of the field values, see the table.

<table id="table_k3d_xgj_2nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the recovery event. The impacted assets are updated based on the asset that is added by the user to the recovery event.

</td></tr><tr><td>

Active

</td><td>

Option to select the active configurations. Active configurations are used to update the dependencies. Inactive configurations are retired.

</td></tr><tr><td>

Order

</td><td>

Field to identify the first configuration that is fulfilled by the record. The identified configuration is used to update the impacted assets. Multiple configurations can be done for the same record.

</td></tr><tr><td class="sub-head" colspan="2">

Target

</td></tr><tr><td>

Target table

</td><td>

Event \[sn\_recovery\_event\] table that contains the event records. These records are updated as per the configuration set up in the Event dependency source configuration record.

</td></tr><tr><td>

Filter condition

</td><td>

Filter conditions to identify specific records in the target table. These records are updated as per the configuration set up in the Event dependency source configuration record.

</td></tr><tr><td class="sub-head" colspan="2">

Sources

</td></tr><tr><td>

Sources

</td><td>

Applicable sources for adding impacted assets to the recovery event. For the event record, one of these sources can be used:-   BIA upstream dependency
-   BIA downstream dependencies
-   CMDB
-   Plan primary assets
-   Plan related assets

</td></tr><tr><td>

Source records to consider

</td><td>

Option to select a specific record or all records. When selecting source records from the specified sources, the system retrieves dependencies from either all matching records or only from the most recently matched BIA record.

</td></tr></tbody>
</table>**Parent Topic:**[Configure Event dependency source configuration record](../task/conf-event-dep-source-confi-module.md)

