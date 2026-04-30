---
title: Activate a playbook in Creator Studio
description: Activating a playbook means that it will run when its related form is created or updated on your non-production, development instance. However, the app must still be deployed to production.
locale: en-US
release: yokohama
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Working with automation in Creator Studio, Building apps with Creator Studio, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Activate a playbook in Creator Studio

Activating a playbook means that it will run when its related form is created or updated on your non-production, development instance. However, the app must still be deployed to production.

## Before you begin

You must resolve any errors in the playbook before you can activate it.

To activate a playbook, you must be given permission to work on the app.

## About this task

You can check the activation status of a playbook at any time in the app header.

![Playbook activation status appears in header](../image/cs-playbook-status.png "Playbook activation status")

If you don't activate a playbook and its app is deployed to production, the automation won't run on the applicable records. However, your App Engine admin can activate the deployed playbook for you.

## Procedure

1.  Go to **All** &gt; **App Engine** &gt; **Creator Studio** to see all the apps on the Creator Studio home page.

2.  Open the app that contains the playbook you want to activate.

3.  Select the form that contains the playbook that you want to activate.

4.  Select the automation that contains the playbook that you want to activate.

    ![Select the automation in the navigation panel](../image/crs-auto-copy-nav.png "Select automation that has the playbook")

5.  Select the **Activate** button.

    ![Select the Activate button to activate the playbook](../image/crs-playbook-activate-btn.png "Activate the playbook")


## Result

The status displayed in the app header updates from **Inactive** to **Saving** to **Active**, informing you of when changes are made.

The playbook is ready to be deployed with your app. Once the app is deployed, the form is available in the associated service catalog. If the form's app hasn't been deployed, you need to deploy it.

**Parent Topic:**[Working with automation in Creator Studio](../concept/creator-studio-working-with-automations.md)

