---
title: Configure the C\#.Net connector
description: Write and validate custom C\#.Net scripts and execute them as part of your automation by using the C\#.Net connector in RPA Desktop Design Studio.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [C\#.Net, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Configure the C\#.Net connector

Write and validate custom C\#.Net scripts and execute them as part of your automation by using the C\#.Net connector in RPA Desktop Design Studio.

## Before you begin

Ensure you have installed the Scripting plugin on the RPA Desktop Design Studio. To install, see [Manage plugins in RPA Desktop Design Studio](install-plugins-rpa-studio.md).

Role required: Developer

## Procedure

1.  In the Toolbox pane, navigate to **Connectors** &gt; **C\#.NET**.

2.  Drag the C\#.Net connector to **Global Objects** in the Project Explorer pane.

3.  Right-click the C\#.Net connector in **Global Objects** and select **Configure**.

    The Script Editor window is displayed.

4.  Enter the custom script in the Script pane.

    ![Script pane in Script Editor](../image/cscript-editor.png "Script pane in Script Editor")

5.  Select **Add Reference** from the **References** tab section if you want to add Dynamic-link library \(DLL\) references to your custom script.

    You can select the references from the Reference Manager window and also from your computer.

6.  Select **Validate**.

    If your custom script has any errors, it is displayed in the Errors pane. Resolve the errors and select **Validate** to check for errors again.

    ![Error pane for Script Editor](../image/cscript-error.PNG "Error pane for Script Editor")

7.  Click **OK**.

    If you want to save the changes, select **Yes**. An error validation is performed again and the changes are saved. If you want to discard the changes, select **No**.


## What to do next

The custom script you created by using the C\#.Net connector is now ready to be used in your automation.

**Parent Topic:**[C\#.Net](../concept/c.md)

