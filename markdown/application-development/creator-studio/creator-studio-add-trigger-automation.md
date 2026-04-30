---
title: Edit the trigger for a playbook in Creator Studio
description: Define the trigger for a playbook in Creator Studio to specify what makes the playbook start running.
locale: en-US
release: xanadu
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Working with automation in Creator Studio, Building apps with Creator Studio, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Edit the trigger for a playbook in Creator Studio

Define the trigger for a playbook in Creator Studio to specify what makes the playbook start running.

## Before you begin

The trigger initiates a playbook to run on one of the app's forms. For example, when a user selects a specific answer to a question, the playbook begins to run.The form you select must already be configured for you to select it for the trigger.

To edit the trigger for a playbook, you must be given permission to work on the app.

## About this task

**Note:** You can't change a playbook's trigger \(whether the form is submitted or updated to initiate the playbook\) or how frequently it should run after you create the playbook. Instead, create a new playbook with a different trigger.

## Procedure

1.  Go to **All** &gt; **App Engine** &gt; **Creator Studio** to see all the apps on the Creator Studio home page.

2.  Open the app that contains the playbook you want to add actions to.

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

    ![Selection of a playbook from the Automations tab](../image/cs-automation-tab-selection.png)

6.  Select the **Trigger** \(![](../image/cs-trigger-icon.png)\).

    The Additional properties modal appears, where you can edit some of the trigger's settings.

7.  Make any changes to the trigger's general attributes.

    |Field|Description|
    |-----|-----------|
    |Playbook name|Descriptive name for the playbook you're editing.|
    |Description|Brief explanation of what the playbook does, for example, the end goal for the record type.|

8.  If necessary, change the **Form** whose catalog item generates the record type that you want the playbook to run on.

9.  Change the conditions that must be met for the playbook to begin running by selecting **Add condition set**.

    -   If you want to trigger the playbook based on the value of a column in a table, select the **[Field](../concept/creator-studio-glossary.md#)** that you want to be the trigger, as well as its condition **Operator** and the specific trigger **Value**. For example, when a **Start date** is **after** the **Date** needed.
    -   If you want to trigger the playbook based on the response from a form, select **Questions** as the trigger **Field**. Then select the question you want in the **Question** field, the condition **Operator** and the answer's **Value**.
    ![Use a specific answer to a form's question as trigger](../image/crs-trigger-question-answer.png "Question answer as trigger for an automation")

    Add as many conditions as you need. For more information, see [Create a condition statement using the condition builder](https://www.servicenow.com/docs/access?context=create-cond-state-using-cond-build&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

10. Save your changes by selecting the **Done** button.


**Parent Topic:**[Working with automation in Creator Studio](../concept/creator-studio-working-with-automations.md)

