---
title: Configure Matrix report registry
description: Configure the Matrix report registry to select the base table. You can create a relationship of the base with the target table to configure the details of the report for an entity-related record or a landing page.
locale: en-US
release: yokohama
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2025-07-24"
reading_time_minutes: 1
breadcrumb: [Matrix report in Risk Workspace, Use Risk Workspace, Risk Management, Governance, Risk, and Compliance]
---

# Configure Matrix report registry

Configure the Matrix report registry to select the base table. You can create a relationship of the base with the target table to configure the details of the report for an entity-related record or a landing page.

## Before you begin

Role required: sn\_matrix\_report.admin

## Procedure

1.  Navigate to **All** &gt; **Matrix report** &gt; **Matrix report registry**.

2.  Select **New**.

3.  Enter the name of the Matrix report registry in the **Name** field.

4.  Select **Entity \[sn\_grc\_profile\]** in the **Base table** field.

5.  Select **Submit**.

    The Matrix report registry is created and appears in a list view.

6.  Select the Matrix report registry that you created.

    The base level of the configuration is auto-populated, which contains the base target table and you can select any filter conditions. For the next level configuration, add new relationships between the base table and a target table for the matrix report.

7.  In the Matrix relationships related list, select **New**.

8.  On the form, fill in the fields.

    For a description of the field values, see [Matrix relationship form](../../grc-workspace-audit/reference/matrix-rel-audit-report-ws.md).

9.  Select **Submit**.

    You have configured the base table, which is the level 0 of the matrix report configuration. You can add new configurations as well. For example, if you have selected the base table as Entity, then you can add configurations such as risk related to that entity, which would be level 1. For level 2, you can configure a relationship between controls and issues. Parent record as source helps to identify the record from which the data is taken.

    **Note:** The Source table and the Relationship can’t be the same in the Matrix report registry.


## What to do next

After the matrix relationship is complete, you can [Configure target table fields as columns for matrix report](../../grc-workspace-audit/task/matrix-report-relationship-audit-ws.md).

**Parent Topic:**[Matrix report in Risk Workspace](../concept/matrix-report-in-risk-workspace.md)

