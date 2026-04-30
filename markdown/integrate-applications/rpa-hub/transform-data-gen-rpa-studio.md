---
title: Transform the data in RPA Desktop Design Studio
description: Transform the data in RPA Desktop Design Studio by using the Transform Data option at a component level. With this option, you can edit the output value of the Data port by using VB.NET, C\#.NET, or JavaScript.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using automations, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Transform the data in RPA Desktop Design Studio

Transform the data in RPA Desktop Design Studio by using the **Transform Data** option at a component level. With this option, you can edit the output value of the Data port by using VB.NET, C\#.NET, or JavaScript.

## Before you begin

Configure a component. For more information, see [Use a component in RPA Desktop Design Studio](configure-components.md).

Role required: none

## About this task

The **Transform Data** option can be used to modify any data that comes from the Data In port or is returned from the Data Out port.

## Procedure

1.  In the RPA Desktop Design Studio, on the Design surface, right-click either the Data In or Data Out port that you want to transform and select **Transform Data**.

2.  In the DATA TRANSFORMATION EDITOR dialog box, select the **Enabled** check box to enter the code in the Script section.

    The Data port turns green to verify the data transformation in the automation flow.

3.  From the following SCRIPT LANGUAGE list, select your preferred scripting language to write the code for the data transformation:

    -   **VB.NET**
    -   **C\#**
    -   **Javascript**
4.  In the Script section, enter the code.

    You can use the Value variable to use the incoming data for the Data In port or the outgoing data for the Data Out port in your script.

5.  After entering the script, click **OK**.

    The system validates the script.

6.  If there are any errors in the Script section, resolve the errors that are displayed in the ERRORS section and then click **OK**.


**Parent Topic:**[Using automations](../concept/rpa-studio-use.md)

