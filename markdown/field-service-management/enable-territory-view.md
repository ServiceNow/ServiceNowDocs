---
title: Configure territory view to allow users to see other members' schedules
description: Allow users to switch between viewing assignment groups and territories within Workforce.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/enable-territory-view.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Workforce, CSM/FSM Configurable Workspace, Configure, Field Service Management]
---

# Configure territory view to allow users to see other members' schedules

Allow users to switch between viewing assignment groups and territories within Workforce.

## Before you begin

An administrator must [Configure Field Service Territory Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/workforce-optimization-for-field-service/configuring-territory-planning-fsm.md).

Role required: wm\_admin

## About this task

Enable territory view by setting the technician visibility type to allow Workforce users to see other members' schedules in the territory view.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Territory Planning** &gt; **Territory**.

2.  Select the **Technician visibility type** field on the group record where you want to add territory visibility.

    If you don't see the **Type** field, click the gear icon to configure the form and add this field.

3.  Choose the visibility type.

    |To|Do This|
    |---|-------|
    |**Make all members within the territory visible to each other.**|Select **Internal**.|
    |**Make all members in the territory visible to all other territories.**|Select **External**.|

4.  Select **Save**.


**Related topics**  


[Configuring Field Service Territory Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/workforce-optimization-for-field-service/configuring-territory-planning-fsm.md)

[Workforce system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/workforce-system-properties.md)

[Managing agents and tasks from Workforce](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/field-service-manager-workforce/using-manager-workforce.md)

