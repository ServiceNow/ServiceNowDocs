---
title: Configure the Upcoming Holiday widget
description: Configure the Upcoming Holiday widget to display location-specific holidays on the Employee Slate home page. Populate the holiday calendar table and control widget visibility through the Admin Console.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-24"
reading_time_minutes: 1
keywords: [Upcoming Holiday widget, holiday calendar, work location, Employee Slate configuration]
breadcrumb: [Calendar and schedule management, Working with Employee Slate capabilities, Employee Slate, Employee Service Management]
---

# Configure the Upcoming Holiday widget

Configure the Upcoming Holiday widget to display location-specific holidays on the Employee Slate home page. Populate the holiday calendar table and control widget visibility through the Admin Console.

## Before you begin

Before you configure the widget, verify the following prerequisites:

-   You have access to the Employee Slate Admin Console.
-   Employee work locations are defined in user records.
-   You have the necessary permissions to modify the holiday calendar table.

Role required: admin

## About this task

The Upcoming Holiday widget displays the next relevant holiday based on the work location of the signed-in employee. The widget queries the holiday calendar table and matches holidays to employee locations automatically.

## Procedure

1.  Navigate to the holiday calendar table in your ServiceNow instance.

    Access the table through the Application Navigator or System Definition tables.

2.  Create a new holiday record for each location and holiday combination.

    Complete the following fields for each holiday:

    |Field|Description|
    |-----|-----------|
    |Holiday name|Name of the holiday as it appears to employees|
    |Holiday date|Date when the holiday occurs|
    |Work location|Location where this holiday applies|
    |Default location|Selected for the fallback location when employee work location is unavailable|

3.  Set one location as the default fallback location.

    Select the **Default location** check box for holidays that should appear when the work location for an employee isn't available.

4.  Access the Employee Slate Admin Console.

    Navigate to the admin interface for Employee Slate configuration.

5.  Locate the Upcoming Holiday widget settings.

    Find the widget configuration options in the Admin Console interface.

6.  Set the widget visibility to **Visible**.

    When set to hidden, the widget doesn't appear on any employee home page regardless of holiday data.

    The widget becomes available for display on employee home pages.

7.  Test the widget display by viewing the Employee Slate home page as different employees.

    Verify that employees see holidays relevant to their work location and that the fallback location works when work location data is missing.


## Result

The Upcoming Holiday widget displays location-specific holidays on the Employee Slate home page. Employees see the next relevant holiday based on their work location, with automatic fallback to the default location when needed.

