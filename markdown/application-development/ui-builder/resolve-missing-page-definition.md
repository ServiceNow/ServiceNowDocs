---
title: Resolve a missing page definition in UI Builder
description: Fix UI Builder page render errors by linking a page definition in the variant record.
locale: en-US
release: australia
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage UI Builder pages and page variants, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Resolve a missing page definition in UI Builder

Fix UI Builder page render errors by linking a page definition in the variant record.

## Before you begin

Role required: ui\_builder\_admin

## About this task

Pages in UI Builder are backed by a screen record \(`sys_ux_screen`\) that references a page definition. The page definition is a macroponent record that UI Builder renders. If the reference is removed or was not set, for example, after a partial import, a manual database edit, or data corruption, UI Builder cannot render the page.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open the experience containing the page displaying the error.

3.  Select the page displaying the error.

4.  Select **Open variant record**.

5.  Right-click the page with the error.

6.  Select **Copy sys\_id**.

7.  Locate the macroponent by navigating to **All** &gt; **sys\_ux\_macroponent.list**.

8.  Filter the list by the application scope associated with the affected experience.

9.  Find the macroponent record that matches the page you want to restore.

10. Copy the macroponent's name from the list.

11. Return to the experience containing the page displaying the error.

12. Select the page displaying the error.

13. Select **Open variant record**.

14. Select the **UX Screens** tab.

15. Open the screen record by selecting the variant screen name.

16. Enter the macroponent from the previous step in the **Page Definition** field.

17. Select **Update**.


## What to do next

Open the experience containing the page with the error to verify that the error has been resolved.

**Parent Topic:**[Manage UI Builder pages and page variants](../concept/work-pages.md)

