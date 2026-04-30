---
title: Publish a form for your app in Creator Studio
description: Publishing forms once they're ready makes them available as catalog items in the production instance for published apps.
locale: en-US
release: xanadu
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Working with forms in Creator Studio, Building apps with Creator Studio, Creator Studio, Building no-code applications, Developing your application, Building applications]
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

3.  Select to **Preview** how different forms appear in various experiences, or select the **View** or **Edit** button to view or edit the application experience.

    Select different previewing options if you want to make sure that you've selected the correct application and see how it will appear in the following formats:

    -   **Portal** \(see a preview of how it'll appear on a desktop website\)
    -   **Now Mobile** \(see a preview of how it'll appear on a mobile phone or device\)
    -   **Virtual agent** \(see a representation of how it'll appear on a chatbot interface\)

        **Note:** Your organization should have the correct plugins installed to see how the form will appear in Virtual Agent. If you're interested, ask your admin and see [Catalog builder preview topic conversation](https://www.servicenow.com/docs/access?context=catalog-builder-preview-topic&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) for more information on previewing forms and their catalog items in Virtual Agent.

    The **View** button displays forms that have been published and doesn't explicitly create a new draft form for development. The **Edit** button takes you to a development form, for example, a new draft version of a form that's already been published.

    ![Preview how your app will look](../image/crs-portal-preview.png "Preview the app's experience")

    You can also check out a representation of how the form submissions workspace will appear by selecting the **Submissions** preview, as well as the records your app generates for it \(by selecting the **Record** preview\).

4.  Check that you're working on the correct form in your app by selecting it from the **Request forms** tab.

5.  Select the **Mark as ready** button.

    ![Mark your app as ready](../image/cs-mark-as-ready.png)


## Result

The catalog item for the form is ready to be deployed with your app. Once the app is deployed, the form is available in the associated service catalog. If the form's app hasn't been deployed, you need to deploy it.

**Parent Topic:**[Working with forms in Creator Studio](../concept/creator-studio-work-with-forms.md)

