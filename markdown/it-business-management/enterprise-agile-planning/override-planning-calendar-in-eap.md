---
title: Override planning calendar in EAP
description: Flexibly change the planning calendar for your Agile Release Train \(ART\) or Agile Team by overriding the default calendar that is set during configuration of Enterprise Agile Planning.
locale: en-US
release: zurich
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Override planning calendar in EAP

Flexibly change the planning calendar for your Agile Release Train \(ART\) or Agile Team by overriding the default calendar that is set during configuration of Enterprise Agile Planning.

## Before you begin

Set the Application Scope of your ServiceNow instance to Strategic Planning.

Role required: sn\_apw\_advanced.eap\_admin

## About this task

The override calendar option EAP settings helps you change the planning calendar that your teams use in EAP. This way, teams can choose their own planning calendars.

The new calendar takes effect after end date of the current calendar. If you want the calendar to take effect sooner or later, you must add or remove iterations to the current calendar.

The new calendar is automatically applied to child teams. For example, if an ART's planning calendar is changed, all child EAP teams associated with this ART must follow the new planning calendar.

This change is applied to only those ARTs that you update.

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace**.

2.  From the **Settings** menu, select **Agile structure** and navigate to your ART.

3.  From the Details tab of your ART, select a value for the **Override planning calendar** field.

    The planning calendar that you select here must have calendar entries so that iterations can be created for this team and its child teams.

4.  Select **Save**.

    The page shows the date from which the new calendar will override the existing calendar.

    For example, in the screenshot shown here, the new calendar **Planning Interval** is set to override an existing calendar on 2024-07-30. If you choose to go back to using your old calendar:

    -   Before 2024-07-30, clear the **Override planning calendar** field.
    -   After 2024-07-30, set your old calendar as the value for the **Override planning calendar** field.
    Once the new calendar comes into effect, the child teams will inherit it for all their future iterations. For Agile Teams, the **Override planning calendar** field is read-only and can't be changed independently of its parent ART.


