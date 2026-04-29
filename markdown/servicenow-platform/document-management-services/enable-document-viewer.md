---
title: Enable Document Viewer
description: Enable Document Viewer to view documents directly rather than download them to view them in their native applications.
locale: en-US
release: australia
product: Document Management Services
classification: document-management-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Document Viewer, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Enable Document Viewer

Enable Document Viewer to view documents directly rather than download them to view them in their native applications.

## Before you begin

Role required: admin

## About this task

Document Viewer is enabled by default. Activate it at the instance level and then enable it at the table level for the tables where you want to use it. Ensure that the system property **com.snc.documentviewer.enable\_document\_viewer** is set to true or create it if it does not already exist. To de-activate Document Viewer, create the system property **com.snc.documentviewer.enable\_document\_viewer** manually and set it to false.

## Procedure

1.  Activate Document Viewer at the instance level

    1.  Navigate to **All** &gt; **System Definition** &gt; **All Available Applications** &gt; **All**.

    2.  Enter `ServiceNow Document Viewer` or `com.snc.documentviewer` in the Search field.

    3.  Select **Install**.

2.  Activate Document Viewer for the tables where you want to use it.

    1.  Navigate to **System Definition** &gt; **Dictionary**.

    2.  Search for the table, open the record with the type field **Collection**.

    3.  Enter `Use Document Viewer` in the **Attribute** field.

    4.  Enter `true` in the **Value** field.

    Document Viewer is enabled at the table level. Repeat this procedure for each table for which you want to enable Document Viewer.


**Related topics**  


[Disable Document Viewer](disable-doc-viewer.md)

