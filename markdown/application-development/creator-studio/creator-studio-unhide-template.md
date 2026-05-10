---
title: Show the AES template
description: You can make the App Engine Studio \(AES\) template, which is hidden by default, appear for users when they create an app in Creator Studio.
locale: en-US
release: australia
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Templates and forms, Administer, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Show the AES template

You can make the App Engine Studio \(AES\) template, which is hidden by default, appear for users when they create an app in Creator Studio.

## Before you begin

Role required: admin

## Procedure

1.  Open the **All** menu.

2.  Type `sys_properties.list` and press Enter.

3.  Enter **com.glide.creator\_studio.template\_deny\_list** in the **Name** column, and then press Enter.

4.  Clear the entry from the **Value** field.

    If you want to hide any other templates, enter their system values \(sys\_id for each template\) in the **Value** field, separated by commas. For more information on the sys\_id, see [Unique record identifier \(sys\_id\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_UniqueRecordIdentifier.md).


**Parent Topic:**[Administering templates and forms for Creator Studio](../concept/creator-studio-administering-forms.md)

