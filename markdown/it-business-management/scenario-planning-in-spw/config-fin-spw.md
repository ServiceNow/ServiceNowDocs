---
title: Configure financials for planning items in Strategic Planning
description: Configure the ServiceNow Internal integrations to view the financials for planning items in Strategic Planning.
locale: en-US
release: yokohama
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configure, Portfolio Planning in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Configure financials for planning items in Strategic Planning

Configure the ServiceNow Internal integrations to view the financials for planning items in Strategic Planning.

## Before you begin

Role required: admin

## Procedure

1.  Configure the attributes to generate labor costs in financials based on the resource assignments on the work items.

    For more information, see [Using the Planning attributes](../../project-management/concept/planning-attributes.md) and [Create or edit planning attributes](../../project-management/task/configure-planning-attributes.md#).

2.  Generate default mapping configurations to create table maps.

    For more information, see [Generate default mapping configurations](../../apw-internal-integrations/task/generate-default-mapping-configurations.md).

3.  Enable financials for epics to work on financial planning.

    For more information, see [Enable financials for planning items in Strategic Planning](enable-spw-fin-epic.md).

4.  Enable budget allocation and define a budget attribute, cost type or expense type, to allocate budget for your planning items.

    For more information see [Enable financial budget allocation for planning items in Strategic Planning](enable-fin-budget-spw.md) and [Configure budget attribute at instance-level to allocate budget](config-budget-allocation-attribute-spw.md)

5.  Enable the monetary and non-monetary benefit plans related lists for your planning items in workspace view.

    For more information, see [Add monetary and non-monetary benefit plans related lists](enable-benefit-plans-planning-items.md).

6.  Create new widgets to view the rolled up financial data at planning item level.

    For more information, see [Configure a widget and associate it with project](configure-financial-widgets.md).

7.  Customize the left pane in the financials screen to match the requirements of your organization.

    For more information, see [Customize the left pane view for financials](customize-fin-left-pane.md).

8.  Customize the Create cost plan form fields to match the requirements of your organization.

    For more information, see [Customise cost plan form](customise-cost-plan-form-fin.md).

9.  Customize the default expense types to manage cost plans for your planning items.

    For more information, see [Change the default expense type for your planning items](config-expense-type-fin-spw.md)

10. Define a custom prefix for your baseline name.

    For more information, see [Create a custom prefix for baseline](fin-config-baseline-prefix.md).

11. Activate and define scheduled job to automatically migrate budget for your planning items.

    For more information, see [Activate a scheduled job to migrate budget of your planning items](fin-migrate-budget-scheduled-job-spw.md).

12. Activate and define a scheduled job to migrate financial baselines for your planning items.

    For more information, see [Migrate financial baselines to Next Experience](../../project-management/task/migrate-fin-baselines-projects.md).

13. Activate and define scheduled job to automatically create financial baselines for your planning items at a defined cadence.

    For more information, see [Activate scheduled job to create financial baselines for planning items](baseline-scheduler-job.md).

14. Activate and define scheduled jobs to automatically generate labor costs for your planning items based on the attribute-based resource assignments at a defined cadence.

    For more information, see [Activate scheduled jobs to generate labor costs for your planning items](labor-cost-scheduler-job-spw.md).


