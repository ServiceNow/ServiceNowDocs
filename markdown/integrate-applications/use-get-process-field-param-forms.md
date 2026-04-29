---
title: Use the GetProcessFieldParameters component
description: Gets the values of the associated Table fields mapped to the process field parameter, that you had configured in an attended configuration record of a bot process. The component returns both the individual values of the parameters and all values as an object. This component reads the value of the associated Table field in the ServiceNow form record.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Forms, ServiceNow, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use the GetProcessFieldParameters component

Gets the values of the associated **Table** fields mapped to the process field parameter, that you had configured in an attended configuration record of a bot process. The component returns both the individual values of the parameters and all values as an object. This component reads the value of the associated **Table** field in the ServiceNow form record.

## Before you begin

If you are running an automation from RPA Desktop Design Studio, then assign the automation to the bot process by using the **Assign bot process** option from the **Design** tab of RPA Desktop Design Studio. In the **Bot Process** field, ensure to select an attended bot process that is enabled with Embedded Task Automation. In the **Attended Config** field, ensure to select an associated attended configuration. In the **Record Context** field, ensure to enter the Sys ID or URL of the ServiceNow form record. For more information, see [Assign bot process to an automation project](assign-bot-process.md).

Create a process field parameters as part of a bot process on the RPA Hub. See [Create a process field parameter in RPA Hub](../../rpa-hub/task/create-process-field-param-rpa.md).

Ensure you are familiar with Embedded Task Automation concepts. For more information, see [Embedded Task Automation \(ETA\) in RPA Hub](../../rpa-hub/concept/embedded-task-auto-rpa.md).

Role required:

-   sn\_rpa\_fdn.rpa\_developer or sn\_rpa\_fdn.rpa\_admin, if you are running the automation from RPA Desktop Design Studio
-   sn\_rpa\_fdn.rpa\_assisted\_user, if you are running the automation from the Attended Robot application.

## About this task

You can configure the properties for the GetProcessFieldParameters component. For more information about these properties, see [Properties of the Forms components](../reference/sn-forms-properties.md).

Let's consider an employee badge creation use case. The following steps provide guidance of how to use the GetProcessFieldParameters component in this use case. For more information about the use case, see [Embedded Task Automation \(ETA\) in RPA Hub](../../rpa-hub/concept/embedded-task-auto-rpa.md).

## Procedure

1.  In the Toolbox pane, navigate to **ServiceNow** &gt; **Forms**.

2.  Drag the GetProcessFieldParameters component to the Design surface.

3.  Click the component settings icon \(![Component settings icon.](../image/component-settings-icon.png)\).

4.  Click the add key icon \(![Add key icon.](../image/add-image-icon.png)\).

5.  Enter the name of one of the process field parameters.

    For example, Title, FirstName, LastName, Location, as shown in the following image.

    ![Enter process field parameters.](../image/get-process-field-param-config.png "Example of the Process Field Parameters Configuration")

6.  Update the process field parameter data type.

    You can define multiple parameters with primitive data type.

7.  Repeat the steps to add more parameters.

8.  Click **OK**.

9.  Connect the data and control ports of the GetProcessFieldParameters component to the corresponding ports of other components as described in the following table.

    |Port type|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |Data Out \(Parameter\)|Returns the value of an individual process field parameter and can be used in the next components.|No|
    |Data Out \(Return, Object\)|Returns the process field parameters in key value pair format that are configured in the attended configuration. This value can be used in the next components.|No|
    |Control In|Connect to the Control Out port of one or more components.|Yes|
    |Control Out|Connect to the Control In port of another component as per the required automation logic.|No|

10. To test the component, right-click the title bar of the component and select **Run From Here**.


**Parent Topic:**[Forms](../concept/forms_sn_rpa_studio.md)

