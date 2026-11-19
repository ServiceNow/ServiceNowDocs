---
title: Include document actions in an activity stream
description: Include document actions in an activity stream to view and track updates to attached documents in a record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/document-management-services/configure-doc-action-activity-stream.html
release: zurich
product: Document Management Services
classification: document-management-services
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Document attachments in an activity stream, Use, Document Management, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Include document actions in an activity stream

Include document actions in an activity stream to view and track updates to attached documents in a record.

## Before you begin

Role required: admin

## About this task

To add and attach documents to a record's activity stream, you would need to complete the following tasks:

-   [Enable Document actions in activity stream](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/document-management-services/configure-doc-action-activity-stream.md)
-   [Enable Documents in the record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/document-management-services/enable-doc-related-list.md)
-   [Add documents to the record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/document-management-services/create-new-doc-parent.md)

## Procedure

1.  Enter `sys_properties.list` in the navigation filter.

2.  Select the **glide.documents.journal.enabled** property.

3.  On the form, set the **Value** field to **true**.

4.  Select **Update**.

5.  Select the **glide.documents.attach.fields**.

6.  On the form, in the **Value** field, add the field name that you want the record to reflect.

    For example, you would enter work\_notes for the **Work notes** field.

    Use a comma to add multiple field names.

    **Note:** Document updates are pushed only if the field names exist.

7.  Select **Update**.


**Parent Topic:**[Document attachments in an activity stream](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/document-management-services/activity-stream-for-documents.md)

