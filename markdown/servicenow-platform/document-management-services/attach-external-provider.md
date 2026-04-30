---
title: Attach a document from an external provider
description: Attach documents from an external cloud like Microsoft OneDrive, Microsoft SharePoint, or Google Drive to Document Management.
locale: en-US
release: xanadu
product: Document Management Services
classification: document-management-services
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Document Management integration with external content providers, Use, Document Management, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Attach a document from an external provider

Attach documents from an external cloud like Microsoft OneDrive, Microsoft SharePoint, or Google Drive to Document Management.

## Before you begin

[Activate Multi Provider Document Services Framework](activate-multi-provider-doc-framework.md)

For Microsoft OneDrive:

-   [Setup Microsoft OneDrive for Document Services](configure-ms-onedrive-doc-services.md)
-   [Register Microsoft OneDrive as an OAuth provider for Document Services](register-ms-onedrive-oauth-provider.md)

For Google Drive, [Set up Document Services framework for Google Drive](setup-gdrive-spoke-document-services.md).

[Configure permission for roles or groups](configure-permissions-mp.md) by selecting the **mp\_document\_admin** from the document list.

Role required: mp\_document\_admin

## Procedure

1.  Navigate to **All** &gt; **Documents** &gt; **Documents**.

2.  Select an existing record or [create a document record](create-new-doc.md).

3.  Select the **Connect With External Provider** check box.

4.  Select **Attach from Provider**.

5.  Select the External Provider.

    -   For Microsoft OneDrive, enter the Folder Path and the File Name.

        To get the Folder Path, go to the file in Microsoft OneDrive and check the folder path.

    -   For Google Drive, enter the File Name and the File URL.

        To get the File Name, go to the file in Google Drive, right click and select **Share** &gt; **Share** &gt; **Copy link**.

6.  If you only want to link the URL, select the **Link Only URL of the external file to the document** check box.

7.  Select **Attach**.

    **Note:** Only the latest version from the provider is attached.

    A new version is created. Select the **Versions** tab to view the versions and the attached document.

8.  Select the **External Provider Settings** tab to view the provider details and the external file URL.

9.  Select **Open Cloud URL** at the top to open the document in the external cloud.


**Parent Topic:**[Document Management integration with external content providers](../concept/integration-external-content-providers.md)

