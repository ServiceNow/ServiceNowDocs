---
title: Use the Log component
description: Capture custom messages as automation logs by using the Log component in an automation in RPA Desktop Design Studio. With this component, you can write custom messages as automation logs and view them from a unified space so that you can track the progress of an automation.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [RPA Hub, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the Log component

Capture custom messages as automation logs by using the Log component in an automation in RPA Desktop Design Studio. With this component, you can write custom messages as automation logs and view them from a unified space so that you can track the progress of an automation.

## Before you begin

Make sure that you enable the **Track Execution Automation Logs** option from a bot process. For more information on how to enable Track Execution Logs, see [Bot Process form in RPA Hub](../../rpa-hub/reference/bot-process-form.md).

Role required: none

## About this task

Previously, the messages from the Log component were updated to the product error log files in the machine where the automation was executed.

Starting from the Vancouver release, the log messages from the automations that execute on the RPA Desktop Design Studio, the attended robots, and the unattended robots are written to the **Message** field in the Automation logs table of a process job in RPA Hub.

You aren’t required to upgrade the plugin version of the older automations. For more information about the list components that are upgraded with RPA Desktop Design Studio, Attended Robot, and Unattended Robot, see [List of components compatible with latest version](../reference/list-components-upgrade.md).

## Procedure

1.  In the Toolbox pane, navigate to **RPA Hub** &gt; **Log**.

2.  Drag the **Log** component to the Design surface.

3.  Configure the **Message** \(string\) field by entering a message or capturing the output string from a previous component or method.

    For example, if the automation is successful, you can enter the string `Success` or capture the string result from a previously executed component or method.

4.  If you want to classify the message, configure the **Log level** property from the Properties explorer.

    You can classify the message as one of the following types:

    -   Info
    -   Warning
    -   Error
    -   Exception

        **Important:** In the previous version of RPA Desktop Design Studio, the **Error image** and **Verbose** options were available. If you open an older automation project in the Vancouver release of RPA Desktop Design Studio, these options are converted to the type **Error**.

    For more information on how to configure the remaining properties of the Log component, see [Properties of the General components](../reference/Properties-general-components.md).

5.  To test the component, under the **DESIGN** tab, select **Run**.

    **Note:** When you run the Log component from RPA Desktop Design Studio, no message updates to RPA Hub because no process job is associated to it.


**Parent Topic:**[RPA Hub](../concept/rpa-hub.md)

