---
title: Create or upload employee documents using Agent Workspace for HR Case Management
description: Create or upload employee documents to an HR case using the Agent Workspace for HR Case Management.
locale: en-US
release: australia
product: Agent Workspace for HR Case Management
classification: agent-workspace-for-hr-case-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Employee Document Management for Agent Workspace for HR Case Management, Using Agent Workspace for HR Case Management, Agent Workspace, HR Service Delivery, Employee Service Management]
---

# Create or upload employee documents using Agent Workspace for HR Case Management

Create or upload employee documents to an HR case using the Agent Workspace for HR Case Management.

## Before you begin

Role required: sn\_hr\_ef.document\_writer

## Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **Agent Workspace for HR Case Management**.

2.  Click the **Lists** icon \(![HR Workspace Lists icon](../image/agent-ws-hr-list-icon.png)\).

3.  Click **Employee documents**.

4.  Click **All**.

5.  Click **New**.

    Alternatively, you can also create an employee document from **HR Profiles**. Select a HR Profile and from the more actions menu, click **New document**.

6.  On the form, fill in the fields.

<table id="table_ydx_mrf_d2b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Employee Document

</td><td>

Employee document to upload.Click **Browse** to upload an employee document.

 By default, the maximum size of a document allowed is 30 MB. The default can be changed from the**Maximum file upload size in megabytes** field in Employee Document Properties. For more information, see [Properties for Employee Document Management application](../reference/employee-doc-properties.md).

 After selecting a document, the read-only fields show the file size, file format, created on, and created by.

 The viewer within the UI only supports viewing .pdf documents. Other types of documents can be downloaded and then viewed.

 For optimal search results, do not use dashes \(-\) in the name of the document. Using full words separated by spaces or underbars provides better search results.

 Check **Yes** in the **Enable Document Viewer to preview pdf documents** in the Employee Documents property to view .pdf documents.

**Note:** FedRAMP, on-premise customers, mobile devices, customers using edge encryption, or encryption support does not support viewing documents.

</td></tr><tr><td>

Description

</td><td>

Description of the employee document.

</td></tr><tr><td>

Employee

</td><td>

Name of the employee the document is associated with.

</td></tr><tr><td>

Document type

</td><td>

Document type associated with the employee document.Document types provide categorization, security, and retention policies.

</td></tr><tr><td>

HR case

</td><td>

HR case number the employee document is associated with when moved from an HR case.

</td></tr><tr><td>

Purge hold

</td><td>

Purge hold status of a document.-   Pending purge authorization: Awaiting authorization for document purging.
-   Purge Approved: Document has authorization to schedule purging.
-   Purged Rejected: Document did not receive purge authorization.

**Important:** Document type's security policy determines purge authorization. The following roles have permission to change purge authorization:

    -   EF admin \[sn\_hr\_ef.admin\]
    -   Employee File Management Manager \[sn\_hr\_ef.manager\]


</td></tr></tbody>
</table>7.  Click **Save** to create the employee document record.

    The **Audit Trail** tab appears.

    Provides view of all actions for an employee document from creation or uploaded to the time it is purged.


