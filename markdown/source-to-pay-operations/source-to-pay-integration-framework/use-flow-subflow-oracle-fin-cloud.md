---
title: Use a flow or subflow in Oracle Financial Cloud \(Outbound\)
description: A flow or subflow can be executed in Oracle Financial Cloud using the Workflow Studio. Follow these steps to run a flow or subflow.
locale: en-US
release: yokohama
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: task
last_updated: "2025-11-14"
reading_time_minutes: 1
breadcrumb: [Use schedule flows in Oracle Financial Cloud, Use, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Use a flow or subflow in Oracle Financial Cloud \(Outbound\)

A flow or subflow can be executed in Oracle Financial Cloud using the Workflow Studio. Follow these steps to run a flow or subflow.

## Before you begin

Role required: sn\_fcms\_intg.integration\_user

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  From the Workflow Studio home page, select **Flows**.

3.  Look up the **Flow** name or **Oracle Financial Cloud** application name using the filter icon, and select **Apply**.

4.  Select the required flow from the list.

    For example, select **Create or update supplier location** flow.

5.  In the Trigger field, specify the time and interval at which you want to run the scheduled flow automatically.

    This flow subsequently triggers subflows to automate tasks. To customize the sample flow, copy it to the desired application scope.

    **Note:** Don’t modify the trigger condition.

    The flow or subflow is executed.


