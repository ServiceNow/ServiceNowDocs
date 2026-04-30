---
title: Create contract-level KPIs from KPI management
description: You can add contract-level KPIs for a supplier from the KPI management tab of the supplier page. Contract-level KPIs are defined under their respective supplier-level KPIs.
locale: en-US
release: zurich
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2025-04-15"
reading_time_minutes: 1
breadcrumb: [Configure Supplier Relationship and Performance Management, Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Create contract-level KPIs from KPI management

You can add contract-level KPIs for a supplier from the **KPI management** tab of the supplier page. Contract-level KPIs are defined under their respective supplier-level KPIs.

## Before you begin

Role required: admin

You can add contract-level KPIs only if you have installed the Sourcing and Purchasing Automation \(com.snc.sn\_pr\) and Source-to-Pay Common Architecture \(com.snc.sn\_shop\) plugins.

## Procedure

1.  Navigate to **All** &gt; **Supplier Lifecycle Operations** &gt; **Source-to-Pay Workspace**.

2.  Under **Quick actions**, select **Manage my suppliers**.

3.  Under **My suppliers**, select the legal name of the supplier.

4.  Select the **KPI management** tab.

5.  Select **Add**.

6.  Select the collection level as **Contract level**.

    ![Select collection level dialog box](../image/contract-level.png)

7.  Select the applicable contracts from the list of available contracts.

8.  Select a KPI template from the list of available KPI templates.

9.  Select **Add**.

    The corresponding KPI records and KPI collection tasks are created.

    **Note:**

    -   All contract-level KPIs are defined under their respective supplier-level KPIs. If a supplier-level KPI doesn’t exist for a newly created contract-level KPI, a corresponding parent supplier-level KPI is also created.
    -   Aggregated values from contract-level KPIs must fall in the threshold ranges of their respective supplier-level KPIs. Therefore, supplier-level KPI thresholds must be defined for all possible aggregated values of contract-level KPIs, otherwise the KPI data won’t be generated.

**Parent Topic:**[Configure Supplier Relationship and Performance Management](../concept/configuring-supplier-performance-mgmt.md)

