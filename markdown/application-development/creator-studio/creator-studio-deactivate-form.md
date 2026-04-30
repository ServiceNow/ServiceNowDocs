---
title: Hide a form from use in the ServiceNow AI Platform in Creator Studio
description: Hiding a catalog item for your app's form effectively makes the form inactive. Hidden forms are unavailable in both the app and the catalog it belongs to.
locale: en-US
release: yokohama
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Working with forms in Creator Studio, Building apps with Creator Studio, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Hide a form from use in the ServiceNow AI Platform in Creator Studio

Hiding a catalog item for your app's form effectively makes the form inactive. Hidden forms are unavailable in both the app and the catalog it belongs to.

## Before you begin

To hide a form, you must be given permission to work on the app.

## About this task

Creator Studio doesn't let you delete forms. Instead, hide forms to ensure that workflows stay intact.

You can hide only forms that have already been published. For more information, see [Deploying your Creator Studio app](../concept/creator-studio-publishing-apps.md).

## Procedure

1.  Go to **All** &gt; **App Engine** &gt; **Creator Studio** to see all the apps on the Creator Studio home page.

2.  Open the app that contains the form you want to hide.

3.  Select the form that you want to hide in the navigation panel.

    If you have multiple forms, make sure to select the form you're hiding.

    ![Select the appropriate form from the navigation panel](../image/crs-forms-select-multi.png "Select the form")

4.  Select the more actions icon \(![More options](../image/cs-more-actions-icon.png)\).

5.  Select **Form settings**.

    ![Menu option to edit form settings](../image/crs-form-settings-menu.png "Form settings menu option")

6.  De-select the **Make form visible to others** option.

    ![Option to hide a form](../image/cs-form-settings-hide.png "Form settings modal")

7.  Select **Save**.


## What to do next

Your admin must re-deploy the app to hide the inactive form \(catalog item\) on the production instance.

**Parent Topic:**[Working with forms in Creator Studio](../concept/creator-studio-work-with-forms.md)

