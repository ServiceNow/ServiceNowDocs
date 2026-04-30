---
title: Publish an automation request
description: Publish an automation request from Automation Center to make the request ready for execution.
locale: en-US
release: xanadu
product: Automation Center
classification: automation-center
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Working with automations, Using Automation Center, Automation Center, Creating integrations with applications]
---

# Publish an automation request

Publish an automation request from Automation Center to make the request ready for execution.

## Before you begin

Create an automation request. For more information, see [Creating an automation request](create-automation-request.md).

To publish an automation request, the associated automation tasks must be in one of the following states:

-   **Closed complete**
-   **Closed incomplete**
-   **Closed skipped**

Verify that the state of the automation request is **In progress**, and map the required Automation CI records whose life-cycle stage status is **Published**. An automation CI record has details about an automation.

For details about mapping an automation request with automation CI record, see [Map automations with automation request](map-automation-to-req.md).

For all ServiceNow RPAs, an Automation CI record is available. For more details, see the RPA documentation.

For third-party RPAs, there are two scenarios:

-   For historical data of process and robot, you must manually create records in the corresponding CMDB Base Process table \(cmdb\_ci\_base-rpa\_process\) and CMBD Base Robot table \(cmdb\_ci\_base\_robot\).

-   For data of process and robot created after installing Automation Center, you must configure Rest API and send the process, robot, and execution details via Rest API and the records are created in the corresponding tables.


For further details, contact ServiceNow Customer Support.

Role required: sn\_ac.automation\_technical\_user or sn\_ac.automation\_admin

## Procedure

1.  Navigate to **All** &gt; **Automation Center** &gt; **Automation Center Home**.

2.  Select the list icon \(![List icon.](../images/autocenter-list-icon.png)\).

3.  On the **Lists** tab, under **Build**, select **All Automation Requests**.

4.  Open the automation request that you want to publish.

5.  In the form header, select **Publish**.

    **Warning:** After you publish an automation request, you can't change or delete the entries in the automation request form, associated automation tasks, or resources.


## Result

After you publish an automation request, the automation is ready for execution, which is the last stage in the automation request life cycle.

**Parent Topic:**[Working with automations](../concept/automations.md)

