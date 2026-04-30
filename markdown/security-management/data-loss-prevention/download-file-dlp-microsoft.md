---
title: Download files for DLP incidents of type Exchange Online, OneDrive, and SharePoint
description: Download files or email that violates the DLP policy on Microsoft Purview. Download this file or email on to your local machine from the DLP IR Incident view. You can download the files for DLP IR incidents of type Scan source Exchange Online, OneDrive, and SharePoint.
locale: en-US
release: xanadu
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Data Loss Prevention Incident Response with Microsoft, DLP integrations, Data Loss Prevention Incident Response, Security Operations]
---

# Download files for DLP incidents of type Exchange Online, OneDrive, and SharePoint

Download files or email that violates the DLP policy on Microsoft Purview. Download this file or email on to your local machine from the DLP IR Incident view. You can download the files for DLP IR incidents of type Scan source Exchange Online, OneDrive, and SharePoint.

## Before you begin

Role required:

-   sn\_dlir.admin, sn\_dlir.analyst
-   Any valid approver

## Procedure

1.  Navigate to **All** &gt; **DLP Incident Management** &gt; **DLP Analyst Workspace**.

2.  Open a DLP incident record of type Scan source Exchange Online or OneDrive or SharePoint which is ingested from Microsoft source.

3.  Click **Download File**.

    The file or email that violated the DLP policy on the Microsoft Purview side will be downloaded to the user’s local machine.

    **Note:** DLP admin can control the access of **Download File** action by disabling the **Should downloading the violating file of the reported incident be allowed** setting from the Advanced Settings page. For more information, see [Configure advanced settings](../../data-loss-prevention/task/configure-advanced-settings-dlp.md).


-   **[Download files approval flow](download-approval-flow.md)**  
The below approval flow describes the procedure for the approvers to view the Download File action.

**Parent Topic:**[Data Loss Prevention Incident Response with Microsoft](../concept/dlp-integration-microsoft.md)

