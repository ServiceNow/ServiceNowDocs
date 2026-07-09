---
title: Configure the show workflow icon
description: You can configure an icon to appear beside a workflow field to display the related workflow in the Workflow Editor.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/platform-administration/t\_ConfigureShowWorkflowIcon.html
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Decorations, Reference field type, Field types reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure the show workflow icon

You can configure an icon to appear beside a workflow field to display the related workflow in the Workflow Editor.

## Before you begin

Role required: admin

## About this task

The show workflow icon \(\[Omitted image "IconRelatedincidentsUI15.png"\] Alt text: Core UI show workflow icon\) opens the workflow in the Workflow Editor.

## Procedure

1.  In the form, right-click the label for the workflow field and select **Configure** &gt; **Configure Dictionary**.

2.  Add the **ref\_contributions=show\_workflow** dictionary attribute in the **Attributes** field.

3.  Click **Update**.

    The form reopens and the show workflow icon appears beside the field on the right.


**Related topics**  


[Altering tables and fields using dictionary attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/table-administration-and-data-management/c_DictionaryAttributes.md)

