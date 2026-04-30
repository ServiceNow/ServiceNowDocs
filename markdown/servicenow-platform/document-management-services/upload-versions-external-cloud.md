---
title: Upload versions to an external cloud
description: Upload document versions Document Management to an external cloud.
locale: en-US
release: zurich
product: Document Management Services
classification: document-management-services
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Document Management integration with external content providers, Use, Document Management, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Upload versions to an external cloud

Upload document versions Document Management to an external cloud.

## Before you begin

[Configure permission for roles or groups](configure-permissions-mp.md) by selecting the **mp\_document\_admin** from the document list.

Role required: mp\_document\_admin

## Procedure

1.  Navigate to **All** &gt; **Documents** &gt; **Documents**.

2.  To upload documents on an external cloud, select the **Versions** tab and select **Upload to cloud**.

3.  Select the default version if available or attach a local file.

4.  -   Select **Remove from instance** check box to remove the attached version from the database

    **Note:** The removed attachment version will still appear for tracking.

-   Select **Do not store instance** check box not to store the attachment in the database.

    **Note:** The attachment won’t be stored in the database, but a new version is created for tracking.

5.  Select **Upload** to proceed.

6.  Select the **External Cloud Settings** tab to view the provider details and the external file URL.

7.  Select **Open Cloud URL** at the top to open the document in the external cloud.


**Parent Topic:**[Document Management integration with external content providers](../concept/integration-external-content-providers.md)

