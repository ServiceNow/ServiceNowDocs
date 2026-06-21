---
title: Add a parallel process to an app's playbook in Creator Studio
description: Create parallel processes in Creator Studio to make things happen in your app at the same time.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/application-development/creator-studio/creator-studio-decision-parallel-process-add.html
release: xanadu
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Working with automation in Creator Studio, Building apps with Creator Studio, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Add a parallel process to an app's playbook in Creator Studio

Create parallel processes in Creator Studio to make things happen in your app at the same time.

## Before you begin

To add a parallel process to a playbook, you must be given permission to work on the app.

## About this task

Activities on a process's parallel branches run at the same time as other specified parallel activities. Unlike decision activities, the activities and stages on a parallel can run on the same conditions as other branches.

## Procedure

1.  Go to **All** &gt; **App Engine** &gt; **Creator Studio** to see all the apps on the Creator Studio home page.

2.  Open the app that contains the playbook you want to add a parallel process to.

3.  Select to **Preview** how different forms appear in various experiences, or select the **View** or **Edit** button to view or edit the application experience.

    Select different previewing options if you want to make sure that you've selected the correct application and see how it will appear in the following formats:

    -   **Portal** \(see a preview of how it'll appear on a desktop website\)
    -   **Now Mobile** \(see a preview of how it'll appear on a mobile phone or device\)
    -   **Virtual agent** \(see a representation of how it'll appear on a chatbot interface\)

        **Note:** Your organization should have the correct plugins installed to see how the form will appear in Virtual Agent. If you're interested, ask your admin and see  for more information on previewing forms and their catalog items in Virtual Agent.

    The **View** button displays forms that have been published and doesn't explicitly create a new draft form for development. The **Edit** button takes you to a development form, for example, a new draft version of a form that's already been published.

    \[Omitted image "crs-portal-preview.png"\] Alt text: Preview how your app will look

    You can also check out a representation of how the form submissions workspace will appear by selecting the **Submissions** preview, as well as the records your app generates for it \(by selecting the **Record** preview\).

4.  Select the **Automations** tab in the application header.

5.  Check that you're editing the correct playbook in your app by selecting it from the **Automations** tab.

    \[Omitted image "cs-automation-tab-selection.png"\] Alt text: Selection of a playbook from the Automations tab

6.  Choose one of the following ways to add a parallel branch in the diagram view.

    -   Select the add icon \(\[Omitted image "cs-add-icon.png"\] Alt text:\) and choose the **Add a parallel path** icon \(\[Omitted image "cs-parallel-path-icon.png"\] Alt text:\) in the menu that pops up.
    -   Select the Drag new connecter dot icon \(\[Omitted image "cs-drag-new-connector-icon.png"\] Alt text:\) for the parallel process’s starting activity and drag it to the activity or decision that should be the end point of the parallel process.
    **Note:** If you can't see the Drag new connector dot icon, you might need to hover over the activity to see it.

    \[Omitted image "cs-drag-new-connector.png"\] Alt text: Hover over the activity to see the Drag new connector icon

7.  Add activities to the parallel branch as needed.

    For more information, see [Add activities to an app's playbook in Creator Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/creator-studio/creator-studio-add-activities-automation.md).

8.  If you want to have several activities happen in a parallel process as soon as the playbook is triggered, complete the following steps.

    1.  Display the Board view.

    2.  For each activity that should be happen in parallel when the playbook is triggered, select the activity's card and set the **When to start** field to **When playbook starts**.

    3.  Select the **Save and close** button.


**Parent Topic:**[Working with automation in Creator Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/creator-studio/creator-studio-working-with-automations.md)

