---
title: Document Viewer
description: Document Viewer enables you to view documents directly in the ServiceNow AI Platform rather than having to download them.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Forms in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Document Viewer

Document Viewer enables you to view documents directly in the ServiceNow AI Platform rather than having to download them.

Document Viewer supports viewing various file types in the platform including a UTF-8 character encoded PDF file. The maximum document file size is 50 MB. To use Document Viewer, enable it at instance level and for the tables for which you want to use it.

**Note:** Document Viewer also supports FedRAMP instances.

You can view the following file types:

-   MS Word \(.doc\) and \(.docx\)
-   MS PowerPoint \(.ppt\) and \(pptx\)
-   MS Excel \(.xls\) and \(.xlsx\)
-   PDF
-   PNG
-   JPEG

**Note:** The rotate option doesn’t work for images.

Other document types, for example, .zip or .exe files, are automatically downloaded without requiring Document Viewer. Document viewer converts word documents and spreadsheets to pdf first in order to view them. This might take some time to render the file the first time.

![Viewing a PDF file in Document Viewer](../image/DocViewerPDFView.png "PDF view in Document Viewer")

**Note:**

You can only download PDF attachments with in the document.

The following table describes the icons used in Document Viewer.

|Icon|Description|
|----|-----------|
|![Sidebar toggle icon to preview all the pages in the document](../image/IconDocViewerToggleSidebar.png)|Toggle the sidebar to see a preview of all the pages in the document.|
|![Icon to download the attachment](../image/IconDocViewerDownloadAttch.png)|Download the attachment.|
|![Page up or page down icons to scroll the page](../image/IconDocViewerPreviousPg.png)|Page up or down using the arrow buttons. You can also scroll or use your keyboard arrow keys.|
|![Icon to rotate document page](../image/IconDocViewerClockwise.png)|Rotate the page to the right.|
|![Icon to rotate page](../image/IconDocViewerUnClockwise.png)|Rotate the page to the left.|
|![Icons to zoom in or zoom out of the document](../image/IconDocViewerMagnification.png)|Zoom in or out of the document.|
|![Icon to increase the page display to full width](../image/IconDocViewerFitWidth.png)|Increase the page to the full width of Document Viewer.|
|![Search bar with arrows to toggle to the next search result](../image/IconDocViewerSearch.png)|Search for keywords in the document. Use the arrows to toggle to the next search result.|

-   **[Enable Document Viewer](../../../administer/form-administration/task/enable-document-viewer.md)**  
Enable Document Viewer to view documents directly rather than download them to view them in their native applications.
-   **[Document Viewer plugins](doc-viewer-plugins.md)**  
With Document Viewer, you can view documents directly in the ServiceNow Platform rather than having to download them. Two new plugins enhance the experience and provide more options for document viewing. You can collaborate with other people, copy, delete, restore, and view version history directly in a ServiceNow instance.
-   **[View attachments with Document Viewer](../task/view-attachment-doc-viewer.md)**  
View documents within the platform using Document Viewer rather than having to download them to your own file system.
-   **[Disable Document Viewer](../../../administer/form-administration/task/disable-doc-viewer.md)**  
Disable Document Viewer at the instance level to disable it or at table level to disable it for specific tables within the instance.

**Parent Topic:**[Forms in the classic environment](c_UsingForms.md)

**Related topics**  


[View attachments with Document Viewer](../task/view-attachment-doc-viewer.md)

[Enable Document Viewer](../../../administer/form-administration/task/enable-document-viewer.md)

