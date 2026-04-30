---
title: Verify Lifecycle Events Employee requests configuration
description: Use the Preview and Test capabilities to verify that the employee request activity has been configured correctly.
locale: en-US
release: yokohama
product: Lifecycle Events
classification: lifecycle-events
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Lifecycle Events employee requests, Using Lifecycle Events, Lifecycle Events, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Verify Lifecycle Events Employee requests configuration

Use the Preview and Test capabilities to verify that the employee request activity has been configured correctly.

## Before you begin

Role required: sn\_hr\_le.admin or admin

## About this task

Verify that the **Request Change in Start Date** option is available when you view the requests that employees can make for the activity set that you're testing.

This task requires that you download the demo data that is provided with the Human Resources Scoped App: Lifecycle Events for Enterprise.

## Procedure

1.  Navigate to **All** &gt; **Lifecycle Events** &gt; **Administration** &gt; **Manage Lifecycle Events**.

2.  Select **New Hire Onboarding \(Demo\)**, and then select the **Activity Sets** tab.

    **Note:** If you don't see this life-cycle event, download the demo data provided with the Human Resources Scoped App: Lifecycle Events for Enterprise.

3.  Select the **Test Activity Sets** icon.

4.  Select **Preview**, and then select **Test**.

    Wait for the confirmation message "New Hire Onboarding \(Demo\) case created..." to display.

    **Note:** In preview mode, all employee requests appear regardless of audience, Opened for, or Subject person settings. Employee requests for the appropriate configuration appear in the completed test results.

5.  Navigate to **All** &gt; **Self-Service** &gt; **Employee Center**.

6.  From the Employee Center global header, select **My Tasks**.

7.  Select the first task in the My tasks widget associated with the new hire onboarding activity set that you created via your test.

    More information about the task you selected appears in the My tasks widget.

8.  Select the link that reflects the name of the activity set that you're testing for new hire onboarding.

    **Note:** This link appears underneath the title of the task that you selected in the My tasks widget.

    The Journey details page appears.

9.  Select the **More Journey actions** icon.

    A list of options appear for the employee requests associated with the activity set that you're testing.

10. Verify that the **Request Change in Start Date** option appears in the list of employee requests associated with the activity set.

    **Note:** The options associated with the **More Journey actions** icon depend on the audience configuration for the employee request. In this example that uses demo data, all employees see the **Request Change in Start Date** option.


**Parent Topic:**[Lifecycle Events employee requests](../concept/employee-requests.md)

