---
title: Handle errors in RPA Desktop Design Studio
description: Handle errors at the component level and activity level in RPA Desktop Design Studio. You can use the Error Handler option to handle the errors that occur during an automation execution.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Handle errors in RPA Desktop Design Studio

Handle errors at the component level and activity level in RPA Desktop Design Studio. You can use the **Error Handler** option to handle the errors that occur during an automation execution.

## Before you begin

Configure a component. For more information, see [Use a component in RPA Desktop Design Studio](configure-components.md).

Create an activity. For more information, see [Create and use an activity in RPA Desktop Design Studio](configure-activity-rpa-studio.md).

Role required: none

## Procedure

1.  In the RPA Desktop Design Studio, select one of the following options to handle errors either at a component level or at an activity level.

<table id="choicetable_r3f_bsy_vqb"><thead><tr><th align="left" id="d551884e89">

Option

</th><th align="left" id="d551884e92">

Action and description

</th></tr></thead><tbody><tr><td id="d551884e98">

**To handle errors at a component level**

</td><td>

On the Design surface, right-click the component title bar and select **Error Handler** to open the ERROR HANDLER dialog box.

</td></tr><tr><td id="d551884e110">

**To handle errors at an activity level**

</td><td>

In the Project Explorer pane, right-click an activity and select **Error Handler** to open the ERROR HANDLER dialog box.By default, error handling at the activity level applies to all components within that activity, except for the components where errors handling is explicitly configured.

</td></tr></tbody>
</table>2.  In the ERROR HANDLER dialog box, from the On Error list, select any one of the following error handler types:

<table id="table_hnm_vtk_4rb"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Inherit

</td><td>

Inherits the error handling settings that are configured at the parent level.Within a component, an activity that the component belongs to, is the parent. Within an activity, the parent is the activity where the activity is being called from.

 This option is the default for error handling at component level.

</td></tr><tr><td>

Stop

</td><td>

Stops the execution if error occurs.This option is the default for error handling at the activity level.

</td></tr><tr><td>

Continue

</td><td>

Continues the execution if an error occurs.

</td></tr><tr><td>

Retry

</td><td>

Retries the execution of the component where the error occurs.After selecting the **Retry** option, the following fields appear:

-   In the **Max Retries** field, you can define the number of retries.
-   In the **Retry Delay** field, you can define the delay between each retry.
 The automation stops with an error if the Maximum retires count is exhausted during an execution.

 In the **On Error After Retry** field, you can select an option such as **Inherit**, **Stop**, and **Continue** to provide further steps if an error persists after a defined retry has failed.

</td></tr></tbody>
</table>3.  Click **OK**.


**Parent Topic:**[Using automations](../concept/rpa-studio-use.md)

