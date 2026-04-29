---
title: Publish a form for your app in Creator Studio
description: Publishing forms once they're ready makes them available as catalog items in the production instance for published apps.
locale: en-US
release: australia
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Forms in apps, Build apps, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Publish a form for your app in Creator Studio

Publishing forms once they're ready makes them available as catalog items in the production instance for published apps.

## Before you begin

To publish a form, you must be given permission to work on the app.

## About this task

After you publish a form, it's available in the specified catalog on the instance you're working on. However, you still need to deploy your app to the production instance for users to access the form. For more information, see [Deploying your Creator Studio app](../concept/creator-studio-publishing-apps.md).

## Procedure

1.  Go to **All** &gt; **App Engine** &gt; **Creator Studio** to see all the apps on the Creator Studio home page.

2.  Open the application that contains the form you want to publish.

3.  Select the form you want to publish in the navigation panel.

    If you have multiple forms, make sure to select the form you're publishing.

    **Note:** If your app has a lot of forms, you can use the search box in the navigation panel to search for a specific form.

    ![Select the appropriate form from the navigation panel](../image/crs-forms-select-multi.png "Select the form")

4.  Select the **Mark as ready** button.

    ![Mark your app as ready](../image/crs-mark-as-ready-nav.png "Publish a form")

    **Note:** If you haven't specified where the form will live, such as in a catalog or in the Employee Center, you're prompted to **Edit location setting**. For more information, see [Edit the settings for a form in Creator Studio](creator-studio-edit-form-settings.md).


## Result

The catalog item for the form is ready to be deployed with your app. Once the app is deployed, the form is available in the associated service catalog. If the form's app hasn't been deployed, you need to deploy it.

**Note:** If you published a form and then edit it, you can’t use the version that's being edited in a condition for a playbook, for example as a trigger for the automation. However, you can use the published version of the form or publish the version that you’re editing, which makes its question answers available to use in playbook conditions.

**Parent Topic:**[Working with forms in Creator Studio](../concept/creator-studio-work-with-forms.md)

