---
title: Find the File location ID for a Cloud file configuration
description: Find the Microsoft SharePoint site ID or drive ID to enter in the File location ID field of a Cloud file configuration record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/governance-risk-compliance/audit-management/get-sharepoint-file-location-id.html
release: australia
product: Audit Management
classification: audit-management
topic_type: task
last_updated: "2026-10-26"
reading_time_minutes: 1
breadcrumb: [Cloud Document Management, Audit Management overview, Audit Management, Governance, Risk, and Compliance]
---

# Find the File location ID for a Cloud file configuration

Find the Microsoft SharePoint site ID or drive ID to enter in the **File location ID** field of a Cloud file configuration record.

## Before you begin

Role required: sn\_grc\_workspace.admin

-   Access to the Microsoft SharePoint site where the files are uploaded.
-   The Microsoft OneDrive connection and credential that the spoke uses must have access to the same site. Otherwise, file uploads fail even if the ID is correct.
-   Permission to use Microsoft Graph Explorer. You might be prompted to consent to permissions such as **Sites.Read.All**. If your organization blocks this, ask your IT administrator to approve it.

## About this task

The **File location ID** identifies where cloud files are uploaded.

## Procedure

1.  Open the Microsoft SharePoint site in a browser and note the hostname and site path from the URL.

    For example, in [https://contoso.sharepoint.com/sites/AuditDocs](https://contoso.sharepoint.com/sites/AuditDocs), the hostname is `contoso.sharepoint.com` and the site path is `sites/AuditDocs`.

2.  Sign in to Microsoft Graph Explorer with your work account.

    Go to [developer.microsoft.com/graph/graph-explorer](https://developer.microsoft.com/graph/graph-explorer).

3.  Run the following request.

    Replace the hostname and site path with your values.

    ```
    GET https://graph.microsoft.com/v1.0/sites/contoso.sharepoint.com:/sites/AuditDocs
    ```

    The response contains an `id` value in the format `hostname,siteCollectionId,siteId`.

4.  Based on the **File location type** that you want to use, get the ID.

    -   **Site**: Copy the entire `id` value from the response, including the commas, with no spaces. For example, `contoso.sharepoint.com,2aa33926-0cf7-4365-970a-e8c50dade57b,6fbf6eac-d87a-474b-86e4-bf450c3c39c5`.
    -   **Drive**: Run `GET https://graph.microsoft.com/v1.0/sites/ <site-id>/drives`, using the site ID from the previous step. In the response, find the entry whose name matches the document library where the files are uploaded, usually Documents, and copy its id value.
5.  Navigate to **All** &gt; **GRC Administration** &gt; **Cloud file configuration** and open the record.

6.  On the **File upload location** tab, select the **File location type** and paste the value in the **File location ID** field.

7.  Select **Update**.


## What to do next

For more information about the fields, see [Cloud file configuration record form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/audit-management/document-access-configuration-record-form.md).

