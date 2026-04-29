---
title: Upgrade SLA to 2011 engine
description: You can upgrade SLA processing to use the 2011 Engine.
locale: en-US
release: australia
product: Service Level Management
classification: service-level-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Level Agreement \(Legacy\) engines, Service Level Management reference, Service Level Management, IT Service Management]
---

# Upgrade SLA to 2011 engine

You can upgrade SLA processing to use the 2011 Engine.

## Before you begin

Role required: admin

## About this task

The service level management plugin was enhanced with the ability to script the condition rules for SLA transitions, giving control over how the conditions in an SLA Definition are used. Please review the documentation before enabling the enhancements to understand how the new engine will impact existing customizations

**Note:** Activating the 2011 SLA engine will deactivate all business rules on the `task_sla` table \(except for the rule **Task SLA Empty Schedule Warning**, which is part of the 2011 engine\). If you have added any additional business rules or customized the default business rules, these will not be automatically deactivated. So you should review these customizations, and manually deactivate such business rules, before making this change.

The default Process SLAs rule on the `task` table will also be deactivated, so any customizations to this script must be incorporated into the new SLA engine.

In addition, breach information is removed from the **Stage** field, and stored in the new **Has breached** field.

To enable the new functionality:

## Procedure

1.  Navigate to **All** &gt; **Service Level Management** &gt; **SLA Properties**.

2.  Change the following property from 2010 to 2011:

    ![Changing the property from 2010 to 2011](../image/SLAConditionEnable.png)

    By default, the 2011 Engine sets the **Stage** field to **In Progress**, shaded red to indicate the breached status, and sets the **Has Breached** field to true. The SLA continues to run until the stop conditions are met.


**Parent Topic:**[Service Level Agreement \(Legacy\) engines](../concept/c_GetStartedWithSLAs.md)

