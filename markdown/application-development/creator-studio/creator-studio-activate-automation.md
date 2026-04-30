---
title: Activate a playbook in Creator Studio
description: Activating a playbook means that it will run when its related form is created or updated on your non-production, development instance. However, the app must still be deployed to production.
locale: en-US
release: xanadu
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Working with automation in Creator Studio, Building apps with Creator Studio, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Activate a playbook in Creator Studio

Activating a playbook means that it will run when its related form is created or updated on your non-production, development instance. However, the app must still be deployed to production.

## Before you begin

You must resolve any errors in the playbook before you can activate it.

To activate a playbook, you must be given permission to work on the app.

## About this task

You can check the activation status of a playbook at any time in the **Automations** tab header.

![Playbook activation status appears in header](../image/cs-playbook-status.png "Playbook activation status")

If you don't activate a playbook and its app is deployed to production, the automation won't run on the applicable records. However, your App Engine admin can activate the deployed playbook for you.

## Procedure

1.  Go to **All** &gt; **App Engine** &gt; **Creator Studio** to see all the apps on the Creator Studio home page.

2.  Open the app that contains the playbook you want to activate.

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

5.  Check that you're activating the correct playbook in your app by selecting it from the **Automations** tab.

    ![Select automation to activate](../image/cs-select-automation.png "Select automation")

6.  Select the **Activate** button.

    ![Select the button to activate the playbook](../image/cs-playbook-activate-button.png "Activate the playbook")


## Result

The status displayed in **Automations** tab header updates from **Inactive** to **Saving** to **Active**, informing you of when changes are made.

The playbook is ready to be deployed with your app. Once the app is deployed, the form is available in the associated service catalog. If the form's app hasn't been deployed, you need to deploy it.

**Parent Topic:**[Working with automation in Creator Studio](../concept/creator-studio-working-with-automations.md)

