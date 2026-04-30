---
title: Record an automation
description: Record an automation by using the recorder option in the RPA Desktop Design Studio application. The actions that you perform on the application elements can be saved as an automation flow to the automation project.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Recording automations, Using automations, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Record an automation

Record an automation by using the recorder option in the RPA Desktop Design Studio application. The actions that you perform on the application elements can be saved as an automation flow to the automation project.

## Before you begin

You must do the following actions before you start recording an automation with the recorder for the first time:

-   Install and enable the ServiceNow RPA Chrome extension to your Google Chrome browser. For more information on adding the RPA Google Chrome extension, see [Add the ServiceNow RPA Chrome extension](../../rpa-hub/task/add-google-chrome-extension-rpa.md).
-   Install and enable the ServiceNow RPA Edge extension to your Microsoft Edge browser. For more information on adding the RPA Edge extension, see [Add the ServiceNow RPA Edge extension](add-servicenow-edge-extension.md).
-   Ensure that the option **Allow this extension to read and change all your data on websites that you visit** to **On all sites** is enabled in the Site access pane of the ServiceNow RPA Google Chrome and Microsoft Edge browser extensions.
-   Enable Java Access Bridge from your Windows machine. For more information on how to enable Java Access Bridge, see [Enabling and Testing Java Access Bridge](https://docs.oracle.com/javase/7/docs/technotes/guides/access/enable_and_test.html).

Ensure to configure the following settings and tasks before you record a web application:

-   Set the zoom level of the browser to 100%.
-   Close the developer tools of the browser.
-   Wait for the web page to load completely to the browser.

Role required: None

## Procedure

1.  Select **Launch recorder** from the toolbar of the **Design** tab.

    The RPA Desktop Design Studio window is minimized and the recorder panel is launched.

    **Important:** If the Universal App Connector \(UAC\) plugin is unavailable or removed from the automation project, the **Launch recorder** button is greyed out in RPA Desktop Design Studio.

2.  Open the application that you want to record and select the **Start recording** icon \(![Start recording icon](../image/start-recording-icon.png)\).

3.  Point to the element where you want to perform an action.

    The default action that is related to the type of element is displayed.

    For example, if you point to the **Save** button in Notepad++, the element type is displayed as &lt;button&gt; and the default action for this item is **Click**.

    ![Element type displayed as button and default action is Click for Save button.](../image/click-save-button-recorder-rpa.png "Element type and default action for Save button")

4.  Select the drop-down button against the default action to view the list of related actions for the element.

    For example, the list of related actions for the button element type are SendKeys, GetText, DoubleClick, and Focus.

    For more information on the different types of actions and elements, see [Types of elements and actions for the recorder](../reference/element-actions-recorder.md).

5.  Select the required action to be performed on the element.

    Each action that you perform is captured sequentially in the Recorded actions pane.

6.  Do any of the following options for a desired action.

<table id="choicetable_vmv_2f1_5rb"><thead><tr><th align="left" id="d187149e261">

Option

</th><th align="left" id="d187149e264">

Action

</th></tr></thead><tbody><tr><td id="d187149e270">

**Highlight the parent of an element**

</td><td>

Select the Highlight parent element icon \(![Highlight parent icon.](../image/hightlight-parent.png)\). For example, if you select the **Highlight parent element** option for a button, the toolbar is highlighted.

![When the parent table is highlighted, the Highlight parent element option for a button in a toolbar.](../image/highligh-parent-element.gif "Highlight parent element option")

</td></tr><tr><td id="d187149e304">

**Pause the recording**

</td><td>

Select the Pause recording icon \(![Pause recording icon.](../image/pause-recording.png)\).

</td></tr><tr><td id="d187149e319">

**View the Recorded actions pane**

</td><td>

Select the Show recorded steps icon \(![Show recorded steps icon.](../image/show-recorded-steps.png)\).You can verify the actions that you performed on the application elements from here.

</td></tr><tr><td id="d187149e336">

**Know more about the recorder feature**

</td><td>

Select the Help icon \(![Help icon.](../image/help-recorder-rpa-icon.png)\) that navigates to the product documentation web page.

</td></tr><tr><td id="d187149e352">

**Delete a recorded action**

</td><td>

Point to the action and select the Delete action icon \(![Delete action icon.](../image/delete-action-icon.png)\).

</td></tr><tr><td id="d187149e367">

**Delete all the recorded actions from the Recorded actions pane**

</td><td>

Select **Delete all**.

</td></tr><tr><td id="d187149e379">

**Edit the recorded action or element details**

</td><td>

1.  Select the Edit action icon \(![Edit action icon.](../image/edit-action-rec-rpa-icon.png)\) in the Recorded actions panel.
2.  Update the action type or element name.
3.  Select **Update**.


</td></tr></tbody>
</table>7.  Select **Review recording**.

8.  On the Review app path and URL pane, review the list of applications and their application paths.

9.  Select **Continue**.

10. On the Save recording pane, fill in the fields.

<table id="table_nf2_51q_gwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Activity name

</td><td>

Name of the automation activity to which the recorded actions are saved as an automation flow.**Note:** Ensure that you don’t give the name of an existing activity.

</td></tr><tr><td>

Save global object to

</td><td>

Option to save the recorded elements to an existing UAC object or a new UAC global object. If you select **New global object**, you must enter the name for the object in the **Global object name** field.

 If you select the **Existing global** object, you must select an existing UAC global object from the Select from existing global objects list.

</td></tr></tbody>
</table>11. Select **Save recording**.

    The recorded actions are saved as an automation activity to the automation project. You can modify the recorded automation activity from the design surface.


## What to do next

You can view the recorded elements as a UAC object in **Global Objects** in Project Explorer. Expand the UAC objects and view all the screens and elements that are captured by the recorder. Do the following actions if you want to change the screens and element match rules in UAC:

1.  Right-click the generated UAC object in **Global Objects** and select **Configure**.

    The Configure screens and elements window is displayed.

2.  Configure the screens and the elements of the recording from the Screens and elements pane.

    For more information on how to configure the screen and element match rules, see [Use the Universal App Connector](configure-uac.md).


**Parent Topic:**[Recording automations](../concept/recording-automations.md)

