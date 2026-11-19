---
title: Enable electronic signature for approval
description: Enabling electronic signatures for approval. Electronic signatures are helpful if you must obtain a digital signature for compliance or auditing purposes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/document-management-services/t\_EnableElectronicSignature.html
release: zurich
product: Document Management Services
classification: document-management-services
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create a document, Managed Documents, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Enable electronic signature for approval

Enabling electronic signatures for approval. Electronic signatures are helpful if you must obtain a digital signature for compliance or auditing purposes.

## Before you begin

Role required: admin

## About this task

You can activate the [Approval with e-signature plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/approvals/r_InstalledWApprWithEsignature.md) to require that users type in a user name and password when reviewing and approving documents.

The digital signature is not tracked or stored in the document record. Users must simply type in a user name and password after clicking the **Approve** or **Reject** button.

\[Omitted image "MDOCDigitalSignature.png"\] Alt text: Approver Authentication

After activating the Approval with E-Signature plugin, ensure that a row in the e-signature registry table is created for the dms\_document\_revision table.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **e-Signature Registry**.

2.  Check if dms\_document\_revision is already listed and **Enabled** is set to true.

3.  If not listed, click **New**.

4.  In **Table name**, select Document Revision.

5.  Select Enabled.

    \[Omitted image "EsigRegistry.png"\] Alt text: e-Signature Registry

6.  Click **Submit**.


**Parent Topic:**[Create a document](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/document-management-services/c_CreateADocument.md)

