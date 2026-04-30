---
title: Use the GracefulStop component
description: Verify that an automation from RPA Hub doesn't stop abruptly by using the GracefulStop component in RPA Desktop Design Studio. With this component, you can define a secure termination point within an automation process and automate housekeeping activities such as closing in-use applications or performing clean-up operations.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Common, RPA Hub, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Use the GracefulStop component

Verify that an automation from RPA Hub doesn't stop abruptly by using the GracefulStop component in RPA Desktop Design Studio. With this component, you can define a secure termination point within an automation process and automate housekeeping activities such as closing in-use applications or performing clean-up operations.

## Before you begin

Make sure that you analyze the automation for scenarios where you can stop the automation gracefully and perform the clean-up tasks such as closing in-use applications.

Role required: None

## About this task

Previously, when you selected the **Stop Process** button on a bot process in RPA Hub, the robots exited the automation abruptly. This process may have caused data inconsistencies. You can now exit the automation smoothly by using the GracefulStop component. For more information on how the GracefuStop component works for an automation in RPA Hub, see [Using Graceful Stop functionality in RPA Hub](../../rpa-hub/concept/graceful-stop-rpa.md).

**Note:** The GracefulStop component is available only for unattended automations.

## Procedure

1.  In the Toolbox pane, navigate to **RPA hub** &gt; **Common**.

2.  Drag the GracefulStop component to the Design surface to add it as part of your automation.

3.  Connect the component to the sequence that stops the automation gracefully by using the Control-In port.

4.  Use the Return data port to connect to the steps that the user performs to initiate a graceful stop from RPA Hub.

    For example, let's consider a scenario where automation copies the employee details from a Microsoft Excel sheet to an Oracle application. By using the Return data port, the current transaction completes and successfully terminates the automation.

    **Important:** Make sure that the GracefulStop component meets the following conditions:

    -   The Control-In port must have a connection.
    -   The Return data port must have a connection or it must be mapped to a variable.

        The Graceful stop option is available in RPA Hub to only those automations that satisfy these conditions.

    When you use the GracefulStop component from RPA Desktop Design Studio, the component returns a false value. By selecting the GracefulStop toggle for the **Stop process** option in a bot process in RPA Hub, the component returns a true value. You can then stop the automation. If the automation path leads to a safe termination point, the automation is gracefully exited. For more information about stopping a bot process in RPA Hub, see [Stop an unattended bot process in RPA Hub](../../rpa-hub/task/stop-bot-process.md).


## What to do next

Publish the automation project. For more information on how to publish an automation project, see [Publish an automation project in RPA Desktop Design Studio](publish-automation-project.md).

**Parent Topic:**[Common](../concept/common_components.md)

