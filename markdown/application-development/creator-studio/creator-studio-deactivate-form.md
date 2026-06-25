---
title: Hide a form from use in the ServiceNow AI Platform in Creator Studio
description: Hiding a catalog item for your app's form effectively makes the form inactive. Hidden forms are unavailable in both the app and the catalog it belongs to.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/application-development/creator-studio/creator-studio-deactivate-form.html
release: yokohama
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2026-06-25"
reading_time_minutes: 1
breadcrumb: [Working with forms in Creator Studio, Building apps with Creator Studio, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Hide a form from use in the ServiceNow AI Platform in Creator Studio

Hiding a catalog item for your app's form effectively makes the form inactive. Hidden forms are unavailable in both the app and the catalog it belongs to.

## Before you begin

To hide a form, you must be given permission to work on the app.

## About this task

Creator Studio doesn't let you delete forms. Instead, hide forms to ensure that workflows stay intact.

You can hide only forms that have already been published. For more information, see [Deploying your Creator Studio app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/creator-studio/creator-studio-publishing-apps.md).

## Procedure

1.  Go to **All** &gt; **App Engine** &gt; **Creator Studio** to see all the apps on the Creator Studio home page.

2.  Open the app that contains the form you want to hide.

3.  Select the form that you want to hide in the navigation panel.

    If you have multiple forms, make sure to select the form you're hiding.

    \[Omitted image "crs-forms-select-multi.png"\] Alt text: Select the appropriate form from the navigation panel

4.  Select the more actions icon \(\[Omitted image "cs-more-actions-icon.png"\] Alt text: More options\).

5.  Select **Form settings**.

    \[Omitted image "crs-form-settings-menu.png"\] Alt text: Menu option to edit form settings

6.  De-select the **Make form visible to others** option.

    \[Omitted image "cs-form-settings-hide.png"\] Alt text: Option to hide a form

7.  Select **Save**.


## What to do next

Your admin must re-deploy the app to hide the inactive form \(catalog item\) on the production instance.

**Parent Topic:**[Working with forms in Creator Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/creator-studio/creator-studio-work-with-forms.md)

