---
title: Use a flow or subflow in Coupa \(outbound\)
description: A flow or subflow can be executed in Coupa using the Workflow Studio.
locale: en-US
release: yokohama
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, Source-to-Pay integration with Coupa, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Use a flow or subflow in Coupa \(outbound\)

A flow or subflow can be executed in Coupa using the Workflow Studio.

## Before you begin

Role required: sn\_fcms\_intg.integration\_user

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  From the Workflow Studio home page, select **Flows**.

3.  Look up the **Flow** name or **Coupa** application name using the filter icon, and select **Apply**.

4.  Select the required flow from the list.

    ![Overview of the Award Purchase flow](../image/coupa-integration-use-flow.png "Award Purchase flow")

5.  In the **Trigger** field, specify the time and interval at which you want to run the scheduled flow automatically.

    This flow subsequently triggers subflows to automate tasks. To customize the sample flow, copy it to the desired application scope.

    **Note:** Don’t modify the trigger condition.


## Result

The flow or subflow gets executed.

**Parent Topic:**[Use Source-to-Pay integration with Coupa](../concept/using-source-to-pay-coupa-integration.md)

**Related topics**  


[Trigger a flow or subflow in Coupa](manually-trigger-subflows-coupa.md)

[View the execution status of a flow](view-executed-flow-status.md)

[Copy a flow or subflow in Coupa](copy-flow-or-subflow-coupa.md)

