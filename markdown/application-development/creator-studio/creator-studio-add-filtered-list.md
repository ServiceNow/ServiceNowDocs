---
title: Add a filtered list to a workspace in Creator Studio
description: Create custom filtered lists in the app submission workspace to view records that meet specific conditions. For example, if your app has multiple forms, you can create a list for each form by filtering on the record type.
locale: en-US
release: zurich
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure workspace lists and records, Build apps, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Add a filtered list to a workspace in Creator Studio

Create custom filtered lists in the app submission workspace to view records that meet specific conditions. For example, if your app has multiple forms, you can create a list for each form by filtering on the record type.

## Before you begin

To add a list to a workspace configuration, you must be given permission to work on the app.

## About this task

**Note:** You can create a filtered list to display open records assigned to a specific user, or all requests that have been cancelled.

## Procedure

1.  Go to **All** &gt; **App Engine** &gt; **Creator Studio** to see all the apps on the Creator Studio home page.

2.  Open the app that contains the list configuration that you want to add a list to.

3.  Select the **List configurations** section in the navigation panel.

    If you tested submitting a record using the **Try it** button, the workspace displays the generated records that you can view.

    ![Customize the workspace in the List configurations section](../image/crs-list-configs-whole.png "List configurations in Creator Studio")

4.  Select **Add a filtered list**.

    ![Adding a filtered list details](../image/cs-new-filtered-list.png "Add a filtered list")

5.  Enter a **Name** for the new list in the modal that appears.

    Choose a name to help users easily identify their category in the workspace, such as `HR timeoff requests`.

    **Note:** You can't change the table for the workspace, as it's linked to the app.

6.  Select the **Add** button.

    The new list appears under the category, with its details appearing in the Filtered list details panel.

7.  Select **Apply conditions** in the Filtered list details panel and use the condition builder to specify what types of records the list should contain, selecting **Apply** when you're done.

    For example, you can select **Urgency** as the field and **High** as the value to have the list show only urgent records. For more information, see [Create a condition statement using the condition builder](https://www.servicenow.com/docs/access?context=create-cond-state-using-cond-build&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

    For example, the following conditions specify open and closed requests:

    -   `Active is true` specifies only open records.
    -   `Active is false` specifies only closed records.
8.  Change which columns appear and the order they're displayed in by selecting **Manage columns**.

    1.  Move columns from **Available columns** to **Selected columns** in the Manage columns dialog box.

    2.  Drag to rearrange the columns.

    3.  Select **Apply**.

9.  Ensure that the **Activate list** option is selected.


## Result

Your new list will appear in the Request App Workspace after your admin deploys it!

**Parent Topic:**[Configuring workspace lists and records for form submissions](../concept/creator-studio-form-submissions-workspace-about.md)

