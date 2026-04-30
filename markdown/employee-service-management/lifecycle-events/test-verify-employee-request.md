---
title: Verify Lifecycle Events Employee requests configuration
description: Use the Preview and Test capabilities to verify that the employee request activity has been configured correctly.
locale: en-US
release: zurich
product: Lifecycle Events
classification: lifecycle-events
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Lifecycle Events employee requests, Use, Lifecycle Events, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Verify Lifecycle Events Employee requests configuration

Use the Preview and Test capabilities to verify that the employee request activity has been configured correctly.

## Before you begin

Role required: sn\_hr\_le.admin or admin

## About this task

Verify that the Employee request menu item for "Request Change in Start Date" is available in an activity set.

This task requires that you download the demo data that is provided with the Human Resources Scoped App: Lifecycle Events for Enterprise.

## Procedure

1.  Navigate to **All** &gt; **Application** &gt; **Lifecycle Events** &gt; **Administration** &gt; **Manage Lifecycle Events**.

2.  Click **New Hire Onboarding \(Demo\)**, and open the**Activity Sets** tab.

    **Note:** If you don't see this life-cycle event, download the demo data provided with the Human Resources Scoped App: Lifecycle Events for Enterprise.

3.  Click the **Test Activity Sets** icon.

4.  Click **Preview** then click **Test**.

    Wait for the confirmation message "New Hire Onboarding \(Demo\) case created..." to display.

    **Note:** In preview mode, all employee requests appear regardless of audience, Opened for, or Subject person settings. Employee requests for the appropriate configuration appear in the completed test results.

5.  Navigate to **Self-Service** &gt; **Employee Center** and click **To-dos**.

6.  Open the "New Hire Onboarding - administrator" activity set.

    The "New Hire Onboarding - System Administrator" activity set link is below the title of each of the To-dos.

7.  Click **Actions** to view the available menu items.

    Verify that the "Request Change in Start Date" menu item is available in the activity set.

    **Note:** Menu items are visible to different users depending on the audience configuration for the request. In this example that uses demo data, all users see the menu item.


**Parent Topic:**[Lifecycle Events employee requests](../concept/employee-requests.md)

