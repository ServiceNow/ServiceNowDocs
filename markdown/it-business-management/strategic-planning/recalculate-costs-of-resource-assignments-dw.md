---
title: Recalculate costs of resource assignments of a demand
description: Recalculate the costs of active resource assignments of a demand when hourly rates change in the associated rate model.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/strategic-planning/recalculate-costs-of-resource-assignments-dw.html
release: zurich
product: Strategic Planning
classification: strategic-planning
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create resource assignments for demands, Manage demands, Use, Next Experience for Demand Management in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Recalculate costs of resource assignments of a demand

Recalculate the costs of active resource assignments of a demand when hourly rates change in the associated rate model.

## Before you begin

The demand must be active with an active rate model.

Role required: it\_demand\_manager

## About this task

To recalculate the costs of resource assignments, you can also use the **Estimate resource requirements** Playbook activity. For more information, see [Use Playbook in Next Experience for Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/strategic-planning/use-playbooks-in-dw.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace**.

2.  Select the Demands icon \[Omitted image "demands-icon.png"\].

3.  Open a demand from the **List** page.

4.  Select **Details** from the navigation menu.

5.  Select the **Resource assignments** tab.

    **Note:** If the **Resource assignments** tab isn't visible, select **More** &gt; **Resource assignments**.

6.  Select a resource assignment record.

7.  Select the More Actions icon \[Omitted image "more-actions-icon.png"\] Alt text: and select **Recalculate Resource Cost**.

8.  If you want to start the recalculation from a specific date or end it on a different date, adjust the values in the **Start date** and **End date** fields.

9.  Select **OK**.


## Result

The resource cost of the selected resource assignment is recalculated based on the hourly rates and is updated on the resource assignment form. The values in the cost fields of the demand are revised accordingly.

