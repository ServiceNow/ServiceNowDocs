---
title: Copy a flow or subflow in Coupa
description: Create a copy of a flow or subflow, make the necessary modifications, and then activate it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/copy-flow-or-subflow-coupa.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, Source-to-Pay integration with Coupa, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Copy a flow or subflow in Coupa

Create a copy of a flow or subflow, make the necessary modifications, and then activate it.

## Before you begin

Role required: sn\_fcms\_intg.integration\_user

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  From the Workflow Studio home page, select **Flows**.

3.  Open the flow that you want to copy.

4.  Select **More actions**, and select **Copy flow**.

    **Important:** Perform this step only if you plan to customize or make specific changes to the flow.

    \[Omitted image "coupa-integration-copy-flow.png"\] Alt text: Copy of a Award Purchase flow

5.  Activate the flow or subflow:

    -   Make sure that the flow or subflow is available and activated on the base system.
    -   Activate the copied flow after making the required changes.
6.  Use the **Trigger Condition** for the flow or subflow.

    **Note:** After data is pulled into staging tables, the transform maps move data into target tables. For more details, refer to [Source-to-Pay integration framework transform maps and subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/s2p-transform-maps-flows.md).

    You have successfully copied and executed the flow.


**Parent Topic:**[Use Source-to-Pay integration with Coupa](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/using-source-to-pay-coupa-integration.md)

**Related topics**  


[Trigger a flow or subflow in Coupa]()

[View the execution status of a flow]()

[Use a flow or subflow in Coupa \(outbound\)]()

