---
title: Add the impacted area
description: Add an impacted area or an object to the operational vulnerability record in the Operational Resilience Workspace.
locale: en-US
release: zurich
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Managing Operational vulnerability, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Add the impacted area

Add an impacted area or an object to the operational vulnerability record in the Operational Resilience Workspace.

## Before you begin

Role required: sn\_oper\_res.manager

## About this task

When an impacted area is added for the vulnerability, its state is updated to **New \(In progress\)** as shown on the **Overview** tab of the vulnerability record.

Beginning with Release 20.1.x, the Operational Resilience application supports the latest Common Service Data Model \(CSDM\). The enhanced functionality supports the roll up of the dependencies.

## Procedure

1.  Navigate to **Workspaces** &gt; **Operational Resilience Workspace** &gt; **All Operational Vulnerabilities**.

2.  Open the vulnerability for which you want to add an impacted area.

3.  Select **New**.

4.  On the Impacted area form, fill in the fields.

    To view more information on the fields, see the [Impacted area form](../reference/impacted-area-form.md).

5.  Select **Save**.

    **Note:** The operational administrator can view the progress of adding impacted assets to the operational vulnerabilities and they can also change the order of the dependencies.

    When you add the primary origin of the operational vulnerability, its impacted areas with upstream entities are updated on the **Impacted areas** tab.

    ![Impacted areas with upstream entities.](../image/op-vul-pri-ori-imp-area.png)

    When the scheduled job is executed, the updated impacted areas and the overall operational vulnerability count are reflected in the dashboard.

    ![Count 0.](../image/op-vul-count-0.png)

    For example, when the impacted areas in the operational vulnerability are updated, the operational vulnerability count on the overview page of SO1 remains at 0 before the scheduled job runs.

    ![Count 1.](../image/op-vul-count-1.png)

    After running the scheduled job, the operational vulnerability count on the overview page of SO1 is updated to 1. This ensures that the updated data is promptly reflected on the Operational Resilience dashboard.


