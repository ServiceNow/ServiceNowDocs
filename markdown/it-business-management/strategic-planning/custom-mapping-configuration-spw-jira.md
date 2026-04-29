---
title: Custom mapping configuration for SPW Jira Integrations
description: Learn about creating custom mapping configurations to map Jira issue types, fields, and choices with SPW entities, to match your team's processes. Create a custom mapping configuration between tables of Strategic Planning Workspace \(SPW\) and Jira.Create a custom mapping configuration between fields of Strategic Planning Workspace \(SPW\) and Jira.Create a custom mapping configuration for field choices between Strategic Planning Workspace \(SPW\) and Jira.
locale: en-US
release: australia
product: Strategic Planning
classification: strategic-planning
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure Jira project settings, Configure, SPW Jira Integrations, Strategic Planning, Strategic Portfolio Management]
---

# Custom mapping configuration for SPW Jira Integrations

Learn about creating custom mapping configurations to map Jira issue types, fields, and choices with SPW entities, to match your team's processes.

Custom mapping configurations allow you to control how Jira issue types, fields, and values align with SPW planning items. While default mappings cover common use cases, they may not fit your team's processes or reporting needs. By creating custom mappings, you can:

-   Ensure accurate synchronization of work items between Jira and SPW.
-   Align data mapping to reflect your team’s terminology and workflows.
-   Support consistent reporting and visibility across strategy and execution.

This flexibility helps provides a tailored integration experience, so that portfolio managers and delivery teams work with information that matches their context.

## Create custom table mapping for SPW Jira integrations

Create a custom mapping configuration between tables of Strategic Planning Workspace \(SPW\) and Jira.

### Before you begin

[Review default mapping configuration for Jira projects in SPW](../task/review-default-map-config-jira-projects-spw.md).

Role required: sn\_jira\_int.user

### About this task

Choose one table from Jira and one from SPW to create a mapping between them.

For example, if your team uses an issue type like Feature that isn’t mapped by default, you can create a new mapping between the Feature issue type in Jira and the Feature \[sn\_align\_core\_feature\] table in SPW.

### Procedure

1.  Navigate to **All** &gt; **Strategic Planning** &gt; **Jira Integration** &gt; **Jira Projects**.

2.  Open your Jira project record.

3.  From the Table Maps related list, select **New**.

4.  On the Table Map form, fill in the fields.

    For field information, see [Table Map form](../reference/spw-table-map-form.md).

5.  Select **Submit**.


### What to do next

1.  Validate your new table map configuration by clicking **Validate and fix mapping** from the Jira project form.
2.  For this table map, create field mappings. See [Create custom field mapping for SPW Jira integrations](custom-mapping-configuration-spw-jira.md#).

## Create custom field mapping for SPW Jira integrations

Create a custom mapping configuration between fields of Strategic Planning Workspace \(SPW\) and Jira.

### Before you begin

Role required: sn\_jira\_int.user

### About this task

Select a Jira field and map it to a corresponding SPW field in the Table Map record.

For example, a table mapping between the Story entity in Jira and the Story \[rm\_story\] table in SPW is available by default. If you need to map additional fields, such as story points, create a custom Field Map record using the steps below.

### Procedure

1.  Navigate to **All** &gt; **Strategic Planning** &gt; **Jira Integration** &gt; **Jira Projects**.

2.  Open your Jira project record.

3.  From the Table Maps related list, open a table map record for which you want to create field maps.

4.  From the Field Map related list, select **New**.

5.  On the form, fill in the fields.

    For field information, see [Field Map form](../reference/spw-field-map-form.md).

6.  Select **Submit**.


### What to do next

1.  Validate your new mapping configuration by clicking **Validate and fix mapping** from the Jira project form.
2.  \(Optional\) If your new field is of the type Choice, create custom choice mapping for it. See [Create custom choice mapping for SPW Jira integrations](custom-mapping-configuration-spw-jira.md#).

## Create custom choice mapping for SPW Jira integrations

Create a custom mapping configuration for field choices between Strategic Planning Workspace \(SPW\) and Jira.

### Before you begin

Role required: sn\_jira\_int.user

### About this task

Select a choice value from a Jira entity and map it to a corresponding choice value in an SPW table.

For example, Jira Stories include default states such as To Do, In Progress, and Done. If your team adds a custom state like Testing, you can create a choice mapping to link **Testing** in Jira to the **Ready for Testing** state in the Story \[rm\_story\] table in SPW.

### Procedure

1.  Navigate to **All** &gt; **Strategic Planning** &gt; **Jira Integration** &gt; **Jira Projects**.

2.  Open your Jira project record.

3.  From the Table Maps related list, open your table map record.

4.  From the Field Maps related list, open a field map record for which you want to create choice maps.

5.  From the Choice Map related list, select **New**.

6.  On the form, fill in the fields.

    For field information, see [Choice Map form](../reference/spw-choice-map-form.md).

7.  Select **Submit**.


### What to do next

1.  Validate your new mapping configuration by clicking **Validate and fix mapping** from the Jira project form.
2.  [Enable bidirectional sync of work items between Jira projects and SPW](../task/enable-bidirectional-sync-spw-jira.md).
3.  [Import issues from Jira to SPW](../task/import-issues-from-jira-to-spw.md).

