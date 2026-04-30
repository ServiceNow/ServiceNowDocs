---
title: Manage profile tabs and visibility in Employee Profile
description: Enable the display of work-related content in the employee profile to help customize the public profile visibility settings.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Employee profile, Setup task management, Configure, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Manage profile tabs and visibility in Employee Profile

Enable the display of work-related content in the employee profile to help customize the public profile visibility settings.

## Before you begin

You can use the profile tab UI only as follows:

-   When the admin opts in to the employee profile
-   When the employee meets the employee definition
-   When the employee has a corresponding profile record in the employee profile table

Role required: sn\_hr\_sp.esc\_admin

## About this task

Provide employees with a professional landing page and help control the information visibility across the organization. You can use the default tabs or create tabs. Using the tabs UI, you can do the following:

-   Enable admins to configure the profile information in tabs.
-   Configure tabs, widgets, and visibility of profile information.
-   Add information from other widgets such as the HR widget and EX widget.
-   Provide employees the flexibility to personalize the visibility settings.

For employees, the tab UI appears only when more than one tab is available for display.

**Note:** For non-employees, the profile information appears as a flat page with the Employee Profile Overview, Employee Profile My Team, Employee Documents List, Granular Delegation List, and HRI Contacts widgets.

## Procedure

1.  Navigate to **All** &gt; **Employee Profile** &gt; **Profile Tabs**.

2.  Select **New** or open a record.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the tab.|
    |Display Name|Tab name to display on the portal. If this field is empty, the value of the **Name** field is displayed on the portal.|
    |Application|Application for the tab.|
    |Active|Option to activate the widget in the tab for use.|
    |Order|Order number that you want the tab to appear in.|

    When you configure and mark multiple tabs as active, the information is displayed as tabs on the profile.

4.  Select **Submit** or **Update**.

    The tab is created or updated.

5.  From the Tab widget mappings related list, select **New** or edit an existing record.

6.  On the Tab widget mapping form, fill in the fields.

    For a description of the field values, see [Tab widget mapping form](../reference/tab-widget-mapping-form.md). The Tab widget mapping **sys\_id** is available in the **tabWidgetMappingId** variable of the widget options object.

    **Note:** The **widgetTitle**, **tabWidgetMappingId**, and **isUserSelectionEnabled** variables are available only within the scope of the Employee Profile tab UI.

7.  Select **Save** or **Update**.


## Result

The **Profile** tab is configured with the widget and visibility settings for employees to view and personalize the visibility. On the UI, the different tabs are visible in a sticky format even when the user scrolls through the page. All widgets under a particular tab are available in the form of navigation menu items.

The admin can use the instance options to configure the visibility of the navigation menu by selecting the **Widget overview panel** option.

**Related topics**  


[Employee profile](../concept/employee-profile-portal.md)

