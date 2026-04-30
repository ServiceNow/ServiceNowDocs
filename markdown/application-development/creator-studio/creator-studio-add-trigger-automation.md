---
title: Edit the trigger for a playbook in Creator Studio
description: Define the trigger for a playbook in Creator Studio to specify what makes the playbook start running.
locale: en-US
release: yokohama
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [Working with automation in Creator Studio, Building apps with Creator Studio, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Edit the trigger for a playbook in Creator Studio

Define the trigger for a playbook in Creator Studio to specify what makes the playbook start running.

## Before you begin

The trigger initiates a playbook to run on one of the app's forms. For example, when a user selects a specific answer to a question, the playbook begins to run. The form you select must already be configured for you to select it for the trigger.

To edit the trigger for a playbook, you must be given permission to work on the app.

## About this task

**Note:** You can't change a playbook's trigger \(whether the form is submitted or updated to initiate the playbook\) or how frequently it should run after you create the playbook. Instead, create a new playbook with a different trigger.

## Procedure

1.  Go to **All** &gt; **App Engine** &gt; **Creator Studio** to see all the apps on the Creator Studio home page.

2.  Open the app that contains the playbook you want to add actions to.

3.  Select the form that contains the playbook that you want to edit the trigger for.

4.  Select the automation that contains the playbook that you want to edit the trigger for.

    ![Select the automation in the navigation panel](../image/crs-auto-copy-nav.png "Select automation that has the playbook")

5.  Select the **Trigger** \(![](../image/cs-trigger-icon.png)\).

    The Additional properties modal appears, where you can edit some of the trigger's settings.

6.  Make any changes to the trigger's general attributes.

    |Field|Description|
    |-----|-----------|
    |Playbook name|Descriptive name for the playbook you're editing.|
    |Description|Brief explanation of what the playbook does, for example, the end goal for the record type.|

7.  If necessary, change the **Form** whose catalog item generates the record type that you want the playbook to run on.

8.  Change the conditions that must be met for the playbook to begin running by selecting **Add condition set**.

    -   If you want to trigger the playbook based on the value of a column in a table, select the **[Field](../concept/creator-studio-glossary.md#)** that you want to be the trigger, as well as its condition **Operator** and the specific trigger **Value**. For example, when a **Start date** is **after** the **Date** needed.
    -   If you want to trigger the playbook based on the response from a form, select **Questions** as the trigger **Field**. Then select the question you want in the **Question** field, the condition **Operator** and the answer's **Value**.
    ![Use a specific answer to a form's question as trigger](../image/crs-trigger-question-answer.png "Question answer as trigger for an automation")

    Add as many conditions as you need. For more information, see [Create a condition statement using the condition builder](https://www.servicenow.com/docs/access?context=create-cond-state-using-cond-build&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

9.  Save your changes by selecting the **Done** button.


**Parent Topic:**[Working with automation in Creator Studio](../concept/creator-studio-working-with-automations.md)

