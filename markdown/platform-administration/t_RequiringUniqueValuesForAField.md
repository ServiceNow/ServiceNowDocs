---
title: Require unique values for a field
description: The system allows you to require that a field's values be unique. When this is done, the system will not let two records have the same value for that field.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Customize, Field administration, Forms, fields, and lists, Configure core features, Administer]
---

# Require unique values for a field

The system allows you to require that a field's values be unique. When this is done, the system will not let two records have the same value for that field.

## Before you begin

Role required: personalize\_dictionary

## About this task

By default, fields are created without this constraint. A field can have unique values only if there aren't already duplicate values in the database for that field. The system doesn't allow you to make a field unique while there are duplicate values in the table.

The system also doesn't allow you to add a unique index if a non-unique index already exists. In this scenario, you can't select the **Unique** check box on the form; instead, the system directs you to the **Tables &amp; Columns** module, so you can drop the non-unique index, and then create the unique index.

## Procedure

1.  Verify that no records in the table for the field have values, or that they all have the same value.

2.  Right-click the field label in the form and select **Configure Dictionary**.

3.  [Configure the form](../../form-administration/concept/configure-form-layout.md#) to add the **Unique** field if it does not already appear.

4.  Select the **Unique** check box.

5.  **Update**.


**Parent Topic:**[Customizing fields on the ServiceNow AI Platform](../concept/customize-fields-now-platform-landing.md)

**Related topics**  


[Configuring the form layout](../../form-administration/concept/configure-form-layout.md#)

