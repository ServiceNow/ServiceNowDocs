---
title: Properties installed with Enterprise Agile Planning
description: System properties that you can configure to modify the way your product manager or scrum team members view their work in the Enterprise Agile Planning \(EAP\) workspace.
locale: en-US
release: australia
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Properties installed with Enterprise Agile Planning

System properties that you can configure to modify the way your product manager or scrum team members view their work in the Enterprise Agile Planning \(EAP\) workspace.

These properties are available for Enterprise Agile Planning.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_q2m_ym2_p2c"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_apw\_advanced.eap\_work\_structure\_allow\_list

</td><td>

Enables viewing different work item types in the Backlog and Planning board pages for EAP teams.

 -   Type: string
-   Default value:

sn\_align\_core\_scrum\_epic,sn\_align\_core\_capability,sn\_align\_core\_feature,rm\_story

**Important:** Any item, which is an extension of the Enterprise agile planning item \[sn\_align\_core\_eap\_planning\_item\] table must be entered before **rm\_story**.

-   Location: System Property \[sys\_properties\] table
-   Learn more: [Configure display of other work item types in EAP Backlog and Planning board](../task/configure-other-work-item-types-for-eap-teams-in-backlog-and-planning-board.md)

</td></tr><tr><td>

sn\_apw\_advanced.enable\_hierarchy\_view

</td><td>

Enables the Hierarchy view in Enterprise Agile Planning to display work items in an expandable parent‑child tree.

 -   Type: true \| false
-   Default value: false
-   Location: System Property \[sys\_properties\] table
-   Learn more: [Enable Hierarchy tab in EAP](../task/hierarchy-enable-eap.md)

This property is available only after the **Populate parent level data for work item** fix script is run. For more information, see [Enable Hierarchy tab in EAP](../task/hierarchy-enable-eap.md).


</td></tr></tbody>
</table>**Parent Topic:**[Enterprise Agile Planning reference](eap-reference.md)

