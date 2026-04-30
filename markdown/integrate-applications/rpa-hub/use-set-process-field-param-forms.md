---
title: Use the SetProcessFieldParameters component
description: Sets the values of the associated Table fields mapped to the process field parameter, that you had configured in an attended configuration record of a bot process. This component updates the values of the configured field parameters associated to the Table field in the ServiceNow form record.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Forms, ServiceNow, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the SetProcessFieldParameters component

Sets the values of the associated **Table** fields mapped to the process field parameter, that you had configured in an attended configuration record of a bot process. This component updates the values of the configured field parameters associated to the **Table** field in the ServiceNow form record.

## Before you begin

If you are running an automation from RPA Desktop Design Studio, then assign the automation to the bot process by using the **Assign bot process** option from the **Design** tab of RPA Desktop Design Studio. In the **Bot Process** field, ensure to select an attended bot process that is enabled with Embedded Task Automation. In the **Attended Config** field, ensure to select an associated attended configuration. In the **Record Context** field, ensure to enter the Sys ID or URL of the ServiceNow form record. For more information, see [Assign bot process to an automation project](assign-bot-process.md).

Create process field parameters as part of a bot process on the RPA Hub. See [Create a process field parameter in RPA Hub](../../rpa-hub/task/create-process-field-param-rpa.md).

Ensure you are familiar with Embedded Task Automation concepts. For more information, see [Embedded Task Automation in RPA Hub](../../rpa-hub/concept/embedded-task-auto-rpa.md).

Role required:

-   sn\_rpa\_fdn.rpa\_developer or sn\_rpa\_fdn.rpa\_admin, if you are running the automation from RPA Desktop Design Studio
-   sn\_rpa\_fdn.rpa\_assisted\_user, if you are running the automation from the Attended Robot application.

## About this task

You can configure the properties for the SetProcessFieldParameters component. For more information about these properties, see [Properties of the Forms components](../reference/sn-forms-properties.md).

Let's consider an employee badge creation use case. The following steps provide guidance of how to use the SetProcessFieldParameters component in this use case. For more information about the use case, see [Embedded Task Automation in RPA Hub](../../rpa-hub/concept/embedded-task-auto-rpa.md).

## Procedure

1.  In the Toolbox pane, navigate to **ServiceNow** &gt; **Forms**.

2.  Drag the SetProcessFieldParameters component to the Design surface.

3.  Click the component settings icon \(![Component settings icon.](../image/component-settings-icon.png)\).

4.  Click the add key icon \(![Add key icon.](../image/add-image-icon.png)\).

5.  Enter the name of one of the process field parameters.

    For example, BadgeID, RequestState.

    ![Enter process field parameters.](../image/set-process-field-param-config-studio.png "Example of the Process Field Parameters Configuration")

    A Data In port is created.

6.  Update the process field parameter data type.

    You can define multiple parameters with primitive data type.

7.  Repeat the steps to add more parameters.

8.  Click **OK**.

9.  Connect the data and control ports of the SetProcessFieldParameters component to the corresponding ports of other components as described in the following table.

    |Port type|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |Data In|Pass the data of the field parameter.|Yes|
    |Is Success \[Data Out\]|Boolean response to whether the update operation on the end form is successful or not.|Not Applicable|
    |Control In|Connect to the Control Out port of one or more components.|Yes|
    |Control Out|Connect to the Control In port of another component as per the required flow.|Not Applicable|

10. To test the component, right-click the title bar of the component and select **Run From Here**.


**Parent Topic:**[Forms](../concept/forms_sn_rpa_studio.md)

