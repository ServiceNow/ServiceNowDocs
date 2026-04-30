---
title: Setting idle state
description: An agent in the idle state is available to receive or initiate work. Customize this state by configuring call controls such as the phone keypad for outbound calls, directory access, and the logout feature to manage the CCaaS platform session.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-10-03"
reading_time_minutes: 1
breadcrumb: [Set up the Voice Controls Simulator tool, Voice Controls Simulator tool, Integrating with contact centers, Integrate, Customer Service Management]
---

# Setting idle state

An agent in the idle state is available to receive or initiate work. Customize this state by configuring call controls such as the phone keypad for outbound calls, directory access, and the logout feature to manage the CCaaS platform session.

## Before you begin

Role required: admin

![Set idle state capabilities in the simulator](../image/int-set-idle-state.png "Set idle state capabilities")

## Procedure

1.  Configure display fields by entering a key and value in the **Key to display** and **Value to display** fields.

    This value is set by the contact center admin. For example, Key = `Selected Queue`, and Value = `Customer Inquiries`.

2.  Select the **Controls** Options.

3.  Select to enable the **Phone directory** option to display the **Queues**, **Agents**, **External numbers**, and **Direct dial** tabs.

4.  Use the **Edit** icon to update entries.

    By default, the **Outbound call**, **Logout**, and **Phone directory** options are enabled. You can clear any options as needed. See [Configuring Transfer capabilities](configure-transfer-capability.md).

5.  Select **Save and continue** to set the chosen options that opens the Global call window with the updated values.

    The window displays icons for the enabled features. The **Phone directory** feature, if not selected, appears inactive.

6.  Configure call controls by selecting options such as **Mute**, **Hold**, **Transfer**, **Flag**, **DTMF**, and **End call**.

7.  Configure **Recording** controls by selecting options such as **Start**, **Stop**, **Pause**, or **Resume recording**.

8.  Select **Save and continue** and move on to the next step for adding participants.

    -   Select **Clear all** to remove all input data for the section you’re updating.
    -   Select the **Logout** and **Reset** options to return to the idle state setup.

## What to do next

If you enable **Transfer**, the simulator guides you through the transfer capabilities setup. If you choose not to select the **Transfer** capability, select **Continue** to proceed to adding participants. See [Configuring Transfer capabilities](configure-transfer-capability.md).

