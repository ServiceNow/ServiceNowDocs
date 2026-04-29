---
title: Configure the entity filters
description: Configure entity filters to define the records from ServiceNow tables that populate each entity type after setting up pillars and entity types. Entity filters use selection criteria to identify and pull relevant records automatically. You can build custom filter conditions tailored to your requirements or select from predefined \(saved\) queries for common scenarios.
locale: en-US
release: australia
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up pillars, entity types, entity filters, and entities, Configuring Operational Resilience, Operational Resilience, Governance, Risk, and Compliance]
---

# Configure the entity filters

Configure entity filters to define the records from ServiceNow tables that populate each entity type after setting up pillars and entity types. Entity filters use selection criteria to identify and pull relevant records automatically. You can build custom filter conditions tailored to your requirements or select from predefined \(saved\) queries for common scenarios.

## Before you begin

Role required: sn\_oper\_res.admin, sn\_oper\_res.manager

## About this task

Choose the appropriate method based on your specific filtering requirements and the complexity of your data selection criteria: build custom conditions for specific requirements or use predefined queries for standard scenarios.

|Options|Use when|Filter example|
|-------|--------|--------------|
|Build custom conditions|You need a specific, tailored criteria|"Status=Active" AND "Region=US" AND "Cost Center=IT"|
|Use predefined queries|Standard filters meet your needs|All Active Servers, All Business Services|

## Procedure

1.  Build custom conditions as the recommended method for configuring entity filters.

    1.  Open an Entity Type record and scroll to the Entity Filters related list.

        The Entity Filters related list is shown in the example.

        ![The Active check box is selected.](../image/ent-types-active-option.png)

    2.  To create a filter condition, select **New**.

        The example shows the dialog box.

        ![Entity filter.](../image/ent-filter-build-condition.png)

    3.  Select **Build your own conditions** in the Filter conditions section, choose **Table** to query \(for example, cmdb\_ci\_server for servers\), and add filter conditions using AND/OR logic.

        You can configure different conditions, for example, "Operational status" IS "Operational."

        The examples show the filter conditions section.

        ![Conditions.](../image/ent-filter-condition-section.png)![Assignment section.](../image/ent-filter-condition-asmt-section.png)

    4.  Select **Pillar** and then select **Entity type** in the Assignment section.

    5.  Check the Active check box.

    6.  Select **Update**.

2.  Select predefined queries as an option step for configuring entity filters.

    1.  Open an Entity Type record and scroll to the Entity Filters related list.

    2.  To create a filter, select **New**.

    3.  Choose **Select from predefined queries** in the Filter conditions section and choose a saved query.\)

        The example shows that you can select a saved query to set up the filter.

        ![Select from predefined queries.](../image/ent-filter-predefined-query-2.png)

    4.  Select **Pillar** and then select **Entity type** in the Assignment section.

    5.  Check the Active check box.

    6.  Select **Submit**.

        **Note:** Entity filters must be activated to generate entities. Inactive filters don’t produce entities even if they’re properly configured.


