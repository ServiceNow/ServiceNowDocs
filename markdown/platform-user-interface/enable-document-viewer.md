---
title: Enable Document Viewer
description: Enable Document Viewer to view documents directly rather than download them to view them in their native applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/enable-document-viewer.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Document Viewer, Forms in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Enable Document Viewer

Enable Document Viewer to view documents directly rather than download them to view them in their native applications.

## Before you begin

Role required: admin

## About this task

Document Viewer is enabled by default. Activate it at the instance level. Ensure that the system property **com.snc.documentviewer.enable\_document\_viewer** is set to true or create it if it does not already exist. To deactivate Document Viewer, create the system property **com.snc.documentviewer.enable\_document\_viewer** manually and set it to false.

## Procedure

1.  Activate Document Viewer at the instance level

2.  Navigate to **All** &gt; **System Definition** &gt; **All Available Applications** &gt; **All**.

3.  Enter `ServiceNow Document Viewer` or `com.snc.documentviewer` in the Search field.

4.  Select **Install**.


**Parent Topic:**[Document Viewer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/Documentviewer.md)

**Related topics**  


[Disable Document Viewer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/disable-doc-viewer.md)

