---
title: Configure the document template for the Sign document action type for supplier task
description: Create and configure the document template that enables you to collect e-signatures from multiple participants and generate a filled PDF document.
locale: en-US
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Configure the document template for the Sign document action type for supplier task

Create and configure the document template that enables you to collect e-signatures from multiple participants and generate a filled PDF document.

## Before you begin

Role required: admin

## About this task

Ensure that you've installed the Document Templates \[com.snc.document\_templates\] plugin.

**Important:** When you create the supplier task of action type Sign document for the very first time, the supplier task is created; however, the document task is not created. Therefore, you cannot use the first Sign document task to upload PDF or HTML documents to get signatures. When you create the Sign document task for the first time, a set of restricted caller access \(RCA\) records are created that you must approve. Approving RCAs is a one-time activity. After you approve the RCAs, you can create and use subsequent Sign document supplier tasks except the first Sign document task. For more information about the approving the required RCAs, see [Approve application restricted caller access privileges for Sign document supplier task type](approve-sign-task-rca.md).

**Important:** Starting from the May Store 2024 release, the supplier task of action type Sign document uses the document template \(PDF or HTML\). The E-signature template is used only for KB articles.

## Procedure

1.  Navigate to **All** &gt; **Document Templates** &gt; **All Document Templates**.

2.  Select **New**.

3.  The **What kind of document template would you like to create?** page is displayed.

    The following options are available on this page:

    -   HTML Document Template
    -   PDF Document Template
4.  Do one of the following:

<table id="table_mdx_jmk_51c"><thead><tr><th>

To

</th><th>

Do this

</th></tr></thead><tbody><tr><td>

Configure an HTML document template

</td><td>

To configure an HTML document template:

 1.  Select **HTML Document Template**.
2.  In the **Table** field, select **Supplier Task \[sn\_slm\_task\]**.
3.  On the form, fill in the fields.

For a description of the field values, see [Configure an HTML document template](https://www.servicenow.com/docs/access?context=configure-HTML-doc-template&version=australia&pubname=australia-employee-service-management&ft:locale=en-US).

4.  Select **Submit** or **Save**.
5.  Select the Participants related list to create participants for the PDF document template. For more information, see [Create participants for an HTML document template](https://www.servicenow.com/docs/access?context=create-participants-html&version=australia&pubname=australia-employee-service-management&ft:locale=en-US).
6.  Insert signatures in an HTML document template by selecting participants from the list. For more information, see [Insert signatures](https://www.servicenow.com/docs/access?context=insert-signatures&version=australia&pubname=australia-employee-service-management&ft:locale=en-US).
7.  Select **Publish**.


</td></tr><tr><td>

Configure a PDF document template

</td><td>

To configure a PDF document template:

 1.  Select **PDF Document Template**.
2.  In the **Table** field, select **Supplier Task \[sn\_slm\_task\]**.
3.  On the form, fill in the fields.

For a description of the field values, see [Configure a PDF document template](https://www.servicenow.com/docs/access?context=configure-editable-pdf&version=australia&pubname=australia-employee-service-management&ft:locale=en-US).

4.  Select **Submit** or **Save**.
5.  Select the **Parse PDF** related link to automatically parse information on the PDF and store that information in the PDF Mapping table for reuse.
6.  Select the Participants related list to create participants for the PDF document template. For more information, see [Create participants for a PDF document template](https://www.servicenow.com/docs/access?context=create-participant&version=australia&pubname=australia-employee-service-management&ft:locale=en-US).
7.  Select the Template Mappings related list to define the PDF field mappings. For more information, see [Define a PDF field mapping](https://www.servicenow.com/docs/access?context=edit-pdf-mappings&version=australia&pubname=australia-employee-service-management&ft:locale=en-US).
8.  Select the Mark signatures related list to choose participants and specify the area in the PDF document where you want to collect the signatures of those participants.

**Note:** You can mark signatures only if you have defined participants and mapped users to those participants.

For more information, see [Mark a signature block](https://www.servicenow.com/docs/access?context=mark-signature-doctemp&version=australia&pubname=australia-employee-service-management&ft:locale=en-US).

9.  Select **Publish**.


</td></tr></tbody>
</table>
-   **[Approve application restricted caller access privileges for Sign document supplier task type](approve-sign-task-rca.md)**  
Approve restricted caller access \(RCA\) privileges after you create a supplier task of action type Sign document for the very first time so that you can create and use subsequent Sign document supplier tasks.

**Parent Topic:**[Configure Supplier Lifecycle Operations](../concept/config-supp-mgmt.md)

**Related topics**  


[Install Supplier Case Management](install-supp-mgmt.md)

[Install Supplier Collaboration Portal](install-supp-central.md)

[Install Supplier Operations](install-supplier-ops.md)

[Install Supplier Payment Optimization](install-supp-payment-opt.md)

[Supplier Document Management](../concept/supp-doc-mgmt-overview.md)

[Advanced Work Assignment for Supplier Lifecycle Operations](../concept/supplier-awa.md)

[Enable M2M mapping between supplier contact and suppliers](enable-m2m-supplier-contacts.md)

[Configure Supplier Relationship and Performance Management](../concept/configuring-supplier-performance-mgmt.md)

[Install Universal Request for SLO](install-universal-request.md)

[Configure smart assessments](../concept/configure-smart-assessments.md)

[Approve application restricted caller access privileges for Sign document supplier task type](approve-sign-task-rca.md)

[Supplier Document Management](../concept/supp-doc-mgmt-overview.md)

