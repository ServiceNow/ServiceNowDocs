---
title: RPA Desktop Design Studio user interface
description: Learn about the RPA Desktop Design Studio user interface.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 18
breadcrumb: [Exploring RPA Desktop Design Studio, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# RPA Desktop Design Studio user interface

Learn about the RPA Desktop Design Studio user interface.

## RPA Desktop Design Studio home

With the RPA Desktop Design Studio home page, you can create and open your automation projects, review your work on these projects, and access resources that help you design automations. The default home page of the RPA Desktop Design Studio is shown in the following example.

Create automations, activities, and automation logic additions from text instructions and preview options using the Now Assist for RPA Hub. For more information, see [Now Assist for RPA Hub](rpa-now-assist-studio.md).

![Home page of RPA Desktop Design Studio.](../image/rpa-studio-home.png "Home page of RPA Desktop Design Studio")

When you launch the RPA Desktop Design Studio for the first time, you view a welcome screen to take a quick tour of the desktop studio and learn more about its features. To take a tour, select **Next** on the welcome screen. The guided tour helps you build your first automation. You can pick your preferred journey to create an automation. You can build an automation with a use case or without a use case. Select **Start** to begin the guided tour.

From the left navigation bar, which is shown in the following example, of the RPA Desktop Design Studio home page, you can do the following actions.

![Left navigation bar of the RPA Desktop Design Studio.](../image/left-nav-bar-rpa-studio.png "Left navigation bar")

<table id="table_ozv_hmx_dbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create Automation

</td><td>

Create an unattended and attended automation project. For more information, see [Create an automation project manually](../task/create-automation-project.md) and [Create an automation with Now Assist](../task/create-automation-now-assist.md).

</td></tr><tr><td>

Create Skill

</td><td>

Create a skill automation project. For more information, see [Create a skill project in RPA Desktop Design Studio](../task/create-skill-project.md).A skill automation is a reusable component. You can build a skill so that you can provide prebuilt capabilities for other automation processes. For example, if a login functionality is used in four different automations, that login functionality can be created as a skill that you can reuse across automations.

</td></tr><tr><td>

Home

</td><td>

Home page of the RPA Desktop Design Studio application.

</td></tr><tr><td>

Automation projects

</td><td>

View the list of automation projects that you recently created.You can open a local project or a cloud project. For more information, see [Open a local automation project in RPA Desktop Design Studio](../task/open-project-rpa-studio.md) and [Open a cloud automation project in RPA Desktop Design Studio](../task/open-project-remote-rpa-studio.md).

You can mark the required projects as favorites.

Select the three-dot icon next to an automation project and access the following options:

-   **Open** - Opens the automation project in the Design surface.
-   **Mark as favorite** - Marks the selected automation project as a favorite.
-   **Remove from favorite** - Removes the selected automation project from the favorites. This option appears only if the automation is marked as favorite.
-   **View details** - View the details of the automation projects such as name, description, and location of the project.
-   **Remove** - Removes the selected automation project from the automation projects list.

</td></tr><tr><td>

Sample automations

</td><td>

A sample automation is a prebuilt automation that shows how different components are configured for a specific use case. The RPA Desktop Design Studio provides multiple sample automations that cater to different use cases. For example, extracting data from a PDF and insert into an Excel file. Select the three-dot icon next to a sample automation and access the following options:

-   **Open**- Opens a selected sample automation.
-   **Open in new window**- Opens a selected sample automation in a new window.
-   **Create copy**- Creates a copy of the selected sample automation.
-   **View details**- View the details of the selected sample automation such as name, description, and location of the project.

For more information, see [Use sample automations in RPA Desktop Design Studio](../task/use-sample-automation.md) and [Sample automations](../reference/sample-automations-rpa-studio.md).

</td></tr><tr><td>

Settings

</td><td>

Specify the location for the automation projects to be downloaded in the **Location** field.Select the **Ask everytime before downloading** check box to change the location of the automation projects while downloading.

View the RPA Desktop Design Studio version and the Plugin bundle version.

</td></tr><tr><td>

Exit Desktop Studio

</td><td>

Exits the RPA Desktop Design Studio application.

</td></tr><tr><td>

Change

</td><td>

Launches connection manager window. For more details, see [Connect to an RPA Hub instance from RPA Desktop Design Studio](../task/connect-studio-instance-rpa.md).You cannot connect to a different instance after the RPA Desktop Design Studio is launched.

To connect to a different instance, you must close and reopen the RPA Desktop Design Studio application.

</td></tr></tbody>
</table>You can do the following actions from the area marked in red in the following example of the home page of RPA Desktop Design Studio.

![Selected area of the home page of RPA Desktop Design Studio.](../image/rpa-studio-home-page-selected.png "Selected area of the home page of RPA Desktop Design Studio")

-   **Automation projects**- View the list of automation projects that you recently created by selecting the **View all**. View the recent automation projects in the **Recents** tab. Mark the required projects as favorites. View the favorite automation projects in the **Favorites** tab for quick access.

    In the automation card, view the type, name, and description of the automation along with the timestamp of when it was last opened. The automations created using Now Assist for RPA Hub have an AI icon \(![AI icon.](../image/ai-sparkle-rpa-icon.png)\).

-   **Sample automations**- View the list of all sample automations by selecting **View all**.

    In the sample automation card, view the type, name, and description of the automation.

    For more information, see [Use sample automations in RPA Desktop Design Studio](../task/use-sample-automation.md).

-   **Resources**- Learn more about RPA Desktop Design Studio documentation, release notes, and ServiceNow University courses. Select a card to navigate to the respective web page.
-   **What's New**- View the new features RPA Desktop Design Studio. For example, you can build your first automation by starting a guided tour. Select **Take tour** to begin the guided tour.

## Design surface

The area marked in red in the following example is the Design surface. You create automations by dragging the components from the Toolbox pane to the Design surface.

You can also create automations by dragging the activities and variables from the Project Explorer pane or by dragging methods and events from the Object Explorer pane.

Create automations, activities, and automation logic additions from text instructions and preview options using the Now Assist for RPA Hub. For more information, see [Using Now Assist for RPA Hub](use-now-assist-rpa-hub.md).

![Design surface.](../image/design-surface.png "Design surface")

The Start and End components are the default components in every activity. They’re the starting and ending point of an activity. You can't delete these components.

Enhance the automation logic with text instructions, either on the design surface or by selecting a component or by using the Now Assist for RPA Hub application. For more information, see [Build an automation with Now Assist](../task/build-automation-now-assist.md).

When you close this application, you’re logged out of the RPA Desktop Design Studio and the ServiceNow instance.

Here's a list of actions that you can do on the Design surface:

-   **Select multiple components**

    To select multiple components, you can select one or more components by pressing and holding the **Ctrl** key and then selecting the title bar of the component.

    Alternatively, you can select the mouse device and drag it across the set of components that you want to select.

-   **Copy, paste, and cut components or methods**

    You can copy or cut, and paste components or methods by using the keyboard shortcuts or the context menu.

    To use the keyboard shortcuts, do the following actions.

    -   Select the components that you want to copy and press the Ctrl +C keys followed by the Ctrl + V keys.
    -   Select the components that you want to cut and press the Ctrl +X keys followed by the Ctrl + V keys.
    To use the context menu, do the following actions.

    1.  Select the components that you want to copy or cut.
    2.  Right-click on the component bar of any of the components.
    3.  Select **Cut** or **Copy**.![Copy-cut-context-menu.](../image/copy-cut-paste.png)
    To paste the components at the same position on the Design surface from where they’re copied, use the Ctrl + V shortcut.

    You can also copy and paste components between different activities and instances of the RPA Desktop Design Studio.

    Alternatively, after copying the components, you can right-click and select **Paste** to paste the components at the position that you choose.

-   **Delete components**

    To delete components, select the components that you want to delete, right-click any of the selected components, and select **Delete**.

    Alternatively, after selecting the components, press the **Delete** key to delete the components. In the Confirmation dialog box, click **Yes**.

-   **Use the zoom settings**

    On the Design surface, you can zoom in and zoom out to increase or decrease your view of a specific activity.

    The zoom settings are in the bottom-right corner of the Design surface as shown in the following example.

    ![Zoom settings in RPA Desktop Design Studio.](../image/zoom-settings.png "Zoom settings")

    To zoom out, drag the bar to the left. To zoom in, drag the bar to the right.

    Alternatively, you can also use the scroll up and down key with your mouse wheel or track pad while holding the **Ctrl** key to adjust the zoom settings.

-   **Scroll shortcut**

    To scroll horizontally on the Design surface, press the **Shift** key and scroll using the mouse.


## Quick Access Toolbar

The Quick Access Toolbar, which is shown in the following example, enables you to create, open, save, undo, and redo your automation projects. You can also minimize the ribbon or change the position of the ribbon by using the options that are provided in the toolbar.

![Quick access toolbar.](../image/quick-access-toolbar.png "Quick access toolbar")

## Design tab

The **Design** tab provides you with options that enable you to execute an automation, configure the settings of the RPA Desktop Design Studio, help you with diagnostics, publish options, connect to a ServiceNow instance, and access some other resources such as launching recorder. The following example shows you the options that are displayed with the **Design** tab.

![Options displayed on the Design tab.](../image/design-tab-rpa-studio.png "Options displayed on the Design tab")

You can access the following sections by using the **Design** tab in RPA Desktop Design Studio:

<table id="table_m1f_mwy_vrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Execution section

</td></tr><tr><td>

**Run**

</td><td>

Use the **Run** button to start the workflow execution of an automation project.

</td></tr><tr><td>

**Move next**

</td><td>

Use the **Move next** button to move to the next component where a breakpoint is hit. This option is enabled only when the execution flow hits a breakpoint.

</td></tr><tr><td>

**Stop**

</td><td>

Use the **Stop** button to stop the workflow execution of an automation project.

</td></tr><tr><td>

**Clear log**

</td><td>

Use the **Clear log** button to clear the runtime log.

</td></tr><tr><td>

**Clear breakpoints**

</td><td>

Use the **Clear breakpoints** button to remove all the breakpoints from the automation. This option is enabled when at least one breakpoint is set. Click the down arrow button next to the **Clear Breakpoints** button and select **Find all** to locate the specific breakpoints in the Find All References section.

</td></tr><tr><td>

**Assign bot process**

</td><td>

Assign the automation package to a bot process and utilize the resources of the automation. For more information on how to assign a bot process, see [Assign bot process to an automation project](../task/assign-bot-process.md).

</td></tr><tr><td class="sub-head" colspan="2">

Settings section

</td></tr><tr><td>

**Minimize studio**

</td><td>

Select the **Minimize studio** check box to minimize the RPA Desktop Design Studio during an automation execution. You can minimize the RPA Desktop Design Studio when you select the **Run** button to run the automation.

</td></tr><tr><td>

**Auto save**

</td><td>

Select the **Auto save** check box to save your automation project file automatically as you work.

</td></tr><tr><td>

**Save layout**

</td><td>

Select the **Save layout** check box to save the pane layout of the RPA Desktop Design Studio.

</td></tr><tr><td class="sub-head" colspan="2">

Diagnostics section

</td></tr><tr><td>

**Attach**

</td><td>

You can review the execution logs of a process that is already executed. To review, use the **Attach** button to attach either a local execution log file or a remote execution log file that is saved in the ServiceNow instance.To find a remote execution log, specify your criteria or use the pagination to navigate to the required page on the **Open Log** window.

![Open Log window to fetch remote logs.](../image/remote-log-window.png)

After specifying the criteria, do the steps.

1.  Select **Fetch Logs** to fetch and display the remote execution logs.
2.  To play the log, select the required log and then select **Play log**.

The following process job records are not displayed in the Attach log window:

-   Process job records with no logs.
-   Process job records that are stored in the robot machine.

</td></tr><tr><td>

**Replay**

</td><td>

Use the **Replay** button to replay the attached log execution.

</td></tr><tr><td>

**Pause**

</td><td>

Use the **Pause** button to pause the attached log execution.

</td></tr><tr><td>

**Stop**

</td><td>

Use the **Stop** button to stop the attached log execution.

</td></tr><tr><td>

**Pause on error**

</td><td>

Use the **Pause on error** button to pause the attached log execution if an error occurs during the execution.

</td></tr><tr><td>

**Log speed**

</td><td>

Adjust the **Log speed** slider to control the speed when you replay the automation using logs. By default, the slider is adjusted to the center where it takes one second to execute each component.

 If you decrease the log speed, each component takes the same amount of time it took during the execution.

 If you increase the log speed, all the components get executed instantly on replay.

</td></tr><tr><td class="sub-head" colspan="2">

RPA Hub

</td></tr><tr><td>

**Publish**

</td><td>

Use the **Publish** button to publish the automation project to RPA Hub.

</td></tr><tr><td>

**Connect to instance**

</td><td>

Use the **Connect to instance** button either to connect to an existing ServiceNow instance or to add ServiceNow instance details.

</td></tr><tr><td class="sub-head" colspan="2">

Resources section

</td></tr><tr><td>

**Skills**

</td><td>

Use the **Skills** button to view the skill automation projects in the Skill Explorer pane. You can reuse these skill automation projects by dragging the skill automation project from the Skill Explorer pane to the Design surface. It’s displayed as a Remote Activity.

</td></tr><tr><td>

**Samples**

</td><td>

Select the **Samples** button to refer to the sample automations in the Samples Explorer pane. A sample automation demonstrates how the RPA Desktop Design Studio executes an automation project.The sample automations are classified into **Beginner**, **Intermediate**, **Advanced**, **References**, and **Attended** categories based on the complexity and use cases of the automations.

For more information, see [Use sample automations in RPA Desktop Design Studio](../task/use-sample-automation.md).

</td></tr><tr><td>

**Project folder**

</td><td>

Use the **Project folder** button to open the current automation project folder.

</td></tr><tr><td>

**Remove Unused resources**

</td><td>

Use the **Remove unused resources** button to remove unused variables, references, and user plugins.

</td></tr><tr><td class="sub-head" colspan="2">

Other Options section

</td></tr><tr><td>

**Insert between**

</td><td>

Use the **Insert between** button to connect to the nearest component with a free Control port to the left of the newly dropped component.

</td></tr><tr><td>

**Auto join**

</td><td>

Use the **Auto join** button to remap the connections between the two components when a component is deleted.

</td></tr><tr><td>

**Silent mode**

</td><td>

Use the **Silent mode** button to execute the automation project without opening further activity tabs.

</td></tr><tr><td>

**Launch recorder**

</td><td>

Capture your actions from your desktop or web applications and convert them into an automation flow by using the recorder option. For more information on recording automations, see [Recording automations](recording-automations.md).

</td></tr><tr><td>

**Code quality check**

</td><td>

Inspect an activity or completion automation project for any automation issues that prevents the automation from progressing by using the Code quality check feature. For more information on how to perform Code quality check in RPA Desktop Design Studio, see [Code quality check in RPA Desktop Design Studio](code-quality-check-studio.md).

</td></tr></tbody>
</table>## View tab

The **View** tab, which is shown in the following example, enables you to view the Tool Windows when they’re closed, install extra plugins by using the plugin manager option, view the console log and execution log, find components, and find all references.

![Options displayed on the View tab.](../image/view-tab-rpa-studio.png "Options displayed on the View tab")

You can access the following sections when you use the **View** tab in RPA Desktop Design Studio:

<table id="table_hpg_qzy_vrb"><thead><tr><th>

Section or field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Tool Windows** section

</td><td>

Click each pane of the tool window \(Toolbox, Project explorer, Properties, and Object explorer\) to reopen these panes when they’re closed.

</td></tr><tr><td>

**Plugin manager**

</td><td>

Use the **Plugin manager** button to install extra plugins to design automations that are required for creating automation projects. For more information, see [Manage plugins in RPA Desktop Design Studio](../task/install-plugins-rpa-studio.md).

</td></tr><tr><td class="sub-head" colspan="2">

Others section

</td></tr><tr><td>

**Console log**

</td><td>

Use the **Console** button to open the console section, if closed. This section has the information that is related to the Console Log component.

</td></tr><tr><td>

**Execution log**

</td><td>

Use the **Execution log** button to open the Execution Log section, if closed. You can view the error logs of the automation execution in this section, when you attach the logs.

</td></tr><tr><td>

**Find**

</td><td>

Use the **Find** button to find components within the automation project.

</td></tr><tr><td>

**References**

</td><td>

Use the **References** button to show the navigation pane, if it’s closed.

</td></tr><tr><td>

**Code quality check results**

</td><td>

Displays the details of the code quality check execution.

</td></tr></tbody>
</table>## Project Explorer pane

The area marked in red in the following example is the Project Explorer pane. You can see all the artifacts that are used in the current automation project in this pane. Artifacts include activities, plugins, user plugins, global objects, and forms \(if you’re creating an attended automation project\).

![Project explorer pane.](../image/project-explorer-pane.png "Project Explorer pane")

## Toolbox pane

The area marked in red in the following example is the Toolbox pane. You can use this pane to see all the available components and connectors in the RPA Desktop Design Studio.

![Toolbox pane.](../image/toolbox-pane.png "Toolbox pane")

Components are listed under multiple categories. You can expand each component group to reveal individual components that can be used on the Design surface.

Search for the components that are available within the Toolbox by entering the text in the **Filter by Name** field.

## Properties pane

The area marked in red in the following example is the Properties pane. Each component, connector, activity, or global object has multiple properties that appear in the Properties pane.

![Properties pane](../image/properties-pane.png "Properties pane")

Properties help you fine-tune the functionality of the objects.

## Object Explorer pane

The area marked in red in the following example is the Object Explorer pane. The methods and events that are associated with the objects in the Project Explorer pane appear in this pane.

![Object Explorer pane.](../image/object-explorer-pane.png "Object Explorer pane")

Double-click the specific object in the Project Explorer pane to view its associated methods and events.

For example, you can click a List connector that you added in the Global Objects node to view the associated methods in the Object Explorer pane.

Global Objects is a section in the Project Explorer pane that is a placeholder for objects that are accessible across all activities like connectors and global variables. You can further organize the objects by creating folders within global objects.

## RPA Desktop Design Studio keyboard shortcuts

You can use keyboard shortcuts to perform the following actions quickly in the RPA Desktop Design Studio.

<table id="table_ybz_kt4_5sb"><thead><tr><th>

Action

</th><th>

Windows keyboard shortcut

</th></tr></thead><tbody><tr><td>

Create a project

</td><td>

Ctrl+N

</td></tr><tr><td>

Open a project

</td><td>

Ctrl+O

</td></tr><tr><td>

Save a project

</td><td>

Ctrl+S

</td></tr><tr><td>

Build an automation

</td><td>

Ctrl+EnterThis option is available only when the Now Assist for RPA Hub is enabled.

For more information, see [Build an automation with Now Assist](../task/build-automation-now-assist.md).

</td></tr><tr><td>

Undo

</td><td>

Ctrl+Z

</td></tr><tr><td>

Redo

</td><td>

Ctrl+Y

</td></tr><tr><td>

Run

</td><td>

F5

</td></tr><tr><td>

Global Run

</td><td>

Ctrl+F5

</td></tr><tr><td>

Global Stop

</td><td>

Ctrl+Shift+F5

</td></tr><tr><td>

Clear logs

</td><td>

Ctrl+F8

</td></tr><tr><td>

Step over

</td><td>

Ctrl+F10

</td></tr><tr><td>

Copy

</td><td>

Ctrl+C

</td></tr><tr><td>

Cut

</td><td>

Ctrl+X

</td></tr><tr><td>

Paste

</td><td>

Ctrl+V

</td></tr><tr><td>

Select All

</td><td>

Ctrl+A

</td></tr><tr><td>

Project Explorer

</td><td>

Ctrl+R

</td></tr><tr><td>

Object Explorer

</td><td>

Ctrl+Alt+J

</td></tr><tr><td>

Toolbox

</td><td>

Ctrl+Alt+X

</td></tr><tr><td>

Properties

</td><td>

F4

</td></tr><tr><td>

Find window

</td><td>

Ctrl+F

</td></tr><tr><td>

Delete

</td><td>

Del

</td></tr></tbody>
</table>