---
title: Recording automations
description: Capture your actions from your desktop or web applications and convert them into an automation flow by using the recorder option in the RPA Desktop Design Studio application. You can record attended and unattended automations by using this capability. When you record an automation, you don't have to create it manually by using connectors or components.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 4
breadcrumb: [Use, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Recording automations

Capture your actions from your desktop or web applications and convert them into an automation flow by using the recorder option in the RPA Desktop Design Studio application. You can record attended and unattended automations by using this capability. When you record an automation, you don't have to create it manually by using connectors or components.

**Important:** The recorder feature supports the applications which can be interrogated using the Universal App Connector.

## Highlighting an element

When you use the recorder, you can highlight the different elements in an application. These highlights enable you to differentiate the different type of elements. You can then perform the required action for each element. Each element has a default action and a list of sub-actions.

![Highlighting an element when using the recorder.](../image/action-recorder-highlight.png "Highlighting an element by using the recorder")

## Recorded actions pane

The action that you perform on each element is captured in the Recorded actions pane. The recorded action in the Recorded actions pane displays the type of action and the element on which the action is performed. The recorded actions are also listed according to the application screens.

## Automation flow generation

When a recording is saved, the RPA Desktop Design Studio application generates an automation flow as an activity to the automation project. The recording is also automatically configured as an object and listed under the **Global Objects** option in the Project Explorer pane. You can improve the generated automation flow from the Design surface by adding further components.

## Configuring the screen match rules

The screens and elements of the recording are also configured as objects to **Global Objects**. You can configure the screen match rules and the element attributes based on your preference, by using the Universal App Connector. For more information on how to use the Universal App Connector, see [Universal app connector](universal-app-connector.md).

## Enhanced element interrogations

## Populate element name

When you record an action in the application, the element name is automatically filled in the Recorded actions pane. The element name is captured from the target application. In the following example, while recording the SendKeys action, the element name "Location" is automatically filled, followed by "with text" and the keys or text value that is inputted by the user during the recording phase. If no default element name is available in the target application, the type of element is used as the name.

![SendKeys action on element name "Location".](../../../release-notes/image/recording-screen-element.png "SendKeys Action type")

## Rearrange recorded actions

You can move and position your recorded actions and screens in the Recorded actions pane. You can also rearrange recorded elements in the Recorded actions pane. The recorded screen segment is split when a recorded action from a screen segment is dropped on to a different screen segment.

![Rearranged elements in the Recorded actions pane.](../../../release-notes/image/recorder-screen-split.png "Rearranged elements in the Recorded actions pane")

For example, when you record two actions of the QUOTES SYSTEM application, \(DoubleClick and Click\) and two actions of the Badge Tool application \(Focus and GetText\). Then, the list of actions are displayed in the Recorded actions pane, in the order in which they are recorded.

![Actions in the Recorded actions pane before rearranging.](../image/applications-actions-before-rearranging-rpa.png "Actions in the Recorded actions pane before rearranging")

When you move the Focus action from the Badge Tool application to the top of the list and above the QUOTES SYSTEM application. Then, the list of actions are displayed as follows in the Recorded actions pane, after the hierarchy is rearranged. The recordings of the QUOTES SYSTEM application are split.

![Actions in the Recorded actions pane after rearranging.](../image/applications-actions-after-rearranging-rpa.png "Actions in the Recorded actions pane after rearranging")

When you save the recording, the automation is generated accordingly. The automation flow is generated based on the new sequence of actions in the Recorded actions pane.

## Editing a recorded action

Instead of deleting and re-recording an action, you can update the action type or element details by editing the recorded action, using the Edit action icon, in the Recorded actions pane. For example, you can edit the "GetText" action type on "About" element name in the following image.

![Edit action on the Recorded actions panel.](../../../release-notes/image/recorder-action-edit.png "Edit a recorded action")

After selecting the edit action, you can change the action type to "SetText" or element name to "Tools" from "About" and select **Update**, as shown in the following example.

![Select the Update button after editing the recorded action.](../../../release-notes/image/recorder-edit-second-step.png "Update the recorded action after editing")

## Launch application

On the design surface, the component to launch an application is now added automatically to the automation flow that is generated by the recorder.

## Benefits of creating automations with the recorder

Using a recorder to create an automation provides the following benefits:

-   Low-code users can create automations more easily. Manually creating an automation with a connector or component is complicated.
-   There's less time and effort needed to create an automation with the recorder.

## Limitations

For information on the known issues and limitations for recording automations, see [Known issues and limitations of RPA Desktop Design Studio for recording automations \[KB1225708\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1225708).

-   **[Record an automation](../task/create-recorded-automation.md)**  
Record an automation by using the recorder option in the RPA Desktop Design Studio application. The actions that you perform on the application elements can be saved as an automation flow to the automation project.
-   **[Types of elements and actions for the recorder](../reference/element-actions-recorder.md)**  
The actions are the activities that you can perform on an application element such as a text box, button, hyperlinks, and so on. By using these actions, you can build an automation flow in the RPA Desktop Design Studio recorder.

**Parent Topic:**[Using automations](rpa-studio-use.md)

