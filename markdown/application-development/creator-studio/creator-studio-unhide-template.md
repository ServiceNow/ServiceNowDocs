---
title: Show the AES template
description: You can make the App Engine Studio \(AES\) template, which is hidden by default, appear for users when they create an app in Creator Studio.
locale: en-US
release: yokohama
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Administering templates and forms for Creator Studio, Administering Creator Studio, Creator Studio, Building no-code applications, Developing your application, Building applications]
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

    If you want to hide any other templates, enter their system values \(sys\_id for each template\) in the **Value** field, separated by commas. For more information on the sys\_id, see [Unique record identifier \(sys\_id\)](https://www.servicenow.com/docs/access?context=c_UniqueRecordIdentifier&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).


**Parent Topic:**[Administering templates and forms for Creator Studio](../concept/creator-studio-administering-forms.md)

