---
title: Duplicate a demo UI interaction
description: Create a duplicate of a demo UI interaction example to work with a separate, editable copy.
locale: en-US
release: australia
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Working with UI interaction demo data, UI interactions, Manage actions in UI Builder pages, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Duplicate a demo UI interaction

Create a duplicate of a demo UI interaction example to work with a separate, editable copy.

## Before you begin

Role required: ui\_builder\_admin

## About this task

Demo UI interaction records define sample UI logic and scripts used to demonstrate common interaction patterns.

When you duplicate demo data, you create a separate copy that you can run or customize without impacting the original record. The duplicated interaction is independent of the original demo and can be safely modified. Demo interactions appear in the UI interactions list like any other interaction, allowing you to open, review, or duplicate them for use in your own scope.

**Note:** The Cascade Delete demo interaction example must be duplicated in the global scope for its first server script step to run correctly. This requirement is unique to Cascade Delete; all other demo interaction examples function normally when duplicated in your application scope.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Select the **UI interactions** tab.

3.  In the **Search UI interactions** field, enter `demo`.

    ![UI interactions list with demo interactions listed.](../image/uib-uii-demo-list.png)

    The list filters to show interactions containing **demo** in their labels or descriptions.

4.  Locate the demo data record that you want to duplicate.

5.  Open the record.

6.  Select the **Settings** tab.

    ![Settings tab.](../image/uib-uii-settings-tab.png)

7.  In the record header, select **Duplicate**.

    ![Settings tab for demo interaction with Duplicate action highlighted.](../image/uib-uii-duplicate-demo.png)

8.  Update the Name and Description fields, as needed.

9.  Select **Create**.


## Result

A new UI interaction record is created in your current application scope, ready for editing.

## What to do next

To use your duplicated interaction, trigger it using one of these methods:

-   From declarative action: Corresponding declarative actions are inactive by default and must be enabled to test.
-   From UI Builder page event. See [Trigger a UI interaction from a page event](trigger-ui-interaction-from-page-event.md).

**Parent Topic:**[Working with UI interaction demo data](../concept/working-with-demo-interactions.md)

