---
title: Employee Document Management for HR Service Delivery Agent Workspace
description: Employee Document Management provides storage space, a filing system, the ability to easily retrieve documents, defining who can view sensitive documents, and when to purge documents.Create or upload employee documents to an HR case using the HR Service Delivery Agent Workspace.Move employee documents from a case in HR Service Delivery Agent Workspace to employee document repository. The employee document repository provides a central repository for quick and easy identification of documents using different sorting features.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Using the HR Service Delivery Agent Workspace, HR Service Delivery Agent Workspace \(Classic\), HR Service Delivery, Employee Service Management]
---

# Employee Document Management for HR Service Delivery Agent Workspace

Employee Document Management provides storage space, a filing system, the ability to easily retrieve documents, defining who can view sensitive documents, and when to purge documents.

For more information about Employee Document Management, see [Employee Document Management](hr-employee-doc-management.md).

## Create or upload employee documents using HR Service Delivery Agent Workspace

Create or upload employee documents to an HR case using the HR Service Delivery Agent Workspace.

### Before you begin

Role required: sn\_hr\_ef.document\_writer

### Procedure

1.  Navigate to **HR Agent Workspace** &gt; **Lists** &gt; **Employee Documents** &gt; **All**.

    Alternatively, you can also create an employee document from **HR Agent Workspace** &gt; **Lists** &gt; **HR Profiles**.

2.  Click **New**.

3.  On the form, fill in the fields.

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
</table>4.  Click **Save** to create the employee document record.

    The **Audit Trail** tab appears.

    Provides view of all actions for an employee document from creation or uploaded to the time it is purged.


## Move employee documents using HR Service Delivery Agent Workspace

Move employee documents from a case in HR Service Delivery Agent Workspace to employee document repository. The employee document repository provides a central repository for quick and easy identification of documents using different sorting features.

### Before you begin

Role required: sn\_hr\_ef.document\_writer, sn\_hr\_core.case\_writer

### Procedure

1.  Navigate to **HR Agent Workspace** &gt; **Lists** &gt; **All HR Cases** &gt; **All**.

2.  Select a case that has employee documents attached.

    **Note:** From the list view, there is no way to identify HR cases with employee documents attached. To locate an HR case, you need the HR case number or the Opened for person.

3.  Click **Move Attachments**.

    ![Move employee documents from agent workspace to employee document management](../task/move-docs-workspace1.png)

4.  In the Move Attachments to Employee documents window:

    1.  Select the check box next to the documents you want to move.
    2.  Select the **Document Type** for each document. The document type determines categorization, who can access it, and the retention policy. Create a document type if none appears for the associated topic detail. Creating a document type ensures correct categorization.
    3.  Click **Move Selected**.
    **Note:** The **Target COE** and **Topic Detail** fields can be modified only if the document has been added under the wrong type of HR case.

    ![Move employee documents from agent workspace to employee document management](../task/move-docs-workspace2.png)


### Result

-   The employee documents move from the HR case to the employee document repository.
-   To view a list of all employee documents in the list column, select **Employee Documents**. ![List of employee documents](../task/move-docs-workspace3.png)
-   The moved attachments appears in the contextual side panel under the ![Employee documents icon](../image/employee-documents.png) employee documents icon within the case.

    ![Moved attachments appearing in the contextual side panel](../task/move-docs-workspace4.png)


