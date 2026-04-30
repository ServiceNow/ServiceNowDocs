---
title: Configure SAP for ERP-CM
description: Enable SQLM \(SQL Monitor\) on the productive system and confirm that ST03 \(Workload Monitor\) is collected for daily workloads before you can install ERP Semantic Mining \(ERP-CM\).
locale: en-US
release: yokohama
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring ERP Semantic Mining, ERP Semantic Mining \(ERP-CM\), Building low-code applications, Developing your application, Building applications]
---

# Configure SAP for ERP-CM

Enable SQLM \(SQL Monitor\) on the productive system and confirm that ST03 \(Workload Monitor\) is collected for daily workloads before you can install ERP Semantic Mining \(ERP-CM\).

## Before you begin

Role required: none

## About this task

**Warning:** If you don't perform the SAP configurations from this procedure, and if there's no data in SAP, then ERP-CM won't work.

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

