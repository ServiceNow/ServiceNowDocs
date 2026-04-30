---
title: Managing employee documents
description: Use Employee Document Management to search, create, move, or manage legal holds on employee documents.Search for and view employee documents using different filters from the employee document repository. You can also download documents for audit purposes.With the employee document writer \[sn\_hr\_ef.document\_writer\] role, you can create or upload an employee document directly to the employee document management repository.You can move employee documents from an HR case to the employee document repository. You can also move employee documents automatically by HR service when an HR case is closed complete.Legal or litigation holds prevent the deletion of documents related to a document type or all employee documents for an HR profile.Add legal hold to multiple HR profiles at one time. Legal or litigation holds prevent the deletion of employee documents for an HR profile.Add legal hold to multiple document types at one time. Legal or litigation holds prevent the deletion of documents related to a document type.You can view a list of all document types or HR profiles that are currently under or had been under a legal hold. You can review the reasons a document type or HR profile was placed on legal hold and remove the legal hold.For optimal system performance and depending on your internal processes, employee documentation is purged based on the security policy established by your company.
locale: en-US
release: xanadu
product: Employee Document Management
classification: employee-document-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 11
breadcrumb: [Using Employee Document Management, Employee Document Management, HR Service Delivery, Employee Service Management]
---

# Managing employee documents

Use Employee Document Management to search, create, move, or manage legal holds on employee documents.

Employee Document Management is your virtual file cabinet containing any or all your organization's employee documents. With Employee Document Management, you can:

-   Search for employee documents: There are many ways you can use to narrow down your search for employee documents.
-   Create employee documents:
    -   Employee documents can be added directly to the document repository.
    -   When combined with HR Service Delivery, HR agents can move documents from an HR case or add directly to the document repository.
