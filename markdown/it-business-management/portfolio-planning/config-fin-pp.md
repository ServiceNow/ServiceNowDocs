---
title: Configure financials for planning items in Portfolio Planning
description: Configure the ServiceNow Internal integrations to view the financials for planning items in Portfolio Planning.
locale: en-US
release: xanadu
product: Portfolio Planning
classification: portfolio-planning
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure, Portfolio Planning, Strategic Portfolio Management]
---

# Configure financials for planning items in Portfolio Planning

Configure the ServiceNow Internal integrations to view the financials for planning items in Portfolio Planning.

## Before you begin

Role required: admin

## Procedure

1.  Configure the attributes to generate labor costs in financials based on the resource assignments on the work items.

    For more information, see [Planning attributes](../../project-management/concept/planning-attributes.md) and [Create or edit planning attributes](../../project-management/task/configure-planning-attributes.md#).

2.  Generate default mapping configurations to create table maps.

    For more information, see [Generate default mapping configurations](../../apw-internal-integrations/task/generate-default-mapping-configurations.md).

3.  Create new widgets to view the rolled up financial data at planning item level.

    For more information, see [Configure a widget and associate it with project](../../spw-financials/task/configure-financial-widgets.md).

4.  Customize the left pane in the financials screen to match the requirements of your organization.

    For more information, see [Customize the left pane view for financials](customize-fin-left-pane-pp.md).

5.  Enable budgeting option to allocate and manage budget of your planning items.

    For more information, see [Enable financial budget allocation for planning items in Portfolio Planning](enable-fin-budget-ppw.md).

6.  Configure the budget attribute to expense type or cost type to manage the budget of your planning items.

    For more information, see [Configure budget attribute at instance-level to allocate budget](config-budget-allocation-attribute-ppw.md).

7.  Customize the Create cost plan form fields to match the requirements of your organization.

    For more information, see [Customise cost plan form](customise-cost-plan-form-fin-pp.md).

8.  Customize the default expense types to manage cost plans for your planning items.

    For more information, see [Change the default expense type in Portfolio Planning](config-expense-type-fin-pp.md).

9.  Define a custom prefix for your baseline name.

    For more information, see [Create a custom prefix for baseline](../../spw-financials/task/fin-config-baseline-prefix.md).

10. Activate and define a scheduled job to migrate budget for your planning items.

    For more information, see [Activate a scheduled job to migrate budget of your planning items](fin-migrate-budget-scheduled-job-ppw.md)

11. Activate and define scheduled job to automatically create financial baselines for your planning items at a defined cadence.

    For more information, see [Activate a scheduled job to create financial baselines for your projects and demands](baseline-schedule-job-pp.md).

12. Activate and define a scheduled job to generate labor costs for your projects and demands based on the attribute-based resource assignments.

    For more information, see [Activate a scheduled job to generate labor costs for your projects and demands](gen-labor-costs-scheduled-job-pp.md).


