---
title: Add activities to an app's playbook in Creator Studio
description: Add activities to an app's playbook to specify what the automation does to the designated record type. An activity defines what actually happens when a playbook executes.
locale: en-US
release: xanadu
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Working with automation in Creator Studio, Building apps with Creator Studio, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Add activities to an app's playbook in Creator Studio

Add activities to an app's playbook to specify what the automation does to the designated record type. An activity defines what actually happens when a playbook executes.

## Before you begin

To add [activities](../concept/creator-studio-glossary.md#) to a playbook, you must be given permission to work on the app.

## About this task

The activities that you can add to a playbook are limited by your administrator to ensure you use the correct ones for your organization. Your admin may have created some custom activities for you to choose from, or hidden some standard activities.

## Procedure

1.  Go to **All** &gt; **App Engine** &gt; **Creator Studio** to see all the apps on the Creator Studio home page.

2.  Open the app that contains the playbook you want to add an activity to.

3.  Select to **Preview** how different forms appear in various experiences, or select the **View** or **Edit** button to view or edit the application experience.

    Select different previewing options if you want to make sure that you've selected the correct application and see how it will appear in the following formats:

    -   **Portal** \(see a preview of how it'll appear on a desktop website\)
    -   **Now Mobile** \(see a preview of how it'll appear on a mobile phone or device\)
    -   **Virtual agent** \(see a representation of how it'll appear on a chatbot interface\)

        **Note:** Your organization should have the correct plugins installed to see how the form will appear in Virtual Agent. If you're interested, ask your admin and see [Catalog builder preview topic conversation](https://www.servicenow.com/docs/access?context=catalog-builder-preview-topic&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) for more information on previewing forms and their catalog items in Virtual Agent.

    The **View** button displays forms that have been published and doesn't explicitly create a new draft form for development. The **Edit** button takes you to a development form, for example, a new draft version of a form that's already been published.

    ![Preview how your app will look](../image/crs-portal-preview.png "Preview the app's experience")

    You can also check out a representation of how the form submissions workspace will appear by selecting the **Submissions** preview, as well as the records your app generates for it \(by selecting the **Record** preview\).

4.  Select the **Automations** tab in the application header.

5.  Check that you're editing the correct playbook in your app by selecting it from the **Automations** tab.

    ![Automations tab in Creator Studio](../image/cs-automations-tab.png)

6.  Select the add icon ![](../image/cs-add-icon.png) on the connector where you want to add an activity and choose the square **Add an activity** icon \(![](../image/cs-add-activity-icon.png)\) in the menu that pops up.

<table id="table_isj_z54_ccc"><thead><tr><th>

View

</th><th>

Steps

</th></tr></thead><tbody><tr><td>

Diagram

</td><td>

1.  Select the **+** icon in the stage.
2.  In the mini-picker, select the square icon \(![](../image/cs-add-activity-icon.png)\) to add an activity.


</td></tr><tr><td>

Board

</td><td>

Select **+ Add activity**.

</td></tr></tbody>
</table>7.  Choose the type of activity that you want from the Activity library pop-up.

    **Note:** In addition to the following standard activities, you may see some custom activities that your admin created.

<table id="table_gj1_3cg_n1c"><thead><tr><th>

Activity type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Request approval

</td><td>

Ask someone for permission to accomplish a task.

</td></tr><tr><td>

Assign to

</td><td>

Choose a person who should fulfill the task.

</td></tr><tr><td>

Create task

</td><td>

Specify a process that must be done as part of the playbook.

</td></tr><tr><td>

Send an email

</td><td>

Send an email to one or more people. You can specify images and enrich text for the email that gets sent automatically.

</td></tr><tr><td>

Placeholder

</td><td>

Set an undefined activity to be specified later, or a more advanced activity such as an email notification, when an activity is completed.Placeholder activities don't have any logic assigned to them yet, and must be edited in Workflow Studio. Or, you can swap them out later for another type of activity in Creator Studio.

</td></tr></tbody>
</table>    ![Select which type of activity to add](../image/cs-add-activity-email.png "Activity library for a playbook")

    Your new activity and its Activity properties panel appear, where you define what the activity is.

8.  Enter the basic details for the activity.

    |Field|Description|
    |-----|-----------|
    |Name|Unique, user-facing name for your activity, which appears to agents and fulfillers while the playbook is running.|
    |Description|Optional details about what the activity accomplishes.|

    ![Activity details panel](../image/cs-assign-to-properties.png "Activity details panel")

9.  If needed, specify the approver or assignee in the **Select an approver** or **Select an assignee** fields.

    Approvers and assignees are the person or people who must approve the task, or who the task gets assigned to. The options are:

    -   **Group**: Enter one or more user groups in the field that appears. For example, `App engine Admins`.
    -   **Specific person**: Enter the person's name as it appears on the ServiceNow AI Platform. If you entered a group, you can select only from users in the specified group.
    -   **Requester's manager**: \(Request approval activities only\) Automatically routes the approval to the manager of the person who's making the request.
10. Enter details for specific types of activities.

    1.  For Request approval activities only, specify the **Approval type**.

        Approval type defines whether a single approver is needed or if everyone must approve the request. The options are:

        -   **Anyone approves**: Only one of the specified approvers must approve the request.
        -   **All approve**: Every one of the specified approvers must approve the request.

            If you select this option and specified a group, all members of the group must approve the request.

    2.  For Create task activities, specify the **Priority**.

        The options are:

        -   **Critical**
        -   **High**
        -   **Moderate**
        -   **Low**
        -   **Planning**
    3.  For Send an email activities, specify the recipients and contents of the email.

        -   Enter the name \(for ServiceNow AI Platform users\) or email address for people who should receive the email in the **To** and **Cc** fields.

            Select the **Requester** option for the **To** or **Cc** fields to include the person who made the request in the email's recipients.

        -   Enter the email's subject in the **Subject** field.
        -   Enter the body of the email in the textbox. Select the additional toolbar buttons icon \(![](../image/cs-more-actions-icon.png)\) to display more formatting options. For example, you can add images, tables, and links to the email.
11. Select at what point the activity should start running in the **When to start** field of the Conditions section.

    The options are:

    -   **When playbook starts**: The approval request runs when the trigger occurs, which is the form's record being created or updated.
    -   **After specific activity**: The approval request runs after one or more activities run, which you must specify in the **Starts after** field. You can select only activities that occur sequentially before the activity you're working on.

        **Note:** This option isn't available for the first activity in a playbook.

12. Define any extra conditions that must be met for the activity to happen by selecting **+ Add conditions**.

    Use the condition builder that appears to specify any other things that must happen for the activity to run. For more information, see [Create a condition statement using the condition builder](https://www.servicenow.com/docs/access?context=create-cond-state-using-cond-build&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

13. Select the **Save and close** button to finish setting up your activity.


## What to do next

Continue adding activities and decisions, as well as connectors and parallel processes if needed, to finish creating your playbook. For more information on decisions, see [Add a decision to an app's playbook in Creator Studio](creator-studio-add-decision-automation.md).

**Parent Topic:**[Working with automation in Creator Studio](../concept/creator-studio-working-with-automations.md)

