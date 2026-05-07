---
title: Duplicate a UI interaction
description: Create an independent copy of an existing UI interaction to use as a starting point for a new interaction or to safely experiment with changes.
locale: en-US
release: australia
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-04-10"
reading_time_minutes: 1
breadcrumb: [UI interactions, Manage actions in UI Builder pages, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Duplicate a UI interaction

Create an independent copy of an existing UI interaction to use as a starting point for a new interaction or to safely experiment with changes.

## Before you begin

Role required: ui\_builder\_admin

## About this task

Duplicating a UI interaction creates an independent copy of the original, including all steps, inputs, and configuration. The duplicate is not linked to the original. Changes to the duplicate do not affect the original interaction or any page events or declarative actions that reference it.

If the UI interaction includes custom UI built with Component Builder, such as a custom modal or modeless dialog, you must also duplicate the custom component separately. The duplicated interaction continues to reference the original component. Update it to reference the new copy.

**Note:** Duplicating a UI interaction does not duplicate any associated declarative actions. If the original interaction is triggered by a declarative action, create or update a declarative action separately to reference the duplicated interaction.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Select the **UI interactions** tab.

3.  In the search field, enter the name of the interaction you want to edit.

    ![UI interactions list with search field highlighted.](../image/uib-uii-search.png "UI interactions list")

4.  Locate the UI interaction record that you want to duplicate.

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

To modify the duplicated interaction, see [Edit an existing UI interaction](edit-ui-interaction.md).

To use your duplicated interaction, trigger it using one of these methods:

-   From declarative action: Corresponding declarative actions are inactive by default and must be enabled to test.
-   From UI Builder page event. See [Trigger a UI interaction from a page event](trigger-ui-interaction-from-page-event.md).

**Parent Topic:**[UI interactions](../concept/uib-ui-interactions.md)