-   Place an HR profile or document type on legal hold: Placing an HR profile or document type on legal hold prevents associated employee documents from being purged after the retention period has been reached.
-   Move employee documents: When employee documents are attached to an HR case, you can manually move them to the document repository. Or, you can configure HR services to automatically move employee documents when the case is closed/complete.
-   View employee documents: Employees can view their own employee documents on the service portal or Employee Center. Here [Define policies for a document type](hr-doc-management-config.md#) is how you give them access by document type. The base system provides example document types.

**Parent Topic:**[Using Employee Document Management](using-employee-document-management.md)

**Related topics**  


[Employee document management bulk imports](edm-bulk-uploads.md)

## Searching for employee documents

Search for and view employee documents using different filters from the employee document repository. You can also download documents for audit purposes.

### Before you begin

Role required: sn\_hr\_ef.document\_reader

### About this task

Employee Documents is the repository for employee documents. No matter how large your repository of employee documents is, you can search on the fly or set up pre-set search filters to find the documents you need quickly.

### Procedure

1.  Navigate to **All** &gt; **HR Profile** &gt; **Employee Documents** &gt; **Search Documents**.

2.  Use the column filters to identify documents you are looking for.

    For example, sorting on the Employee column shows all documents by employee.

3.  To download documents, select the check the box next to the documents and then select **Download** from the Actions choice list.

    Downloading multiple documents with the same name appends each document with the employee name. A number is added when documents are still duplicated.

4.  To view more information about a document, click the document name.

    If **Yes** is checked in the**sn\_hr\_ef.enable\_document\_viewer** Employee Document Property, the employee document appears.


## Create or modify an employee document

With the employee document writer \[sn\_hr\_ef.document\_writer\] role, you can create or upload an employee document directly to the employee document management repository.

### Before you begin

Role required: sn\_hr\_ef.document\_writer

### About this task

Documents can also be uploaded from the HR case form and then moved to the document repository.

**Note:** Employee documents can also be moved from the HR case form automatically when the case is closed by configuring the HR service. For information on configuring this feature, see [Configure an HR service](../task/configure-hr-service.md).

### Procedure

1.  Navigate to **All** &gt; **HR Profile** &gt; **Employee Documents** &gt; **Create New Document**.

2.  On the form, fill in the fields.

<table id="table_ydx_mrf_d2b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Document

</td><td>

Employee document to upload.Click **Choose File** to upload an employee document.

**Note:** By default, the maximum size of a document allowed is 30 MB. The default can be changed from the **Maximum file upload size in megabytes** field in Employee Document Properties. For more information, see [Properties for Employee Document Management application](../reference/employee-doc-properties.md).

 After selecting a document, the read-only fields show the file size, file format, created on, and created by.

 The viewer within the UI only supports viewing .pdf documents. Other types of documents can be downloaded and then viewed.

 For optimal search results, do not use dashes \(-\) in the name of the document. Using full words separated by spaces or underbars provides better search results.

 The **Enable "Document Viewer" to preview pdf documents** in the Employee Documents property must be checked **Yes** to view .pdf documents.

**Note:** Viewing documents is not supported for FedRAMP, on-premise customers, mobile devices, customers using edge encryption, or encryption support.

</td></tr><tr><td>

Description

</td><td>

Description of the employee document.

</td></tr><tr><td>

Employee

</td><td>

Name of the employee the document is associated with.

</td></tr><tr><td>

Payroll country

</td><td>

Payroll country of the employee at the time of document creation. **Note:** When you upload the document or move the case attachments to employee file, the value in the **Payroll country** field defaults to the user profile of the employee.

</td></tr><tr><td>

Document type

</td><td>

Document type associated with the employee document.Document types provide categorization and the retention policy.

**Note:**

-   You can read and write a document only if you fulfill the read or write configuration requirement of at least one security policy associated with the document type.
-   You can purge a document only if you fulfill the purge authorization configuration requirement of at least one security policy associated with the document type.
-   You can receive a purge notification only if you fulfill the purge authorization or notification configuration requirement of at least one security policy that is associated with the document type.


</td></tr><tr><td>

Effective date

</td><td>

Date and time from when the employee document is valid. In general, effective date takes the date of document creation, except in cases of contractual agreements. For example, the pay increase or promotion might come into effect from a date different from the date of the performance appraisal.

</td></tr><tr><td>

HR case

</td><td>

HR case number the employee document is associated with when moved from an HR case.

</td></tr><tr><td>

Purge hold

</td><td>

Purge hold status of a document.-   Pending purge authorization: Purge notification has been sent out, but authorization has not been received.
-   Purge Approved: Purge authorization was received, the document is scheduled to be purged.
-   Purged Rejected: Purge authorization was rejected, the document is not scheduled to be purged.

The security policy associated with a document type sets purge authorization. The following roles have permission to change purge authorization:

    -   EF admin \[sn\_hr\_ef.admin\]
    -   Employee File Management Manager \[sn\_hr\_ef.manager\]


</td></tr><tr><td>

Expiration date

</td><td>

Option to set an expiration date for a document. Email notifications will be sent to document owners, managers, or HR representatives \(as per expiration policies\) when the document expires or is nearing its expiration.**Note:** This option is enabled only when an administrator enables the **Expiration date** check box.

</td></tr></tbody>
</table>3.  Click **Submit** to create the employee document record.

    The Employee Document Audit Trail related list tab appears.

    Provides view of all actions for an employee document from creation or uploaded to the time it is purged.

    The following actions are captured:

    -   Record created
    -   Fields updated
    -   Attachment removed
    -   Attachment updated
    -   Attachment renamed
    -   Platform tag added
    -   Platform tag removed
    -   Document viewed
    -   Document downloaded
    -   Document downloaded by employee on Employee Center

## Move employee documents to the document repository

You can move employee documents from an HR case to the employee document repository. You can also move employee documents automatically by HR service when an HR case is closed complete.

### Before you begin

Role required: sn\_hr\_ef.document\_writer or sn\_hr\_core.case\_reader

### About this task

Employee documents can also be added directly to the employee document repository. The employee document repository provides a central repository for quick and easy identification using different sorting features. See [Create or modify an employee document](hr-doc-management-admin.md#).

### Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **All HR Cases**.

2.  Select a case that has employee documents attached.

    From the list view, there is no way to identify HR cases with employee documents attached. The HR case number or the Opened for person are required to locate an HR case.

3.  From the form header, click **Move Attachments**.

    The **Move Attachments to Employee File** menu appears.

4.  Select the check box next to the documents you want to move.

    The **Select COE for attachments to be moved** and **Topic Detail** fields can be modified, but only if the document was added under the wrong type of HR case.

5.  Select the **Document Type** for each document.

    The document type determines categorization, who can access it, and the retention policy. If no document type appears for the associated topic detail, one should be created to ensure correct categorization. See [Define policies for a document type](hr-doc-management-config.md#).

6.  Click **Move Selected**.


### Result

The employee documents move from the HR case to the employee document repository. After an employee document is moved, the file name, format, and size are copied from the attachment to the document.

**Note:** You can also automate this process by checking the **Automatically move attachments** box from HR services. See [Configure an HR service](../task/configure-hr-service.md).

### What to do next

Once you have moved the attachments, the attachments are displayed in the Employee Documents section in the case.

## Add or remove a legal hold for employee documents

Legal or litigation holds prevent the deletion of documents related to a document type or all employee documents for an HR profile.

### Before you begin

Role required: sn\_hr\_ef.admin, sn\_hr\_ef.manager, sn\_hr\_core.profile\_writer, sn\_hr\_ef.legal\_hold\_writer

### About this task

A legal hold suspends all retention policies for associated employee documentation.

**Note:** If you are logged in as System Admin \[admin\], ensure that you are viewing in the Employee Document Management scope. If you change your scope, you also have to refresh the page.

A legal hold prevents the purging of documents only by out-of-box document clean-up mechanism. It is not applicable to custom clean-up mechanisms, such as custom table cleaners or table archival rules.

### Procedure

1.  Navigate to **All** &gt; **HR Profile** &gt; **HR Profiles**.

2.  Select an HR profile you want to place on legal hold.

3.  Click **Add Legal Hold** in the form header.

4.  From **Add legal hold on this profile**, select a reason and add comments.

5.  Click **OK**.

6.  Add comments.

7.  Click **OK**.

8.  To place a document type on legal hold, navigate to **HR Administration** &gt; **Employee Documents** &gt; **Document Types**.

9.  Select a document type.

10. Click **Add Legal Hold**.

    The **Add Legal Hold** button is in the form header.

11. Add comments.

12. Click **Ok**.

13. Click **Update**.

    All documents associated with the document type are placed on legal hold and are not purged based on the retention policy.


## Add legal hold to multiple HR profiles

Add legal hold to multiple HR profiles at one time. Legal or litigation holds prevent the deletion of employee documents for an HR profile.

### Before you begin

Role required: sn\_hr\_ef.admin, sn\_hr\_ef.manager, sn\_hr\_core.profile\_writer, sn\_hr\_ef.legal\_hold\_writer

### Procedure

1.  Navigate to **All** &gt; **HR Profile** &gt; **HR Profiles**.

2.  In the list view, select all the HR profiles on which you intend to apply legal hold.

3.  In **Actions on selected rows**, select **Add Legal Hold**.

4.  In the Add legal hold dialog box:

    1.  In the **Reason** field, select a value.
    2.  In the **Comments** field, add more details.
    3.  Click **OK**.
    Employee documents of selected HR profiles are placed on legal hold and are not purged based on retention policy.


## Add legal hold to multiple document types

Add legal hold to multiple document types at one time. Legal or litigation holds prevent the deletion of documents related to a document type.

### Before you begin

Role required: sn\_hr\_ef.admin, sn\_hr\_ef.manager, sn\_hr\_core.profile\_writer, sn\_hr\_ef.legal\_hold\_writer

### Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **Document Types**.

2.  In the list view, select all documents on which you intend to apply legal hold.

3.  In **Actions on selected rows**, select **Add Legal Hold**.

4.  In the Add legal hold dialog box:

    1.  In the **Reason** field, select a value.
    2.  In the **Comments** field, add more details.
    3.  Click **OK**.
    Documents associated with selected Document Types are placed on legal hold and are not purged based on the retention policy.


## Manage documents on legal hold

You can view a list of all document types or HR profiles that are currently under or had been under a legal hold. You can review the reasons a document type or HR profile was placed on legal hold and remove the legal hold.

### Before you begin

Role required: sn\_hr\_ef.legal\_hold\_writer

### About this task

Legal holds are placed on employee documents by HR profile or by document type. See [Add or remove a legal hold for employee documents](hr-doc-management-admin.md#).

### Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **Employee Documents** &gt; **Legal Holds**.

2.  Select a document type or HR profile.

3.  Change the **Legal hold reason** if applicable.

4.  Enter **Comments**.

5.  Click **Update**.


## View employee document purge logs

For optimal system performance and depending on your internal processes, employee documentation is purged based on the security policy established by your company.

### Before you begin

Role required: sn\_hr\_ef.manager

### About this task

Purging permanently deletes employee documents from the instance. Purging frees up overall storage.

-   The purge log shows what documents were deleted.
-   Attributes of the deleted documents are stored.
-   The default attributes that identify deleted documents are employee and HR case number. You can change the default in the Properties for Employee Document Management.

See [Properties for Employee Document Management application](../reference/employee-doc-properties.md).

### Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **Employee Documents** &gt; **Purge Logs**.

    A list of purged documents with the fields specified in the **These fields will be included in the purge logs if enabled** of Properties for Employee Document Management Application appear.


