---
title: Test one of your forms for an app
description: Use the Try it button on the Request forms tab to submit a request, which triggers any associated playbooks and creates a record that you can work with in Creator Studio.
locale: en-US
release: australia
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Testing and previewing apps, Build apps, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Test one of your forms for an app

Use the **Try it** button on the **Request forms** tab to submit a request, which triggers any associated playbooks and creates a record that you can work with in Creator Studio.

## About this task

Trying out a form differs from the preview that appears when you first view an app in Creator Studio in the following ways:

-   Previewing doesn't submit the form, and thus doesn't generate a record from the form submission.
-   Previewing lets you see how the form will look when accessed in different places, such as a portal, mobile, and Virtual Agent.
-   You can preview a form at any time, but a form must be published for you to test it using the **Try it** button.
-   Testing the form with the **Try it** button runs playbooks and generates a record.
    -   Any automations \(playbooks\) associated with the form are run after you submit the form, and the results are available on the generated record.
    -   You can then use that record, which opens in Creator Studio, to test how the record appears and functions for users in the Request App Workspace.

## Before you begin

You must first create and publish \(mark as ready\) a form for you to test it using the **Try it** button. For more information, see [Publish a form for your app in Creator Studio](creator-studio-publish-form.md).

To test an app, you must be given permission to work on the app.

## Procedure

1.  Head over to **All** &gt; **App Engine** &gt; **Creator Studio**.

    All the apps built in Creator Studio appear on the home page.

2.  Open the application that contains the form you want to try out.

3.  Select the **Try it** button.

    ![Select the Try it button](../image/crs-try-it-btn.png "Try it button")

    The Try form that appears tells you which user will receive your request. For example, the administrator.

4.  Fill in the fields for each question on the form.

5.  Select the **Submit** button when you're done.


## Result

After you submit your responses, the ServiceNow AI Platform runs any playbooks associated with the form.

The record that your submitted form creates appears in Creator Studio. You can view the results of the playbooks and interact with the record to see how it appears in the Request App Workspace.

-   Answers to the form's questions \(which are catalog variables\) appear on the **Details** tab of the submitted record. For more on form questions, see [Working with forms in Creator Studio](../concept/creator-studio-work-with-forms.md).
-   Results of any playbooks appear on the **Automations** tab of the submitted record. For more on playbooks, see [Working with automation in Creator Studio](../concept/creator-studio-working-with-automations.md).

For details, see [Preview how an app's records appear](creator-studio-preview-record.md).

**Parent Topic:**[Testing and previewing Creator Studio apps and records](../concept/creator-studio-testing-apps.md)

