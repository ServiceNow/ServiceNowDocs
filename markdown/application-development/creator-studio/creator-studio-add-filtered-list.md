---
title: Add a filtered list to a workspace in Creator Studio
description: Create custom filtered lists in an app's workspace to view records that meet specific conditions. For example, if your app has multiple forms, you can create a list for each form by filtering on the record type.
locale: en-US
release: xanadu
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Working with form submission workspaces in Creator Studio, Building apps with Creator Studio, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Add a filtered list to a workspace in Creator Studio

Create custom filtered lists in an app's workspace to view records that meet specific conditions. For example, if your app has multiple forms, you can create a list for each form by filtering on the record type.

## Before you begin

To add a list to a workspace, you must be given permission to work on the app.

## About this task

**Note:** You can create a filtered list to display open records assigned to a specific user, or all requests that have been cancelled.

## Procedure

1.  Go to **All** &gt; **App Engine** &gt; **Creator Studio** to see all the apps on the Creator Studio home page.

2.  Open the app that contains the workspace you want to add a list to.

3.  Select to **Preview** how different forms appear in various experiences, or select the **View** or **Edit** button to view or edit the application experience.

    Select different previewing options if you want to make sure that you've selected the correct application and see how it will appear in the following formats:

    -   **Portal** \(see a preview of how it'll appear on a desktop website\)
    -   **Now Mobile** \(see a preview of how it'll appear on a mobile phone or device\)
    -   **Virtual agent** \(see a representation of how it'll appear on a chatbot interface\)

        **Note:** Your organization should have the correct plugins installed to see how the form will appear in Virtual Agent. If you're interested, ask your admin and see [Catalog builder preview topic conversation](https://www.servicenow.com/docs/access?context=catalog-builder-preview-topic&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) for more information on previewing forms and their catalog items in Virtual Agent.

    The **View** button displays forms that have been published and doesn't explicitly create a new draft form for development. The **Edit** button takes you to a development form, for example, a new draft version of a form that's already been published.

    ![Preview how your app will look](../image/crs-portal-preview.png "Preview the app's experience")

    You can also check out a representation of how the form submissions workspace will appear by selecting the **Submissions** preview, as well as the records your app generates for it \(by selecting the **Record** preview\).

4.  Select the **Form submissions** tab in the application header.

    ![Form submission workspace in Creator Studio](../image/cs-corm-sub-workspace.png "Form submission workspace in Creator Studio")

5.  Select **Add a filtered list**.

    ![Adding a filtered list details](../image/cs-new-filtered-list.png "Add a filtered list")

6.  Enter a **Name** for the new list in the modal that appears.

    Choose a name to help users easily identify their category in the workspace, such as `HR timeoff requests`.

    **Note:** You can't change the table for the workspace, as it's linked to the app.

7.  Select the **Add** button.

    The new list appears under the category, with its details appearing in the Filtered list details panel.

8.  Select **Apply conditions** in the Filtered list details panel and use the condition builder to specify what types of records the list should contain, selecting **Apply** when you're done.

    For example, you can select **Urgency** as the field and **High** as the value to have the list show only urgent records. For more information, see [Create a condition statement using the condition builder](https://www.servicenow.com/docs/access?context=create-cond-state-using-cond-build&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

    For example, the following conditions specify open and closed requests:

    -   `Active is true` specifies only open records.
    -   `Active is false` specifies only closed records.
9.  Change which columns appear and the order they're displayed in by selecting **Manage columns**.

    1.  Move columns from **Available columns** to **Selected columns** in the Manage columns dialog box.

    2.  Drag to rearrange the columns.

    3.  Select **Apply**.

10. Ensure that the **Activate list** option is selected.


## Result

Your new list will appear in the Request App Workspace after your admin deploys it!

**Parent Topic:**[Working with form submission workspaces in Creator Studio](../concept/creator-studio-form-submissions-workspace-about.md)

