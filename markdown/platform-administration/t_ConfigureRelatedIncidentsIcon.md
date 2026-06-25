---
title: Configure the related incidents icon
description: You can configure an icon to appear beside a reference field in a form, such as the Caller field, to display related incidents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/t\_ConfigureRelatedIncidentsIcon.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Decorations, Reference field type, Reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure the related incidents icon

You can configure an icon to appear beside a reference field in a form, such as the **Caller** field, to display related incidents.

## Before you begin

Role required: admin

## About this task

The show related incidents icon \(\[Omitted image "icon-workflow.png"\] Alt text: Core UI related incidents icon.\) displays other incidents related to the referenced record.

## Procedure

1.  In the form, right-click the label for the reference field and select **Configure Dictionary**.

2.  Add the **ref\_contributions=user\_show\_incidents** dictionary attribute in the **Attributes** field.

3.  Click **Update**.

    The form reopens and the related incidents icon appears beside the field on the right.


**Related topics**  


[Altering tables and fields using dictionary attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/c_DictionaryAttributes.md)

