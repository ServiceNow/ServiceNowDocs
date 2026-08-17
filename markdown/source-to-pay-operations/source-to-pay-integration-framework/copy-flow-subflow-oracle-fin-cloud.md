---
title: Copy a flow or subflow in Oracle Financial Cloud
description: You can create a copy of the a flow or subflow and make the necessary modifications. Use the following steps to activate a flow or subflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/source-to-pay-integration-framework/copy-flow-subflow-oracle-fin-cloud.html
release: zurich
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use schedule flows in Oracle Financial Cloud, Use, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Copy a flow or subflow in Oracle Financial Cloud

You can create a copy of the a flow or subflow and make the necessary modifications. Use the following steps to activate a flow or subflow.

\[Omitted video\] Description: Video demonstrating how to copy a flow or subflow in Oracle Financial Cloud

## Before you begin

Role required: sn\_fcms\_intg.integration\_user

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  From the Workflow Studio homepage, select **Flows**.

3.  Open the flow that you want to copy.

4.  Select **More actions**, and select **Copy flow**.

    **Important:** Perform this step only if you plan to customize or make specific changes to the flow.

    \[Omitted image "oracle-fin-copy-subflow.png"\] Alt text: Copy a flow or subflow in Oracle Financial Cloud

5.  Activate the flow or subflow.

    -   Make sure that the flow or subflow is available and activated on the base system.
    -   Activate the copied flow after making the required changes.
6.  Use the Subflow **Inputs &amp; Outputs** for providing your inputs and outputs as per your requirements.

    **Note:**

    -   Don't modify the trigger condition.
    -   Once data is pulled into staging tables, transform maps move data into target tables. For more details, refer to [Source-to-Pay integration framework transform maps and subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/source-to-pay-integration-framework/s2p-transform-maps-flows.md)
7.  Select **Done**.

8.  Select **Publish** to publish the subflow.

9.  Select **Publish** again to confirm the publication of the subflow.

    You have successfully copied and executed the flow.


