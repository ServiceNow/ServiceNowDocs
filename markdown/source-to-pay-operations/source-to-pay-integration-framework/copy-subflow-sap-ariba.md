---
title: Copy a flow or subflow in SAP Ariba
description: You can create a copy of the a flow or subflow, and modify based on your requirements.
locale: en-US
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use flows in SAP Ariba, Use, Source-to-Pay integration with SAP Ariba, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Copy a flow or subflow in SAP Ariba

You can create a copy of the a flow or subflow, and modify based on your requirements.

## Before you begin

Role required: sn\_fcms\_intg.admin, sn\_shop.procurement\_specialist, connection\_admin

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  From the Workflow Studio homepage, select **Flows**.

3.  Open the flow that you want to copy.

    For example, Update or Create Sourcing Event in SAP Ariba.

4.  Select **More actions**, and select **Copy flow**.

    **Important:** Perform this step only if you plan to customize or make specific changes to the flow.

    1.  In the Create a copy of this flow dialog, provide a name for the new flow.

        The Application is SAP Ariba Spoke, by default.

5.  Activate the flow or subflow.

    -   Make sure that the flow or subflow is available and activated in the base system.
    -   Activate the copied flow after making the required changes.
6.  Use the **Trigger Condition** for the flow or subflow.

    This flow or subflow is triggered when the condition **Integration status** is **New** is met.

    **Note:** Do not modify the trigger condition.

    ![Trigger conditions to create or update in SAP Ariba](../../source-to-pay-operations/image/sap-ariba-trigger-conditions.png "Trigger condition to create or update sourcing even in SAP Ariba")

    **Note:**

    Once data is pulled into staging tables, transform maps move data into target tables. For more details, refer to [Source-to-Pay integration framework transform maps and subflows](../concept/s2p-transform-maps-flows.md).

    You have successfully copied and executed the flow.


**Parent Topic:**[Use flows in SAP Ariba](../concept/use-flows-sap-ariba.md)

**Related topics**  


[Manually trigger flows or subflows in SAP Ariba \(Inbound\)](manually-trigger-subflows-sap-ariba.md)

[Use a flow or subflow in SAP Ariba \(Outbound\)](use-subflow-sap-ariba.md)

