---
title: Use the LockUIDialog component
description: Provide additional authentication to any step of your attended automation by using the LockUIDialog component in the RPA Desktop Design Studio application.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Dialogs, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the LockUIDialog component

Provide additional authentication to any step of your attended automation by using the LockUIDialog component in the RPA Desktop Design Studio application.

## Before you begin

Ensure that you are in an attended automation project to use the LockUIDialog component.

Role required: RPA developer

## About this task

Consider the scenario where you want to provide additional security to a step in your attended automation. For example, the automation is trying to access the employee database. This database has sensitive information. When you use the LockUIDialog component, the automation proceeds to the next step only if the user is authenticated by using the machine user name and password. You can also provide a message to be displayed during the authentication.

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Dialogs** in an attended automation project.

2.  Drag the LockUIDialog component to the Design surface.

3.  Connect the data and control ports of the LockUIDialog component to the corresponding ports of the other components as described in the following table:

<table id="table_ucm_psl_fwb"><thead><tr><th>

Port name

</th><th>

Port type

</th><th>

Port description

</th><th>

Required?

</th></tr></thead><tbody><tr><td>

DisplayText

</td><td>

Data In

</td><td>

Text that you want to display during the authentication. The text can be used to convey why an authentication is required for the automation step. For example, you can use the following text if the automation step is trying to access the employee database:`Enter the user name and password to access the employee database.`

 The text is displayed in the authentication dialog box that is used to enter the machine user name and password.

</td><td>

No

</td></tr><tr><td>

Result

</td><td>

Data Out

</td><td>

True or false value of the authentication. If the authentication is successful, the result is true. If the authentication is unsuccessful, the result is false.The true or false value of the result can be further used to connect to any condition. For more information on how to use the condition components, see [Conditions](../concept/conditions-components.md).

</td><td>

No

</td></tr><tr><td>

Not applicable

</td><td>

Control In

</td><td>

Passes the control from the previously executed component.

</td><td>

No

</td></tr><tr><td>

Not applicable

</td><td>

Control Out

</td><td>

Passes the control from the LockUIDialog component to the next component to be executed.

</td><td>

No

</td></tr></tbody>
</table>4.  To test the component, right-click the component and select **Run From Here**.

    You can also run the automation by selecting **Run** from the **Design** tab.


**Parent Topic:**[Dialogs](../concept/dialogs.md)

