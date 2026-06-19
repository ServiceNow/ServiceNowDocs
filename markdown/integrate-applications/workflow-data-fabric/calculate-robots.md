---
title: Calculate the number of robots in RPA Hub
description: Calculate the number of robots that you need to complete an unattended bot process execution that is based on the allocation type, for example, the SLA Based and Percentage Reduction.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/calculate-robots.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Robot pool, Use, RPA Hub, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Calculate the number of robots in RPA Hub

Calculate the number of robots that you need to complete an unattended bot process execution that is based on the allocation type, for example, the SLA Based and Percentage Reduction.

## Before you begin

Familiarize yourself with robot pool concepts. For more information, see [Robot pool in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/robot-pool-rpa.md).

Create a robot pool. For more information, see [Create a robot pool in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/create-robot-pool.md).

Enable robot pool for the bot process. For more information, see [Bot Process form in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/select-botprocess.md).

Associate a queue to the bot process. For more information, see [c to the bot process from the related list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/associate-queue-botprocess.md).

Define Average Handling Time \(AHT\) details on the queue form. For more information, see [Queue form in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/queue-form.md).

Ensure that multiple queues are not associated to a bot process.

Ensure that the pending work items are available in the queue.

If you select the allocation type as SLA Based on the Bot Process form, ensure that the work items must contain a Service Level Agreement \(SLA\).

If you select the **Percentage Reduction** allocation type on the Bot Process form, make sure that you define a value in the **Percentage Reduction** field.

Role required: sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

## About this task

If the value of the calculation is in decimals, the value is rounded off to the next higher value. For example, if the calculation result is 2.2 robots, the result that is displayed is 3. That means that 3 robots are required to execute the bot process.

queryConditions included in the PickWorkItem component are considered for calculating the number of robots required to complete an unattended bot process execution, if the bot process is enabled with robot pool. For more information about PickWorkItem component, see [Queue connector methods](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/connectors-queues-methods.md).

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(\[Omitted image "rpahublist-icon.png"\] Alt text: List icon.\).

3.  On the **Lists** tab, under **Build**, select **Bot Process**.

4.  Open a bot process.

5.  In the form header, select the down arrow in the **Start Process** button.

6.  Select **Calculate**.

    A message is displayed about the number of robots that are required to execute the bot process.


**Parent Topic:**[Robot pool in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/robot-pool-rpa.md)

