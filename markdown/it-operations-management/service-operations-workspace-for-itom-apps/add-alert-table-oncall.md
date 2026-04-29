---
title: Add alert table to enable on-call scheduling for Service Operations Workspace for ITOM
description: Enable on-call scheduling by incorporating the Alert table \[em\_alert\] into the Trigger Rule Table Config list. This allows for creating shifts and implementing escalation triggers and policies, ensuring teams can promptly respond to alerts and maintain operational continuity.
locale: en-US
release: australia
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Enable on-call scheduling in SOW ITOM]
breadcrumb: [On-call scheduling in SOW for ITOM, Configuring SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Add alert table to enable on-call scheduling for Service Operations Workspace for ITOM

Enable on-call scheduling by incorporating the Alert table \[em\_alert\] into the Trigger Rule Table Config list. This allows for creating shifts and implementing escalation triggers and policies, ensuring teams can promptly respond to alerts and maintain operational continuity.

## Before you begin

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** and in the search field, type `trigger_rule_table_cfg.list`.

    The Trigger Rule Table Configs page opens.

2.  On the form, fill in the fields with the following values.

    ![Trigger rule table config form.](../image/sow-trigger-rule-table-config.png)

    -   In the **Table** field, select **Alert \[em\_alert\]**.
    -   In the **Trigger group** field, select **Assignment group**.
    -   In the **Trigger user** field, select **Assigned to**.
    -   In the **Journal** field, select **Work notes**.
3.  Select **Submit**.


## What to do next

[Create on-call shift for your team](https://www.servicenow.com/docs/access?context=on-call-scheduling-in-sow&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

