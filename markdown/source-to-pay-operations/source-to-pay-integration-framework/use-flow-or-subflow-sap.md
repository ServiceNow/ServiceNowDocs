---
title: Use a flow or subflow in SAP \(Outbound\)
description: A flow or subflow can be executed in SAP using the Workflow Studio. Follow these steps to run a flow or subflow.
locale: en-US
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 1
breadcrumb: [Use schedule flows, Use, Source-to-Pay integration with SAP, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Use a flow or subflow in SAP \(Outbound\)

A flow or subflow can be executed in SAP using the Workflow Studio. Follow these steps to run a flow or subflow.

## Before you begin

Role required:

-   sn\_fcms\_intg.admin - Write role
-   sn\_shop.procurement\_specialist, sn\_shop.shopper, sn\_fcms\_intg.admin - Read role

## About this task

Use an Outbound flow or subflow in SAP 

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  From the Workflow Studio home page, select **Flows**.

3.  Look up the **Flow** name or **SAP** application name using the filter icon, and select **Apply**.

    For example, SAP ECC, or SAP S4 HANA Cloud, or SAP HANA OData

4.  Select the required flow from the list.

    For example, select **Create non-purchase order invoice** flow.

    ![Overview of the Create non purchase order invoice flow](../../source-to-pay-operations/image/sap-integration-invoice-flow.png "Create non-purchase order invoice flow")

5.  In the Trigger field, specify the time and interval at which you want to run the scheduled flow automatically.

    This flow subsequently triggers subflows to automate tasks. To customize the sample flow, copy it to the desired application scope.

    **Note:** Don’t modify the trigger condition.

    The flow or subflow gets executed.


**Parent Topic:**[Use schedule flows in SAP](../concept/using-schedule-flows-sap.md)

**Related topics**  


[Copy a flow or subflow in SAP](copy-flow-or-subflow-sap.md)

