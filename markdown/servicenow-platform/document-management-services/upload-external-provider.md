---
title: Upload to an external provider
description: Upload documents from Document Management to external cloud like Microsoft OneDrive, Microsoft SharePoint, or Google Drive.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/servicenow-platform/document-management-services/upload-external-provider.html
release: xanadu
product: Document Management Services
classification: document-management-services
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Document Management integration with external content providers, Use, Document Management, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Upload to an external provider

Upload documents from Document Management to external cloud like Microsoft OneDrive, Microsoft SharePoint, or Google Drive.

## Before you begin

[Activate Multi Provider Document Services Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/document-management-services/activate-multi-provider-doc-framework.md)

For Microsoft OneDrive:

-   [Setup Microsoft OneDrive for Document Services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/document-management-services/configure-ms-onedrive-doc-services.md)
-   [Register Microsoft OneDrive as an OAuth provider for Document Services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/document-management-services/register-ms-onedrive-oauth-provider.md)

For Google Drive, [Set up Document Services framework for Google Drive](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/document-management-services/setup-gdrive-spoke-document-services.md).

[Configure permission for roles or groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/document-management-services/configure-permissions-mp.md) by selecting the **mp\_document\_admin** from the document list.

Role required: mp\_document\_admin

## Procedure

1.  Navigate to **All** &gt; **Documents** &gt; **Documents**.

2.  Select an existing record or [create a document record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/document-management-services/create-new-doc.md).

3.  For a newly created record, [create a document version](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/document-management-services/create-doc-version.md).

4.  Select the **Connect With External Provider** check box.

5.  Select **Upload to Provider**.

6.  Select the external provider and enter the folder path.

7.  Select **Upload**.

    **Note:** Only the latest version is uploaded.

8.  Select the **External Provider Settings** tab to view the provider details and the external file URL.

9.  Select **Open Cloud URL** at the top to open the document in the external cloud.


**Parent Topic:**[Document Management integration with external content providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/document-management-services/integration-external-content-providers.md)

