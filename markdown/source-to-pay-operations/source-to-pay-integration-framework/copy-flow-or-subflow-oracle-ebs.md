---
title: Copy a flow or subflow in Oracle EBS
description: You can create a copy of the a flow or subflow and make the necessary modifications. Use the following steps to activate a flow or subflow.
locale: en-US
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 1
breadcrumb: [Use schedule flows in Oracle EBS, Use, Source-to-Pay integration with Oracle EBS, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Copy a flow or subflow in Oracle EBS

You can create a copy of the a flow or subflow and make the necessary modifications. Use the following steps to activate a flow or subflow.

## Before you begin

Role required: sn\_fcms\_intg.integration\_user

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  From the Workflow Studio homepage, select **Flows**.

3.  Open the flow that you want to copy.

4.  Select **More actions**, and select **Copy flow**.

    **Important:** Perform this step only if you plan to customize or make specific changes to the flow.

    ![Overview of the Create or update purchase order flow](../../source-to-pay-operations/image/oracle-ebs-create-po-flow.png "Create or update purchase order flow")

5.  Activate the flow or subflow.

    -   Make sure that the flow or subflow is available and activated on the base system.
    -   Activate the copied flow after making the required changes.
6.  Use the **Trigger Condition** for the flow or subflow.

    This flow or subflow is triggered and associated with the purchase order when the following conditions are met:

    -   **Legal entity . ERP source . Active** is **true**.
    -   **Legal entity . ERP source . ERP Source** is **not empty**.
    -   **Status** is **Pending Submission**
    **Note:** Do not modify the trigger condition.

    ![Trigger conditions for create purchase order](../../source-to-pay-operations/image/oracle-ebs-create-po.png)

    **Note:** Once data is pulled into staging tables, transform maps move data into target tables. For more details, refer to [Source-to-Pay integration framework transform maps and subflows](../concept/s2p-transform-maps-flows.md)

    You have successfully copied and executed the flow.


**Parent Topic:**[Use schedule flows in Oracle EBS](../concept/using-schedule-flows-oracle-ebs.md)

**Related topics**  


[Manually trigger flows or subflows in Oracle EBS \(Inbound\)](manually-trigger-subflows-oracle-ebs.md)

[Use a flow or subflow in Oracle EBS \(Outbound\)](use-flow-or-subflow-oracle-ebs.md)

