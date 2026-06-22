---
title: Hide a form from use in the ServiceNow AI Platform in Creator Studio
description: Hiding a catalog item for your app's form effectively makes the form inactive. Hidden forms are unavailable in both the app and the catalog it belongs to.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/application-development/creator-studio/creator-studio-deactivate-form.html
release: xanadu
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Working with forms in Creator Studio, Building apps with Creator Studio, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Hide a form from use in the ServiceNow AI Platform in Creator Studio

Hiding a catalog item for your app's form effectively makes the form inactive. Hidden forms are unavailable in both the app and the catalog it belongs to.

## Before you begin

To hide a form, you must be given permission to work on the app.

## About this task

Creator Studio doesn't let you delete forms. Instead, hide forms to ensure that workflows stay intact.

You can hide only forms that have already been published. For more information, see [Deploying your Creator Studio app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/creator-studio/creator-studio-publishing-apps.md).

## Procedure

1.  Go to **All** &gt; **App Engine** &gt; **Creator Studio** to see all the apps on the Creator Studio home page.

2.  Open the app that contains the form you want to hide.

3.  Select to **Preview** how different forms appear in various experiences, or select the **View** or **Edit** button to view or edit the application experience.

    Select different previewing options if you want to make sure that you've selected the correct application and see how it will appear in the following formats:

    -   **Portal** \(see a preview of how it'll appear on a desktop website\)
    -   **Now Mobile** \(see a preview of how it'll appear on a mobile phone or device\)
    -   **Virtual agent** \(see a representation of how it'll appear on a chatbot interface\)

        **Note:** Your organization should have the correct plugins installed to see how the form will appear in Virtual Agent. If you're interested, ask your admin and see [Catalog builder preview topic conversation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/servicenow-platform/service-catalog/catalog-builder-preview-topic.md) for more information on previewing forms and their catalog items in Virtual Agent.

    The **View** button displays forms that have been published and doesn't explicitly create a new draft form for development. The **Edit** button takes you to a development form, for example, a new draft version of a form that's already been published.

    \[Omitted image "crs-portal-preview.png"\] Alt text: Preview how your app will look

    You can also check out a representation of how the form submissions workspace will appear by selecting the **Submissions** preview, as well as the records your app generates for it \(by selecting the **Record** preview\).

4.  Select the form for the catalog item you want to hide in the **Request forms** header tab.

    \[Omitted image "cs-request-forms-tab.png"\] Alt text: Request forms tab

5.  Select the more actions icon \(\[Omitted image "cs-more-actions-icon.png"\] Alt text: More options\).

6.  Select **Form settings**.

    \[Omitted image "cs-form-settings-menu.png"\] Alt text: Menu option to edit form settings

7.  De-select the **Make form visible to others** option.

    \[Omitted image "cs-form-settings-hide.png"\] Alt text: Option to hide a form

8.  Select **Save**.


## What to do next

You must re-deploy the app to hide the inactive form \(catalog item\) on the production instance.

**Parent Topic:**[Working with forms in Creator Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/creator-studio/creator-studio-work-with-forms.md)

