---
title: Document Approval template
description: Build an application in App Engine Studio \(AES\) using the Document Approval template to manage the approval of documents in your organization.The following tables, experiences, automated workflows, and roles are included in the Document Approval template for App Engine Studio \(AES\).
locale: en-US
release: australia
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Available templates, Use an app template, Create your app, Build, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Document Approval template

Build an application in App Engine Studio \(AES\) using the Document Approval template to manage the approval of documents in your organization.

To use the Document Approval template, install this application from the ServiceNow Store.

![Document Approval template](../image/template-document-approval.png)

A document approval app enables your users to quickly create and use document approval workflows. Document owners and submitters can upload documents needing approvals and check the progress on those approvals. Designated approvers can approve, reject, or return documents with comments.

Admins can use the document approval application to create different workflows for different document types.

This app template is an ideal way to quickly and efficiently make your internal workflows for processing documents. Document owners and submitters can upload a document needing approval to a portal using simple upload functionality that automatically sends submissions through a unique workflow. Once a document has been received, submitters follow the progress of their documents while designated users approve, reject, or return their document for edits. Both submitters and approvers use comments to add notes and feedback to the submission, which is stored in the system for future reference. To give this app even more variety, admins can create unlimited workflows that are customized for each document type and user that allows for multiple stages and approvers depending on what the document category requires.

![Document Approval template](../image/template-doc-approval.png "Document Approval template")

For more information on creating an application using a template, see [Create your app using an application template](../task/use-app-template.md).

**Parent Topic:**[Available templates](template-library.md)

## Document Approval template contents

The following tables, experiences, automated workflows, and roles are included in the Document Approval template for App Engine Studio \(AES\).

### Tables in the Document Approval app template

<table id="table_cfc_ctm_j4b"><thead><tr><th>

Table label \[name\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Document Approver Table\[x\_ &lt;company-code&gt;\_ &lt;document\_approver&gt;\]

</td><td>

Tracks document approvers, their comments, and state of a document.

</td></tr><tr><td>

Document Approval Category Table\[x\_ &lt;company-code&gt;\_ &lt;document\_approval\_category&gt;\]

</td><td>

Tracks the category of document approval requests.

</td></tr><tr><td>

Document Approval Table\[x\_ &lt;company-code&gt;\_ &lt;document\_approval&gt;\]

</td><td>

Tracks the document approval requests.

</td></tr></tbody>
</table>### Experiences in the Document Approval app template

|Experience|Experience type|Description|
|----------|---------------|-----------|
|Document Approval \| Default view|Form|Form for creating a document approval request.|
|Document Approval \| Portal|Form|Simplified form for creating a document approval request.|
|Document Approval Category \| Default view|Form|Form to attach a flow to a document approval record.|
|Document Approval Category \| Workspace|Form|Form to attach a flow to a document approval record.|
|*App name* Workspace|Workspace|Main document approval app workspace, where users can upload documents, check the status of an approval, edit documents, and view their submissions in the workspace. Approvers can view assigned approvals, view previous submissions, and approve or reject submissions.|
|Document Approver \| Workspace|Form|Form for assigning document approvers to records.|
|Document Approval \| Workspace|Form|Form for creating a document approval request.|
|Document Approver \| Default view|Form|Approvers can view assigned approvals and approve or reject submissions.|
|*App name* Portal|Portal|Main portal for people to submit documents for approvals and manage previous submissions.|
|Document Approval Mobile Experience|Mobile experience|Mobile app that employees and managers can use to check the status of an approval, approve or reject documents, and view submissions using your organization's iOS or Android app.|

### Automated workflows in the Document Approval app template

|Workflow name|Workflow type|Description|
|-------------|-------------|-----------|
|Document Approval - Master Flow|Flow - record|Executed when a new document approval record is submitted. It then retrieves the flow to be executed from the document category and executes it.|
|Document Approval Notification|Email|Notifies users of changes to their document approvals.|
|Single Stage Approval|Flow|Allows for the user's manager to be the approver, with basic email notifications being generated on approval, return, or rejection.|

### Roles in the Document Approval app template

<table id="table_htl_zxm_j4b"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Approvers\[x\_&lt;company-name&gt;\_ &lt;document\_approval\_app&gt;.approver\]

</td><td>

Approvers can create, read, delete all documents, and read document approval category data.

</td><td>

Create, Read \(all\), Edit \(all\)

</td></tr><tr><td>

Admins\[x\_&lt;company-name&gt;\_ &lt;document\_approval\_app&gt;.admin\]

</td><td>

Admins can create, read, write, and delete in the Document Approval \[x\_ &lt;company-code&gt;\_ &lt;document\_approval&gt;\] and Document Approval Category \[x\_ &lt;company-code&gt;\_ &lt;document\_approval\_category&gt;\] tables.

</td><td>

Create, Read \(all\), Edit \(all\), Delete \(all\)

</td></tr><tr><td>

Submitters\[x\_&lt;company-name&gt;\_ &lt;document\_approval\_app&gt;.submitter\]

</td><td>

Submitters can create documents, read their own documents, edit their own documents when status is not submitted and delete their own documents. They can also read data from document approval category.

</td><td>

Create, Read \(own\), Edit \(own when status is not submitted\), Delete \(own\)

</td></tr></tbody>
</table>