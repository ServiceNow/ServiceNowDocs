---
title: Microsoft OneDrive integration with Document Services
description: Use Microsoft OneDrive to copy, delete, restore, and get version actions on documents directly in your ServiceNow instance.
locale: en-US
release: zurich
product: Document Management Services
classification: document-management-services
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integrate with Document Services, Multi Provider Document Services Framework, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Microsoft OneDrive integration with Document Services

Use Microsoft OneDrive to copy, delete, restore, and get version actions on documents directly in your ServiceNow instance.

## Benefits of Microsoft OneDrive integration

Increase collaboration by integrating Microsoft OneDrive with your ServiceNow instance.

With Microsoft OneDrive integration you can do the following:

-   Edit, share, and copy documents from Microsoft OneDrive to your ServiceNow instance.
-   Edit, share, and copy documents from a ServiceNow instance to Microsoft OneDrive.
-   Push a document authored in your ServiceNow instance to Microsoft SharePoint.
-   Attach a shared link to a record.
-   Share links to collaborate and edit documents in real time.
-   Fetch the current version of the document.
-   Collaborate with Microsoft 365 for reviewing, approving, or co-authoring documents.
-   Migrate documents from Microsoft SharePoint to your ServiceNow instance.

## Activation information

To integrate Microsoft OneDrive with Document Services, install the Multi Provider Document Services Framework plugin \(com.snc.multiprovider\_documents\). For more information, see [Activate Multi Provider Document Services Framework](../task/activate-multi-provider-doc-framework.md).

You also need to install the Document Services Framework for Microsoft OneDrive.

-   **[Document Services Framework for Microsoft OneDrive](onedrive-spoke-document-services-framework.md)**  
Integrate the Document Services Framework with Microsoft OneDrive.
-   **[Setup Microsoft OneDrive for Document Services](../task/configure-ms-onedrive-doc-services.md)**  
Integrate the ServiceNow instance and Microsoft OneDrive for Document Services by creating a custom OAuth application in Document Services to authenticate ServiceNow requests.
-   **[Register Microsoft OneDrive as an OAuth provider for Document Services](../task/register-ms-onedrive-oauth-provider.md)**  
Use the information generated during Microsoft OneDrive account configuration to register Microsoft OneDrive as an OAuth provider and allow the instance to request OAuth 2.0 tokens.

**Parent Topic:**[Integrate with Document Services](../reference/integrate-with-document-services-mp.md)

