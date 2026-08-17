---
title: Document Viewer
description: Document Viewer enables you to view documents directly in the ServiceNow AI Platform rather than having to download them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/Documentviewer.html
release: australia
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Forms in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
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

-   **[Enable Document Viewer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/enable-document-viewer.md)**  
Enable Document Viewer to view documents directly rather than download them to view them in their native applications.
-   **[Document Viewer plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/doc-viewer-plugins.md)**  
With Document Viewer, you can view documents directly in the ServiceNow Platform rather than having to download them. Two new plugins enhance the experience and provide more options for document viewing. You can collaborate with other people, copy, delete, restore, and view version history directly in a ServiceNow instance.
-   **[View attachments with Document Viewer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/view-attachment-doc-viewer.md)**  
View documents within the platform using Document Viewer rather than having to download them to your own file system.
-   **[Disable Document Viewer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/disable-doc-viewer.md)**  
Disable Document Viewer at the instance level to disable it or at table level to disable it for specific tables within the instance.

**Parent Topic:**[Forms in the classic environment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_UsingForms.md)

**Related topics**  


[View attachments with Document Viewer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/view-attachment-doc-viewer.md)

[Enable Document Viewer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/enable-document-viewer.md)

