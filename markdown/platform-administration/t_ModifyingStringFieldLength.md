---
title: Modify string field length
description: You can modify the maximum character limit for a string field.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Customize, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Modify string field length

You can modify the maximum character limit for a string field.

## Before you begin

Role required: personalize\_dictionary

## About this task

The URL type field hides the Max Length field on the Dictionary form by default. Browsers support URL length up to 2,083 characters. The URL field is a String field.

## Procedure

1.  Navigate to a form that contains the field that you want to modify.

2.  Right-click the field label in the form and select **Configure Dictionary**.

3.  Change the **Max length** field to the desired length.

    **Note:** You can change between string-based data types as long as length changes do not cause any data loss from truncation. For example, you can change from a MEDIUM database type to a VARCHAR\(100\) database type if none of the existing data is greater than 100.

4.  Click **Update**.

    The system cancels any length change that results in data loss due to truncation.


**Parent Topic:**[Customizing fields on the ServiceNow AI Platform](../../field-administration/concept/customize-fields-now-platform-landing.md)

**Related topics**  


[Field types reference](../reference/r_FieldTypes.md)

