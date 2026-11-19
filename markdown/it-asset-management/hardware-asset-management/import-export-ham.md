---
title: Import and export content data
description: Import content data from or export content data to the Hardware Asset Management content library service to support hardware normalization of asset models. On-premise users can import or export data via a zip file using the Manage Hardware Library module.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/hardware-asset-management/import-export-ham.html
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [import hardware asset management content library, export hardware normalization data, Manage Hardware Library module]
breadcrumb: [Work with hardware normalization, Use, Hardware Asset Management, IT Asset Management, Asset Management]
---

# Import and export content data

Import content data from or export content data to the Hardware Asset Management content library service to support hardware normalization of asset models. On-premise users can import or export data via a zip file using the Manage Hardware Library module.

## Before you begin

Get the content ZIP files from ServiceNow before you import:

-   If your instance can connect to the Content Service, use automatic delivery.
-   If your instance can't connect, open a Now Support service request titled “Request HTTPS Access for On-Prem \(HAM or SAM\) Content Library”. Enter your instance name in the request. ServiceNow emails you HTTPS credentials and folder paths.

Download all ZIP files from the folders. Don't merge them. Import each file separately, in the order described in the procedure.

Role required:

-   ham\_admin
-   domain\_admin \(if domain separation is enabled\)

## Procedure

1.  Navigate to **Modules** and search for **Manage Hardware Library**.

2.  Open the Manage Hardware library form layout and select the **Active** check box to activate the module.

3.  Select **Save** and refresh the form layout.

4.  Navigate to the **Manage Hardware Library** module.

5.  Import the content data to get the new data into your system.

    1.  Select **Import Hardware Library Content**.

    2.  Select **Attach Content File** and then select one ZIP file that contains the content.

        Each import accepts one ZIP file. If you attach more than one, an error appears.

        ServiceNow provides the content as several ZIP files. Don't merge them. Import the files one at a time:

        1.  Attach one ZIP file, and select **Run Import**.
        2.  Wait for the import to finish.
        3.  Repeat for the next ZIP file.
        **Important:** Import incremental files in date order. Don't skip any.

    3.  Select **Run Import**.

        After the data is imported, the content update schedule job, **HAM - Apply latest content changes**, is triggered to process the content updates.

        If the import does not start, an error appears. Common error types:

        -   No file attached: Attach the content ZIP file first, then select **Run Import**.
        -   Invalid file: The attachment is not a ZIP file. Before Hardware Asset Management version 16.0.0, a valid ZIP file labeled application/x-zip-compressed is also rejected.
        -   Multiple files attached: Remove the extra attachments so that only one ZIP file remains.
        -   Operation already running: Wait for the import or export to finish, then try again.
6.  Export content to send the custom data or any hardware models that aren't fully normalized to the ServiceNow content service team.

    1.  Select **Content Service Opt-in: Export Hardware Normalization Content**.

    2.  If you already haven't opted in to share the data with ServiceNow content service, select **opt-in** and refresh the Manage Hardware Library page.

    3.  Select **Run Export**.

    4.  After the status changes to Ready for Download, refresh the page.

        A zip file is created and appears at the top of the Manage Hardware Library page. If there is no content to export, an error message appears informing you that no content exists.

    5.  Download and send this zip file to the ServiceNow content service team.


## What to do next

After the import finishes, check the result:

1.  Open the Import files related list. Each file shows its status. For failed files, **Details** gives the reason.
2.  Open the Asset Job Log entry **HAMP - Content File Manager - Import status** and check the counts. The record can show successfully imported even when some files failed.
3.  If the import failed, fix the issue, attach the file again, and select **Run Import**.

**Parent Topic:**[Work with hardware normalization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/hardware-asset-management/Work-with-hardware-normalization.md)

**Related topics**  


[IT Asset Management content request process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/asset-management/content-request-itam.md)

[Create IT Asset Management content request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/asset-management/create-itam-content-request.md)

