---
title: Change the layout of an app's record in Creator Studio
description: Adjust how the records that your app generates will look, such as the order in which fields appear.
locale: en-US
release: xanadu
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Working with form submission workspaces in Creator Studio, Building apps with Creator Studio, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Change the layout of an app's record in Creator Studio

Adjust how the records that your app generates will look, such as the order in which fields appear.

## Before you begin

To change the layout of an app's record in the form submission workspace, you must be given permission to work on the app.

## About this task

All columns of the app's Task table are available as fields on the record page, though you may want to adjust them. For example, you may want to move the **Priority** field to appear more visibly on the record so fulfillers can tell how important the request is. You could then build an automated playbook that runs when the priority changes to high.

**Note:** You can't edit UI policies or make more advanced edits to the form in Creator Studio. To make advanced edits, open the record in Table Builder. For more information, see [Forms in Table Builder](../../../administer/form-builder/concept/form-view-configuration.md).

## Procedure

1.  Go to **All** &gt; **App Engine** &gt; **Creator Studio** to see all the apps on the Creator Studio home page.

2.  Open the app that contains the form submissions workspace you want to edit.

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

5.  Select the **Open record details** button.

    ![Open record details button](../image/cs-open-record-details.png "Open record details button")

    The Record details appear in a new **Record** application tab.

6.  Make any additional changes to how the record appears, such as moving the fields around.

    Check out [Important Task table fields](https://www.servicenow.com/docs/access?context=r_ImportantTaskTableFields&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) for a list of the most commonly used fields that you can work with and their definitions.

    ![Record details in the editor to design how the record appears](../image/cs-record-details.png "Record details")

7.  Select **Save**.


## What to do next

After you're done customizing how the app's records will appear, you can check out how they'll look in the Request App Workspace while remaining in Creator Studio. For more information, see [Preview how an app's records appear](creator-studio-preview-record.md).

**Parent Topic:**[Working with form submission workspaces in Creator Studio](../concept/creator-studio-form-submissions-workspace-about.md)

