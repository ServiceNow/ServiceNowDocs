---
title: Analytics User manager
description: The Analytics user manager provides the user managers with reports of time sheet exceptions, and category wise time reported by the users.The Analytics User manager shows the time sheet reports for the users.
locale: en-US
release: xanadu
product: Time Card Management
classification: time-card-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Time Card management, Project Portfolio Management, Strategic Portfolio Management]
---

# Analytics User manager

The Analytics user manager provides the user managers with reports of time sheet exceptions, and category wise time reported by the users.

**Important:** Starting with Xanadu release, **User Manager Dashboard** is renamed to **Analytics User manager** for new customers.

The dashboard can be activated using the Performance Analytics - Content Pack - Project Portfolio Suite Dashboards plugin \(com.snc.pps\_dashboards\). You require Performance Analytics license to use this dashboard.

The dashboard displays time sheet reports only for those time card users who have the **Manager** field on [User form](https://www.servicenow.com/docs/access?context=t_CreateAUser&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) set to the current user.

The reports in the dashboard are filtered based on **Date** range, and **User** selected.

The Analytics user manager consists of these components:

## Time sheet exception count

It displays the total count of entries in **Time sheet exceptions** report.

![Screenshot for Time Sheet Exception Count section](../image/TimesheetExceptionCount.png "Time sheet exception count")

## Time sheet exceptions report

The Time sheet exceptions report lists the users who did not submit/create their time sheets, and the time sheets which are not yet approved for the selected user, and time range. The report displays the following data:

-   **User**: The time card user whose manager in User profile is the current user. If there are more than one time sheets for a user in a given date range which are not submitted or require approval, then multiple entries are listed for the user.
-   **Week starts on**: Starting date of the time sheet week in the selected time range.
-   **State**: State of the time card. Time sheet entries with state as **Not Submitted** are also listed if a time sheet is not created for the week.

The report is generated from the time\_sheet\_exception table. It requires the schedule job **Time Sheet Exceptions** to be running to get the up-to date information.

![Screenshot for Time Sheet Exceptions report](../image/TimeSheetExceptions.png "Time sheet exceptions report")

## Total approved hours

It displays the total approved hours in all categories displayed in **Time by category** report.

![Screenshot for total approved hours in all categories](../image/UserDashboardTotalHours.png "Total approved hours")

## Time by category report

The bar chart report displays the time approved against each category for the selected users whose manager in User profile is the current user.

![Screenshot for Time by Category report](../image/TimeByCategory.png "Time by category report")

**Parent Topic:**[Time Card Management](time-card-management.md)

## Use the Analytics User manager

The Analytics User manager shows the time sheet reports for the users.

### Before you begin

Role required: resource\_manager, timecard\_admin

### About this task

**Important:** Starting with Xanadu release, **User Manager Dashboard** is renamed to **Analytics User manager** for new customers.

The dashboard displays time sheet reports only for those time card users who have the **Manager** field on [User form](https://www.servicenow.com/docs/access?context=t_CreateAUser&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) set to you.

### Procedure

1.  Navigate to **All** &gt; **Time Sheets** &gt; **Analytics User manager**.

2.  Select a date range and user from the **Date** and **User** choice lists.

3.  Review the displayed reports and take necessary actions, if required.


