---
title: Add a parallel process to an app's playbook in Creator Studio
description: Create parallel processes in Creator Studio to make things happen in your app at the same time.
locale: en-US
release: zurich
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Automation in apps, Build apps, Creator Studio, Building no-code applications, Developing your application, Building applications]
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

3.  Select the form that contains the playbook that you want to add a parallel process to.

4.  Select the automation that contains the playbook that you want to add a parallel process to.

    ![Select the automation in the navigation panel](../image/crs-auto-copy-nav.png "Select automation that has the playbook")

5.  Choose one of the following ways to add a parallel branch in the diagram view.

    -   Select the add icon \(![](../image/cs-add-icon.png)\) and choose the **Add a parallel path** icon \(![](../image/cs-parallel-path-icon.png)\) in the menu that pops up.
    -   Select the Drag new connecter dot icon \(![](../image/cs-drag-new-connector-icon.png)\) for the parallel process’s starting activity and drag it to the activity or decision that should be the end point of the parallel process.
    **Note:** If you can't see the Drag new connector dot icon, you might need to hover over the activity to see it.

    ![Hover over the activity to see the Drag new connector icon](../image/cs-drag-new-connector.png)

6.  Add activities to the parallel branch as needed.

    For more information, see [Add activities to an app's playbook in Creator Studio](creator-studio-add-activities-automation.md).

7.  If you want to have several activities happen in a parallel process as soon as the playbook is triggered, complete the following steps.

    1.  Display the Board view.

    2.  For each activity that should be happen in parallel when the playbook is triggered, select the activity's card and set the **When to start** field to **When playbook starts**.

    3.  Select the **Save and close** button.


**Parent Topic:**[Working with automation in Creator Studio](../concept/creator-studio-working-with-automations.md)

