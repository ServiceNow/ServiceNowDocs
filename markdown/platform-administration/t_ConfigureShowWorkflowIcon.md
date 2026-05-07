---
title: Configure the show workflow icon
description: You can configure an icon to appear beside a workflow field to display the related workflow in the Workflow Editor.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Decorations, Reference field type, Reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure the show workflow icon

You can configure an icon to appear beside a workflow field to display the related workflow in the Workflow Editor.

## Before you begin

Role required: admin

## About this task

The show workflow icon \(![Core UI show workflow icon](../image/IconRelatedincidentsUI15.png)\) opens the workflow in the Workflow Editor.

## Procedure

1.  In the form, select and hold \(or right-click\) the label for the workflow field and select **Configure** &gt; **Configure Dictionary**.

2.  Add the **ref\_contributions=show\_workflow** dictionary attribute in the **Attributes** field.

3.  Select **Update**.

    The form reopens and the show workflow icon appears beside the field on the right.


**Related topics**  


[Altering tables and fields using dictionary attributes](../../reference-pages/concept/c_DictionaryAttributes.md)

