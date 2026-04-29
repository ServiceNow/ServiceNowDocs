---
title: Duplicate existing records with Mobile App Builder
description: Using Mobile App Builder \(MAB\) you can duplicate existing records with their associated child records. You can then use these duplicated records as a template from which you can create new screens and cards.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using the Mobile App Builder, Mobile App Builder, Building tools, Building mobile apps, Mobile Platform]
---

# Duplicate existing records with Mobile App Builder

Using Mobile App Builder \(MAB\) you can duplicate existing records with their associated child records. You can then use these duplicated records as a template from which you can create new screens and cards.

## Before you begin

Role required: admin or delegated developer

## About this task

The ability to duplicate records is available for the following record types:

-   List screen
-   Input form screen
-   Launcher screen
-   Function
-   Cards and card templates

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the **Screens** or the **Cards &amp; icons** category for the type of record that you want to duplicate, and then search for the screen or card you want to use as a template.

4.  In the upper right corner of the screen or card form, select the menu \(![More menu button.](../image/mab-button-more.png)\), and then select **Duplicate**.

    ![Mobile App Builder showing the 'Duplicate' menu.](../image/mab-dup-rec-dup-menu.png)

    **Note:** The **Duplicate** option might be turned off for one of the following reasons:

    -   If the record you selected to duplicate is a 'floor node' and displays a message that says the record has been partially loaded. In this case, select **Open record** and the **Duplicate** option becomes available.
    -   If the content tree for the record you want to duplicate has any unsaved changes. Save all changes and then the **Duplicate** option becomes available.
    -   If the content tree for the record you want to duplicate references any records for which you don't have permission to view.
    After selecting **Duplicate**, a modal dialog box appears where you can customize the new record.

5.  In the modal dialog box, name the record, select the **Application scope** from the drop-down list, and then select **Create**.

    ![Modal dialog box.](../image/mab-dup-rec-modal-dialog.png)

    **Note:**

    -   Most of the child records are automatically renamed when you create a new name for the parent record. Only child records that act as a property type such as **Min** or **Max** or those child records whose name appears on screen to end users retain their original name.
    -   The child records that have a green check mark \(![Green check mark image.](../image/green-check-mark.png)\) next to them in the Preview section of the modal dialog box are duplicated for the new screen or card. If no check mark appears next to a child record, that means the original record is reused for the new screen or card.
    -   Records can be duplicated into a different application scope. Any cross-scope records are consolidated into one destination scope.
6.  In the Success dialog box, you can select **Continue editing existing record** to make further changes to the original record or select **Go to record** to view the new duplicated screen or card.

    ![Success dialog box.](../image/mab-dup-rec-succ-msg.png)

7.  Make any additional changes to child records in the new duplicated screen or card, and then select **Save**.

    For example, you might need to change the table from where the data is retrieved, so you might need to edit the Data Item for a duplicated screen.


