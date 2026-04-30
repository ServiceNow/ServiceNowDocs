---
title: Edit a playbook in Creator Studio
description: Update a playbook to change its settings, or rearrange or remove tasks, to make it work for your app.
locale: en-US
release: xanadu
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Working with automation in Creator Studio, Building apps with Creator Studio, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Edit a playbook in Creator Studio

Update a playbook to change its settings, or rearrange or remove tasks, to make it work for your app.

## Before you begin

To edit a playbook, you must be given permission to work on the app.

## About this task

**Note:**

Not all items that can be added to playbooks are supported in Creator Studio, for example, notifications.

If you want to add complex, unsupported items to a playbook \(such as optional activities, multiple stages, or data pills from previous activities\), you must open and edit that playbook in Workflow Studio. After you edit a playbook in Workflow Studio, you can't edit it in Creator Studio. However, you can still work on the rest of the app in Creator Studio.

## Procedure

1.  Go to **All** &gt; **App Engine** &gt; **Creator Studio** to see all the apps on the Creator Studio home page.

2.  Open the app that contains the playbook you want to edit.

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

    ![Selection from the Automations tab](../image/cs-automation-tab-selection.png)

6.  Address any errors in the playbook's logic by selecting the error message icon.

    In the error tray that appears, you can open the properties to fix each error by selecting the **Location** link.

    ![Select the error location to open it](../image/cs-automation-errors.png)

7.  Edit the playbook's settings.

    1.  Select the more actions icon \(![](../image/cs-more-actions-icon.png)\) and select **Properties**.

    2.  Update any of the settings.

        **Note:** You can't change a playbook's trigger once it's created. Instead, add a new playbook with a different trigger.

    3.  Select the **Done** button.

8.  Rearrange the order of tasks as needed.

    1.  Display the **Board view** for the playbook.

    2.  Drag the cards for each activity into the order that you want.

    Creator Studio automatically saves the changes.

9.  Swap a placeholder activity if you want to replace it with another activity type.

    1.  Hover over the placeholder activity and select the replace activity icon \(![Replace activity icon](../image/crs-replace-icon.png)\) to directly open the activity picker.

        ![Select the replace activity icon](../image/crs-swap-placeholder.png "Swap out a placeholder activity")

    2.  Select the new activity from the activity picker.

    3.  Update the **Label** and **Description** as needed, or any of the other properties of the activity.

        For more information, see [Add activities to an app's playbook in Creator Studio](creator-studio-add-activities-automation.md).

10. Delete any unnecessary activities by hovering over the activity and selecting the delete icon \(![](../image/cs-delete-icon.png)\).

11. Make any advanced edits in Workflow Studio by selecting the more actions icon \(![](../image/cs-more-actions-icon.png)\) and selecting **Open in Workflow Studio**.


**Parent Topic:**[Working with automation in Creator Studio](../concept/creator-studio-working-with-automations.md)

