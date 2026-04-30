---
title: Add field types in Guided Application Creator
description: When you add fields to a custom table in Guided Application Creator, there are only 18 field types available by default. You can add a property to include more field types.
locale: en-US
release: yokohama
product: Guided Application Creator
classification: guided-application-creator
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Guided Application Creator, Building pro-code applications, Developing your application, Building applications]
---

# Add field types in Guided Application Creator

When you add fields to a custom table in Guided Application Creator, there are only 18 field types available by default. You can add a property to include more field types.

## Before you begin

Role required: admin

## About this task

For a list of field types that are available in the ServiceNow AI Platform, see [Field types](https://www.servicenow.com/docs/access?context=r_FieldTypes&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

## Procedure

1.  [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US) with the following settings:

    -   Name: **sn\_g\_app\_creator.field\_types**
    -   Type: string
2.  In the **Value** field, enter a comma-separated list of field type names.

    For example, to add the Image and Document ID field types, enter `user_image,document_id`.

3.  Select **Submit**.


**Parent Topic:**[Guided Application Creator](../concept/guided-app-creator.md)

