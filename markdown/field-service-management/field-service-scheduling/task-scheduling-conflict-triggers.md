---
title: Configure task scheduling conflict triggers
description: Configure which work order task \(WOT\) fields are monitored for scheduling conflicts during a scheduling run.
locale: en-US
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2026-04-03"
reading_time_minutes: 1
breadcrumb: [Task scheduling conflicts, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Configure task scheduling conflict triggers

Configure which work order task \(WOT\) fields are monitored for scheduling conflicts during a scheduling run.

## Before you begin

Role required: wm\_admin

## About this task

Updating a WOT record during a scheduling run creates a scheduling conflict. A field set in the **Application Common Configuration** application controls which WOT fields are considered in conflict tracking. Use this procedure to enable or disable fields to consider for conflict during scheduling.

## Procedure

1.  Navigate to **All****.**

2.  In the navigation filter, type **app\_cmn\_field\_set\_list.do** and press **Enter**.

3.  Search for and open **Work Order Task Scheduling Conflict Triggers**.

4.  In the **Application Field Set Items** related list, locate the field you want to configure.

    If a **Security prevents writing to this field** message appears, select the red **X** to dismiss it. A banner at the top of the screen then indicates that the record is in the Application Common Configuration application while Global is the current application. Select **here** in the banner to edit the record.

5.  In the **Always Show** field, double-click \(or use the keyboard shortcut\) the current value, select **true** to include the field in conflict tracking or **false** to exclude it, then select the check mark to confirm.

6.  Select **Update**.


