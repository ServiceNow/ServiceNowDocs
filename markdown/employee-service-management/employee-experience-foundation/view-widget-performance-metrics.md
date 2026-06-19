---
title: View widget performance metrics
description: View the metrics provided by the performance window to identify which widgets take the longest to load data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/employee-experience-foundation/view-widget-performance-metrics.html
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Managing portal performance, Configure, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# View widget performance metrics

View the metrics provided by the performance window to identify which widgets take the longest to load data.

## Before you begin

Role required: sp\_admin

To track the performance of a custom widget, add a hotspot to the script: [Add hotspots to track custom widget performance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/add-hotspots-track-custom-widget-performance.md)

## About this task

The **Performance Details** window provides comprehensive tracking of each widget on a page, enabling better assessment of the user experience. You can view load times, customization status, and display visibility for each widget.

\[Omitted image "performance-details.jpg"\] Alt text: The Performance detailswindow displays widget performance metrics

## Procedure

1.  Navigate to **All** &gt; **Employee Center**.

2.  Select the clock icon to open the **Performance details** window.

    The clock \[Omitted image "clock-icon.jpg"\] Alt text: the clock icon to access the performance details page icon is located at the bottom-left corner of the screen.

3.  Click **Enable Performance Stats**.

4.  Click **Close**.

5.  Impersonate a user to enable the system to capture widget load times for that user.

    1.  Click on your profile image.

    2.  Click **Impersonate**.

        \[Omitted image "ec-impersonate.png"\] Alt text: Impersonate button

    3.  Select the user to impersonate.

    4.  Click on your profile image and **End impersonation**.

        \[Omitted image "ec-end-impersonation.png"\] Alt text: End impersonation button

6.  Select the clock icon to open the **Performance details** window.

7.  In the **Search for user** field, select the user that you impersonated.

8.  Review the **Server time** column to identify which widgets have the longest load times.

9.  Export the data as an Excel file.

10. Click **Close** when you are done.


**Parent Topic:**[Managing portal performance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/improve-manage.md)

