---
title: Update Hermes messaging settings
description: Review and modify the current the Hermes configuration properties to control Apache Kafka integration, topic management, and other messaging behavior.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/multi-instance-framework-hermes/view-and-modify-a-hermes-property-value.html
release: australia
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: task
last_updated: "2026-05-21"
reading_time_minutes: 1
keywords: [Hermes, Hermes settings, Hermes configuration, background jobs, hermes\_admin, maint, scheduled jobs]
breadcrumb: [Managing Hermes settings, Administer, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Update Hermes messaging settings

Review and modify the current the Hermes configuration properties to control Apache Kafka integration, topic management, and other messaging behavior.

## Before you begin

Role required: maint or hermes\_admin

## Procedure

1.  Navigate to **All** &gt; **Hermes Messaging Service** &gt; **Settings**.

    The Hermes Settings page is displayed.

2.  Locate the category for the property that you plan to modify, such as **Kafka Integration** or **Topic Management**.

    Each category displays a table of properties with property name, value, valid range, and description columns.

3.  Review the current value and valid range for the property.

4.  Change the value by entering a new value in the **Value** field.

    Verify that the value is within the range shown in the **Valid Range** column.

    -   Boolean properties use a list with true or false options.
    -   Topic Inspector format properties use a list with string or binary options.
5.  Select **Save Changes**.

    -   If the value was accepted and applied, the message `Properties saved successfully` is displayed.
    -   If the value exceeds the valid range or is invalid, the message `Some properties could not be saved. Invalid values for the following properties` is displayed. Correct the value and save your changes again.

**Parent Topic:**[Managing Hermes settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/multi-instance-framework-hermes/manage-hermes-settings.md)

