---
title: Copy a flow or subflow in Coupa
description: Create a copy of a flow or subflow, make the necessary modifications, and then activate it.
locale: en-US
release: xanadu
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: task
last_updated: "2025-07-09"
reading_time_minutes: 1
breadcrumb: [Using Source-to-Pay integration with Coupa, Source-to-Pay integration with Coupa, Source-to-Pay integration with third-party applications, Source-to-Pay Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Copy a flow or subflow in Coupa

Create a copy of a flow or subflow, make the necessary modifications, and then activate it.

## Before you begin

Role required: sn\_fcms\_intg.integration\_user

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  From the Workflow Studio home page, select **Flows**.

3.  Open the flow that you want to copy.

4.  Select the more actions icon \(![More actions menu](../../../common/image/icon-ellipses.png)\).

5.  Select **Copy flow**.

    **Important:** Perform this step only if you plan to customize or make specific changes to the flow.

6.  Activate the flow or subflow.

    -   Make sure that the flow or subflow is available and activated on the base system.
    -   Activate the copied flow after making the required changes.
7.  Use the **Trigger Condition** for the flow or subflow.

    **Note:** After data is pulled into staging tables, the transform maps move data into target tables. For more details, refer to [Source-to-Pay integration framework transform maps and subflows](../../sourcing-procurement-operations/concept/s2p-transform-maps-flows.md).


**Parent Topic:**[Using Source-to-Pay integration with Coupa](../concept/using-source-to-pay-coupa-integration.md)

**Related topics**  


[Trigger a flow or subflow in Coupa](manually-trigger-subflows-coupa.md)

[View the execution status of a flow](view-executed-flow-status.md)

[Use a flow or subflow in Coupa \(outbound\)](use-flow-or-subflow-coupa.md)

