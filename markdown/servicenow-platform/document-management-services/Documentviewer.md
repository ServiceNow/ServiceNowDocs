---
title: Document Viewer
description: Document Viewer enables you to view documents directly in the ServiceNow AI Platform rather than having to download them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/document-management-services/Documentviewer.html
release: australia
product: Document Management Services
classification: document-management-services
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Document Viewer

Document Viewer enables you to view documents directly in the ServiceNow AI Platform rather than having to download them.

Document Viewer is available in the Classic UI, Service Portals and Workspace.

Document Viewer supports viewing various file types in the platform including a UTF-8 character encoded PDF files up to 50 MB. To use Document Viewer, enable it at instance level.

**Note:** Document Viewer also supports FedRAMP instances.

**Supported file types**

-   MS Word \(.doc\) and \(.docx\)
-   MS PowerPoint \(.ppt\) and \(pptx\)
-   MS Excel \(.xls\) and \(.xlsx\)
-   PDF
-   txt
-   PNG
-   JPEG

Other file types, such as .ZIP or .exe files, are automatically downloaded without opening in Document Viewer. Word documents and spreadsheets are converted to PDF before viewing, which may take a moment to render on first load.

## Document Viewer features

The following features are available in Document Viewer across Workspace, Classic UI, and Service Portals:

-   Document summary in text and voice
-   Voice and text based Q&amp;A
-   FAQ
-   Smart redaction
-   Manual redaction

## Revert to the classic document viewer

By default, viewing an attachment opens the Next Experience Document Viewer. To revert to the classic document viewer, a user with the document\_admin role can set the system property value to classic.

The **com.snc.documentviewer.default** system property determines which document viewer opens when a user selects **View** on an attachment in the Classic UI. By default, the property is set to **next\_experience**, which opens the Next Experience Document Viewer and makes ServiceNow Otto features such as document summary, voice Q&amp;A, smart redaction, and manual redaction available in the Classic UI and Service Portals.

To revert to the classic document viewer:

1.  Navigating to **System Properties** and search for **com.snc.documentviewer.default**.
2.  Set the value to `classic`.

**Related topics**  


[View attachments with Document Viewer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/document-management-services/view-attachment-doc-viewer.md)

[Enable Document Viewer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/document-management-services/enable-document-viewer.md)

