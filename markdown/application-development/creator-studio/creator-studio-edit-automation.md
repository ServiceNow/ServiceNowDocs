---
title: Edit a playbook in Creator Studio
description: Update a playbook to change its settings, or rearrange or remove tasks, to make it work for your app.
locale: en-US
release: zurich
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Automation in apps, Build apps, Creator Studio, Building no-code applications, Developing your application, Building applications]
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

3.  Select the form that contains the playbook that you want to edit.

4.  Select the automation that contains the playbook that you want to edit.

    ![Select the automation in the navigation panel](../image/crs-auto-copy-nav.png "Select automation that has the playbook")

5.  Address any errors in the playbook's logic by selecting the error message icon.

    In the error tray that appears, you can open the properties to fix each error by selecting the **Location** link.

    ![Select the error location to open it](../image/cs-automation-errors.png)

6.  Edit the playbook's settings.

    1.  Select the more actions icon \(![](../image/cs-more-actions-icon.png)\) and select **Properties**.

    2.  Update any of the settings.

        **Note:** You can't change a playbook's trigger \(whether the form is submitted or updated to initiate the playbook\) or how frequently it should run after you create the playbook. Instead, create a new playbook with a different trigger.

    3.  Select the **Done** button.

7.  Rearrange the order of tasks as needed.

    1.  Display the **Board view** for the playbook.

    2.  Drag the cards for each activity into the order that you want.

    Creator Studio automatically saves the changes.

8.  Swap a placeholder activity if you want to replace it with another activity type.

    1.  Hover over the placeholder activity and select the replace activity icon \(![Replace activity icon](../image/crs-replace-icon.png)\) to directly open the activity picker.

        ![Select the replace activity icon](../image/crs-swap-placeholder.png "Swap out a placeholder activity")

    2.  Select the new activity from the activity picker.

    3.  Update the **Label** and **Description** as needed, or any of the other properties of the activity.

        For more information, see [Add activities to an app's playbook in Creator Studio](creator-studio-add-activities-automation.md).

9.  Delete any unnecessary activities by hovering over the activity and selecting the delete icon \(![](../image/cs-delete-icon.png)\).

10. Make any advanced edits in Workflow Studio by selecting the more actions icon \(![](../image/cs-more-actions-icon.png)\) and selecting **Open in Workflow Studio**.


**Parent Topic:**[Working with automation in Creator Studio](../concept/creator-studio-working-with-automations.md)

