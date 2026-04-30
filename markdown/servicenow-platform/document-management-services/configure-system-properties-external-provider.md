---
title: Configure system properties to access files and folders from external content providers
description: Configure system properties to enable access to files and folders from external content providers like Microsoft OneDrive V3.1 and Google Drive V3.1 when using the sn-document-explorer-connected component in Document Management with Personal authentication.
locale: en-US
release: zurich
product: Document Management Services
classification: document-management-services
topic_type: task
last_updated: "2025-12-02"
reading_time_minutes: 1
breadcrumb: [Document Management integration with external content providers, Use, Document Management, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure system properties to access files and folders from external content providers

Configure system properties to enable access to files and folders from external content providers like Microsoft OneDrive V3.1 and Google Drive V3.1 when using the **sn-document-explorer-connected** component in Document Management with Personal authentication.

## Before you begin

Role required: mp\_document\_admin

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  Search for and select the system property related to the external provider that you're integrated with.

    -   For Google Drive V3.1:
        -   sn\_docs\_gdrive.google\_drive.base\_alias
        -   sn\_docs\_gdrive.google\_drive.current\_alias
    -   For Microsoft OneDrive V3.1:
        -   sn\_docs\_onedrive.one\_drive.base\_alias
        -   sn\_docs\_onedrive.one\_drive.current\_alias
3.  In the **Value** field of the selected property, enter the base\_alias and current\_alias system IDs from the **sys\_alias** table for the external provider.

    The base\_alias is the system ID of the personal authentication connection alias and the current\_alias is the system authentication connection alias.


**Parent Topic:**[Document Management integration with external content providers](../concept/integration-external-content-providers.md)

