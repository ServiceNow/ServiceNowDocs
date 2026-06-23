---
title: Add field types in Guided Application Creator
description: When you add fields to a custom table in Guided Application Creator, there are only 18 field types available by default. You can add a property to include more field types.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/application-development/guided-application-creator/gac-add-field-types.html
release: xanadu
product: Guided Application Creator
classification: guided-application-creator
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Guided Application Creator, Building pro-code applications, Developing your application, Building applications]
---

# Add field types in Guided Application Creator

When you add fields to a custom table in Guided Application Creator, there are only 18 field types available by default. You can add a property to include more field types.

## Before you begin

Role required: admin

## About this task

For a list of field types that are available in the ServiceNow AI Platform, see [Field types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/platform-administration/r_FieldTypes.md).

## Procedure

1.  [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/platform-administration/r_AvailableSystemProperties.md) with the following settings:

    -   Name: **sn\_g\_app\_creator.field\_types**
    -   Type: string
2.  In the **Value** field, enter a comma-separated list of field type names.

    For example, to add the Image and Document ID field types, enter `user_image,document_id`.

3.  Select **Submit**.


**Parent Topic:**[Guided Application Creator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/guided-application-creator/guided-app-creator.md)

