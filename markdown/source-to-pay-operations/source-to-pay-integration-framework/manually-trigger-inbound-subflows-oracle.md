---
title: Manually trigger flows or subflows in Oracle EBS \(Inbound\)
description: You can manually trigger flows or subflows in Oracle EBS on demand. Follow these steps to manually trigger a flow or subflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/manually-trigger-inbound-subflows-oracle.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: task
last_updated: "2026-06-25"
reading_time_minutes: 1
breadcrumb: [Use schedule flows in Oracle EBS, Use, Source-to-Pay integration with Oracle EBS, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Manually trigger flows or subflows in Oracle EBS \(Inbound\)

You can manually trigger flows or subflows in Oracle EBS on demand. Follow these steps to manually trigger a flow or subflow.

## Before you begin

Role required: sn\_fcms\_intg.integration\_user

## About this task

\[Omitted video\] Description: Manually trigger flows or subflows in Oracle EBS \(Inbound\)

## Procedure

1.  Navigate to **All** &gt; **Finance – ERP Integration** &gt; **ERP Source Configuration**.

2.  In the ERP Configurations view, select the **Oracle EBS** ERP source to manually trigger the flows or subflows.

3.  In the Integration Services list, select the subflows that you want to manually trigger.

    \[Omitted image "manual-trigger-flow-oracle.png"\] Alt text: Manually trigger flows or subflows in Oracle EBS \(Inbound\)

4.  Select **Run job** to trigger the flow or subflow.

5.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

6.  From the Workflow Studio home page, select the **Operations** tab and then select **Flows** tab.

    The list of flow executions appear. You can look up the status of the flows or subflows that you triggered. If there were any errors during execution, you can view them under the processing message column.

7.  Navigate back to the **Homepage** tab, and select **Flows** or **Subflows**.

8.  Look up the **Flow** or **Subflow** name or **Oracle EBS** application name using the filter icon, and select **Apply**.

    You can view the flows or subflows that you triggered.

    \[Omitted image "manual-trigger-ws-oracle.png"\] Alt text: View the list of Flows or subflows in Workflow Studio

9.  You can use the trigger condition as a part of the base system to execute the flow or subflow.

    **Note:** Don’t modify the trigger condition.

    The flow or subflow gets executed.


**Parent Topic:**[Use schedule flows in Oracle EBS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/using-schedule-flows-oracle-ebs.md)

**Related topics**  


[Use a flow or subflow in Oracle EBS \(Outbound\)]()

[Copy a flow or subflow in Oracle EBS]()

