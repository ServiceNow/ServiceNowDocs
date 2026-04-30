---
title: Configure matrix report registry to set up base table for audit matrix report
description: Configure the Matrix report registry to select the base table. You can create a relationship with the target table to configure the details of the report for an audit-related record or a landing page.
locale: en-US
release: xanadu
product: Audit Management
classification: audit-management
topic_type: task
last_updated: "2025-01-20"
reading_time_minutes: 1
breadcrumb: [Matrix report in Audit Workspace, Audit Workspace for the Auditor, Audit Workspace, Audit Management, Governance, Risk, and Compliance]
---

# Configure matrix report registry to set up base table for audit matrix report

Configure the Matrix report registry to select the base table. You can create a relationship with the target table to configure the details of the report for an audit-related record or a landing page.

## Before you begin

Role required: sn\_matrix\_report.admin

## Procedure

1.  Navigate to **All** &gt; **Matrix report** &gt; **Matrix report registry**.

2.  Select **New**.

3.  Enter the name of the Matrix report registry in the **Name** field.

4.  Select the base table from the **Base table** list.

5.  Select **Submit**.

6.  Select the matrix report registry that you created by clicking the **Name**.

    The base level of the configuration is auto-populated, which contains the base target table and you can select any filter conditions. For the next level configuration, add new relationships between the base table and a target table for the matrix report.

7.  In the Matrix relationships related list, select **New**.

8.  On the form, fill in the fields.

    For a description of the field values, see [Matrix relationship form](../reference/matrix-rel-audit-report-ws.md).

9.  Select **Submit**.

    You have configured the base table, which is the level 0 of the matrix report configuration. You can add new configurations as well. For example, if you have selected the base table as Risk, then you can add configurations such as risk related to controls, which would be level 1. For level 2, you can configure a relationship between controls and issues. Parent record as source helps to identify the record from which the data is taken. The Source table and the Relationship cannot be the same in the Matrix report registry.

    To configure column heads for the matrix report, see, [Configure target table fields as columns for matrix report](matrix-report-relationship-audit-ws.md).


