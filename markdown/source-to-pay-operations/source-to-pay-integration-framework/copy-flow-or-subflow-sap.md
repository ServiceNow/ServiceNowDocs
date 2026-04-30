---
title: Copy a flow or subflow in SAP ECC and SAP S4 HANA
description: You can create a copy of the a flow or subflow and make the necessary modifications. Use the following steps to activate a flow or subflow.
locale: en-US
release: xanadu
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Use schedule flows in SAP ECC and SAP S4 HANA, Using Source-to-Pay integration with SAP ECC and SAP S4 HANA, Source-to-Pay integration with SAP ECC and SAP S4 HANA, Source-to-Pay integration with third-party applications, Source-to-Pay Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Copy a flow or subflow in SAP ECC and SAP S4 HANA

You can create a copy of the a flow or subflow and make the necessary modifications. Use the following steps to activate a flow or subflow.

## Before you begin

Role required: sn\_fcms\_intg.integration\_user

## About this task

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  From the Workflow Studio homepage, select **Flows**.

3.  Open the flow that you want to copy.

4.  Click the ![More actions menu](../../../common/image/icon-ellipses.png) more actions icon, and select **Copy flow**.

    **Important:** Perform this step only if you plan to customize or make specific changes to the flow.

    ![Copy of a Create non-purchase order flow](../image/sap-integration-copy-flow.png "Copy of a Create non-purchase order flow")

5.  Activate the flow or subflow.

    -   Make sure that the flow or subflow is available and activated on the base system.
    -   Activate the copied flow after making the required changes.
6.  Use the **Trigger Condition** for the flow or subflow.

    This flow or subflow is triggered and associated with the purchase order when the following conditions are met:

    -   **Legal entity . ERP source . Active** is **true**.
    -   **Legal entity . ERP source . ERP Source** is **not empty**.
    -   **Status** is **Pending Submission**
    **Note:** Do not modify the trigger condition.

    ![Trigger conditions for Creating a non-purchase order invoice flow](../image/sap-integration-flow-trigger.png "Trigger conditions for Creating a non-purchase order invoice flow")

    **Note:**

    Once data is pulled into staging tables, transform maps move data into target tables. For more details, refer to [Source-to-Pay integration framework transform maps and subflows](../../sourcing-procurement-operations/concept/s2p-transform-maps-flows.md).


**Parent Topic:**[Use schedule flows in SAP ECC and SAP S4 HANA](../concept/using-schedule-flows-sap.md)

**Related topics**  


[Use a flow or subflow in SAP ECC and SAP S4 HANA \(Outbound\)](use-flow-or-subflow-sap.md)

