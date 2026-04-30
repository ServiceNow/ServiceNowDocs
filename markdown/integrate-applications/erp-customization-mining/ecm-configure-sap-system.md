---
title: Configure SAP for ERP Semantic Mining
description: Enable SQLM \(SQL Monitor\) on the productive system and confirm that ST03 \(Workload Monitor\) is collected for daily workloads before you can install ERP Semantic Mining.
locale: en-US
release: zurich
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, ERP Semantic Mining overview, Workflow Data Fabric]
---

# Configure SAP for ERP Semantic Mining

Enable SQLM \(SQL Monitor\) on the productive system and confirm that ST03 \(Workload Monitor\) is collected for daily workloads before you can install ERP Semantic Mining.

## Before you begin

Role required: none

**Important:** Starting with the Zurich release, ERP Semantic Mining is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

## About this task

**Warning:** You must perform the SAP configurations in this procedure and have data in SAP for ERP Semantic Mining to work correctly.

## Procedure

1.  Collect SQLM information from the productive environment by enabling SQLM in the SAP system.

    1.  In the production system, start the transaction SQLM.

        For more information, refer to the [SAP SQL Monitor documentation](https://help.sap.com/docs/).

    2.  Confirm that the **Activation state** field is set to **Globally active**.

    3.  If SQLM isn't active, start the transaction SQLM again.

    4.  Navigate to **SQL Monitor** &gt; **Setting** &gt; **General Settings**.

    5.  Confirm that the **Delete Older Than \[Days\]** option is set to a minimum of `365` days, and select **Confirm**.

    6.  Activate the setting by selecting **All Servers**.

2.  Verify that ST03 is collected for daily workloads from the productive environments.

    1.  In the production system, start the transaction ST03.

    2.  Verify that the **Workload data** field is set to **Daily**.


**Parent Topic:**[Configuring ERP Semantic Mining](../concept/configuring-ecm.md)

