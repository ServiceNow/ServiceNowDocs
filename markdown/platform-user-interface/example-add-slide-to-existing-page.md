---
title: Example of adding a panel to an existing overview help page
description: This example adds panels to the existing overview help page that display only for users with specific roles and when a specific plugin is activated.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Overview help pages, User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Example of adding a panel to an existing overview help page

This example adds panels to the existing overview help page that display only for users with specific roles and when a specific plugin is activated.

## Before you begin

Role required: admin

## About this task

You can create a panel that displays a screenshot of auditing gauges to users with the sn\_audit.manager role, when the GRC: Audit Management plugin is activated. Create another panel visible only to users with the activity\_admin role that displays a view of the **Custom** tab in the Workflow Editor. Add the panels to the overview help page for the current version. Use the condition on a panel to specify the plugin and a slushbucket to select the roles required for access.

## Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **Overview Help**.

2.  Open the help page for the current version.

    ![Overview help page record](../image/OverviewHelpPageIstanbul.png "Overview help page record")

3.  In the **Overview Help Panels** related list, click **New**.

4.  Create a panel with these values:

    -   **Title**: **Custom Orchestration Activities**. The title is the label that appears on the panel when it is displayed to the user.
    -   **Order**: **20**. This order number is the lowest for any of the panels in this page, and means that this button appears on the left side of the page.
    -   **Roles**: **activity\_admin**. Only users with this role are able to see this panel.
    -   **Image**: This is a view of the Workflow Editor and the **Custom** tab that best introduces the feature to users.
    -   **Text**: Enter a description of the feature, emphasizing the highlights in this version. In this example, the text describes the ability to create activities and share them in the ServiceNow store.
    **Note:** Buttons for custom panels do not have icons on them.

    ![Workflow Editor panel](../image/OverviewHelpExample1.png "Workflow editor panel")

5.  Save the record.

6.  Create another panel with these values:

    -   **Title**: **Assessment Reports.** The title is the label that appears on the panel when it is displayed to the user.
    -   **Order**: **60**. This order number is the highest for any of the panels in this page, and means that this button appears on the right side of the page.
    -   **Roles**: **assessment\_admin**. Only users with this role are able to see this panel.
    -   **Image**: This is an example of a bubble chart that you want the assessment administrators to see.
    -   **Text**: Enter a description of the chart to display to the users, emphasizing the advantages of this type of chart.
    ![Assessment reports panel](../image/OverviewHelpPanelHelsinki.png "Assessment reports panel")

7.  Save the record.

8.  Log in as a user with the assessment\_admin role.

9.  Click the help icon in the form header, and then click **What's New** in the help sidebar.

    The overview help page for the current version appears, with the control button for the auditing dashboard displayed for the user in the order configured.

    ![Overview help page for the assessment administrator](../image/OverviewHelpExamplePageIstanbul.png "Overview help page for the assessment administrator")

10. Click the button to display the assessment report panel.

    The image you selected for your custom panel appears with the title and description you defined.

    ![Assessment report panel](../image/OverviewHelpExample6.png "Assessment report panel")

11. Log out and log in again as a user with the activity\_admin role.

12. Click the help icon in the form header, and then click **What's New** in the help sidebar.

    The overview help page for the current version appears, with the control button for the Workflow Editor tabs displayed for the user in the order configured.

    ![Overview help page for the Orchestration user](../image/OverviewHelpExample7.png "Overview help page for the Orchestration user")

13. Click the button to display the Orchestration activities panel.

    The image you selected for your custom panel appears with the title and description you defined.

    ![Orchestration panel](../image/OverviewHelpExample5.png "Orchestration panel")


**Parent Topic:**[Overview help pages](../concept/overview-help-pages.md)

