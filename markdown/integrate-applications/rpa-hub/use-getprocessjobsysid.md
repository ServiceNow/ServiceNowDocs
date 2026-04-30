---
title: Use the GetProcessJobSysID component
description: Retrieves the process job SysID of a process job record when an automation gets executed by a robot. By using the GetProcessJobSysID component in the RPA Desktop Design Studio application, you can identify when the robot is in a free state to execute a process or you can identify the state of the process job.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Common, RPA Hub, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the GetProcessJobSysID component

Retrieves the process job SysID of a process job record when an automation gets executed by a robot. By using the GetProcessJobSysID component in the RPA Desktop Design Studio application, you can identify when the robot is in a free state to execute a process or you can identify the state of the process job.

## Before you begin

Role required: none

## About this task

If a robot is working on an automation, a process job record for the execution is created in RPA Hub. The robot is then moved to the Busy state. For more information on the different states of a robot, see [Robot states form](../../rpa-hub/task/edit-robot.md#table_dvx_x3l_rrb). If you try to execute another automation in the Busy state against this robot, the automation doesn’t execute and a process job record is created in the Skipped state. Use the process job SysID to identify when the robot is free and to assign the skipped process jobs to the robot for execution.

The process job SysID can be a passed as an input parameter to a subflow when the subflow is used to check the completion of a process job. When the process job is completed, you can start a new process on the same robot.

**Important:**

You can’t retrieve the process job SysID by running the GetProcessJobSysID component from RPA Desktop Design Studio. The component can retrieve the process job SysID only during the execution of an automation by a robot. If you run the component from RPA Desktop Design Studio, an error is displayed.

## Procedure

1.  In the Toolbox pane, navigate to **RPA Hub** &gt; **Common**.

2.  Drag the **GetProcessJobSysID** component to the Design surface to add it as part of your automation.

3.  Connect the data and control ports of the GetProcessJobSysID component to the other components as described in the following table.

    |Port name|Port type|Port description|
    |---------|---------|----------------|
    |SysID|Data out|Process job system ID of the execution when the automation gets executed by a robot in a Windows machine. Returns a string value.|
    |Control In|Not applicable|Connects to the Control Out port of one or more components.|
    |Control Out|Not applicable|Connects to the Control In port of another component or the default end component.|

4.  To test the component, right-click the component and select **Run From Here**.

    You can also run the automation by selecting **Run** from the **Design** tab.


**Parent Topic:**[Common](../concept/common_components.md)

