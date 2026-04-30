---
title: Use the AttendedConfigurations component
description: When you use the AttendedConfigurations component, it shows a list of attended configurations associated to the selected same bot process. To select and give control out port for each configuration that routes the automation logic.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Forms, ServiceNow, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Use the AttendedConfigurations component

When you use the AttendedConfigurations component, it shows a list of attended configurations associated to the selected same bot process. To select and give control out port for each configuration that routes the automation logic.

## Before you begin

If you are running an automation from RPA Desktop Design Studio, then assign the automation to the bot process by using the **Assign bot process** option from the **Design** tab of RPA Desktop Design Studio. In the **Bot Process** field, ensure to select an attended bot process that is enabled with Embedded Task Automation. In the **Attended Config** field, ensure to select an associated attended configuration. In the **Record Context** field, ensure to enter the Sys ID or URL of the ServiceNow form record. For more information, see [Assign bot process to an automation project](assign-bot-process.md).

Ensure you are familiar with Embedded Task Automation concepts. For more information, see [Embedded Task Automation in RPA Hub](../../rpa-hub/concept/embedded-task-auto-rpa.md).

Role required:

-   sn\_rpa\_fdn.rpa\_developer or sn\_rpa\_fdn.rpa\_admin, if you are running the automation from RPA Desktop Design Studio
-   sn\_rpa\_fdn.rpa\_assisted\_user, if you are running the automation from the Attended Robot application.

## About this task

The AttendedConfigurations component segregates the execution of the automations in a single automation project and calls the respective logic according to the action invoked.

If you are triggering the automation from the ServiceNow form's UI action \(button\) and it executes using the Attended Robot application, then the AttendedConfigurations component routes the automation flow from the associated attended configuration.

You can configure the properties for the AttendedConfigurations component. For more information about these properties, see [Properties of the Forms components](../reference/sn-forms-properties.md).

For example, if an automation requires two UI actions, create two attended configurations in RPA Hub, that are associated to the same bot process and table. Define the automation logics separately for these UI actions, under different activities.

Let's consider a currency price retrieval use case, where one automation is built with two automation logics for UI actions such as Get Prices and Update Price. These UI actions are associated to two attended configurations, Get Prices and Update Price. The attended configurations are associated to the same bot process and table. The following steps provide guidance of how to use the AttendedConfigurations component in this use case.

## Procedure

1.  In the Toolbox pane, navigate to **ServiceNow** &gt; **Forms**.

2.  Drag the AttendedConfigurations component to the Design surface.

3.  Click the component settings icon \(![Component settings icon.](../image/component-settings-icon.png)\).

4.  Select one or more applicable attended configurations.

    In this example, select both the attended configurations \(Get Prices and Update Price\).

    ![Select attended configurations.](../image/attended-config-forms-studio.png "Example: Select attended configurations")

5.  Click **OK**.

    You will view more than one control out port.

6.  Connect the data and control ports of the AttendedConfigurations component to the corresponding ports of other components as described in the following table.

    In this example, map the Get Prices Control Out port to the corresponding activity. Similarly, map the Update Price Control Out port to the corresponding activity. After you select the Get Prices UI action, the corresponding logic is executed. Similarly, after you select the Update Price UI action, the corresponding logic is executed.

    |Port type|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |Control In|Connect to the Control Out port of one or more components.|Yes|
    |Control Out|\[Multiple\] For each selected attended configuration, a control out is created. Connect to the Control In port of another component or activity as per the required automation logic.|No|

7.  To test the component, right-click the title bar of the component and select **Run From Here**.


**Parent Topic:**[Forms](../concept/forms_sn_rpa_studio.md)

