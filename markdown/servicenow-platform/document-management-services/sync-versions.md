---
title: Sync versions
description: Sync document versions from an external provider to Document Management and vice versa.
locale: en-US
release: yokohama
product: Document Management Services
classification: document-management-services
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Document Management integration with external content providers, Use, Document Management, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Sync versions

Sync document versions from an external provider to Document Management and vice versa.

## Before you begin

Versions can be synced multiple times but a new version on Document Management can't be uploaded to an external provider.

[Configure permission for roles or groups](configure-permissions-mp.md) by selecting the **mp\_document\_admin** from the document list.

Role required: mp\_document\_admin

## Procedure

1.  Navigate to **All** &gt; **Documents** &gt; **Documents**.

2.  To sync the documents, select the **Versions** tab and select **Sync from Provider**.

3.  Select **Sync now**.

    If the external cloud document has been updated, then a new version will be created under the **Versions** tab.

4.  Select the **External Provider Settings** tab to view the provider details and the external file URL.

5.  Select **Open Cloud URL** at the top to open the document in the external cloud.


**Parent Topic:**[Document Management integration with external content providers](../concept/integration-external-content-providers.md)

