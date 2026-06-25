---
title: Use a flow or subflow in Oracle EBS \(Outbound\)
description: A flow or subflow can be executed in Oracle EBS using the Workflow Studio. Follow these steps to run a flow or subflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/use-flow-or-subflow-oracle-ebs.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: task
last_updated: "2026-06-25"
reading_time_minutes: 1
breadcrumb: [Use schedule flows in Oracle EBS, Use, Source-to-Pay integration with Oracle EBS, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Use a flow or subflow in Oracle EBS \(Outbound\)

A flow or subflow can be executed in Oracle EBS using the Workflow Studio. Follow these steps to run a flow or subflow.

## Before you begin

Role required: sn\_fcms\_intg.integration\_user

## About this task

\[Omitted video\] Description: Use an Outbound flow or subflow in Oracle EBS

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  From the Workflow Studio home page, select **Flows**.

3.  Look up the **Flow** name or **Oracle EBS** application name using the filter icon, and select **Apply**.

4.  Select the required flow from the list.

    For example, select **Create or update or cancel purchase order** flow.

    \[Omitted image "oracle-ebs-create-po-flow.png"\] Alt text: Overview of the Create or update purchase order flow

5.  In the Trigger field, specify the time and interval at which you want to run the scheduled flow automatically.

    This flow subsequently triggers subflows to automate tasks. To customize the sample flow, copy it to the desired application scope.

    **Note:** Don’t modify the trigger condition.

    The flow or subflow gets executed.


**Parent Topic:**[Use schedule flows in Oracle EBS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/using-schedule-flows-oracle-ebs.md)

**Related topics**  


[Manually trigger flows or subflows in Oracle EBS \(Inbound\)]()

[Copy a flow or subflow in Oracle EBS]()

