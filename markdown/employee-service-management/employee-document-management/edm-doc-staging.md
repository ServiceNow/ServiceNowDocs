---
title: Correcting employee documents in the staging table
description: Use the Employee Document Staging form to correct staging records prior to importing to HR Service Delivery. Staging records are created after you have mapped your source employee documents and the Start staging job has run.
locale: en-US
release: zurich
product: Employee Document Management
classification: employee-document-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Bulk imports, Use, Employee Document Management, HR Documents, HR Service Delivery, Employee Service Management]
---

# Correcting employee documents in the staging table

Use the Employee Document Staging form to correct staging records prior to importing to HR Service Delivery. Staging records are created after you have mapped your source employee documents and the Start staging job has run.

## Before you begin

Role required: sn\_hr\_ef.admin, sn\_hr\_ef.document\_import

## Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **Bulk Import** &gt; **Document Staging**.

    Or, from the Employee Document Import Configuration form, click the **Start staging job** related link.

    After the Employee Document Staging job runs successfully, you can review and correct any errors.

2.  Click an employee name.

3.  Click the **Validate** button.

    The Verify Fields pop-up appears.

4.  Edit incorrect information.

5.  Click **Complete**.

6.  Click **Ready for Import**.

    You can also correct fields from the **Employee Document Staging** form.

<table id="table_vjh_tzw_qfb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Employee

</td><td>

Employee associated with the staged employee document.

</td></tr><tr><td>

Document Type

</td><td>

The document type you want associated with the employee document.Document types categorize your employee documents and determine access and retention.

 See [Define policies for a document type](../concept/hr-doc-management-config.md#).

</td></tr><tr><td>

File name

</td><td>

File name of the employee document.

</td></tr><tr><td>

State

</td><td>

The state of the employee document.-   Ready: Document is ready to be captured and moved to Employee Document Management.
-   Draft: Document ignored when the Capture job is run and not moved to Employee Document Management.


</td></tr></tbody>
</table>7.  Click the **Attachment Content** tab.

<table id="table_alk_zzw_qfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Content source

</td><td>

The type of source document repository your employee documents are being pulled from.-   URL: The source employee document repository is cloud-based.
-   Local: The source employee document repository is local.


</td></tr><tr><td>

Content

</td><td>

The path in the source repository that the staged document resides.

</td></tr></tbody>
</table>8.  Click the Additional Information tab.

<table id="table_evg_c1x_qfb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Job

</td><td>

The name of the Employee Document Staging job. The job takes the document bulk import configuration name.

</td></tr><tr><td>

Configuration

</td><td>

The name of that identifies your employee document bulk import configuration. See [Configuring employee document management bulk import with source document repository](edm-bulk-configuration.md#).

</td></tr><tr><td>

Description

</td><td>

Currently not used.

</td></tr><tr><td>

Domain

</td><td>

Automatically populated via domain separation and identifies the specific domain you are configuring employee documentation bulk uploads for.For more information on domain separation, see [Domain Separation and HR Service Delivery](../concept/hr-domain-separation.md).

</td></tr></tbody>
</table>9.  Click **Validate** to ensure that the employee and document type are correct.

    You can change this information from the pop-up.

10. After making changes, click **Update**.

    The Employee Document Import Configuration form returns. You can continue reviewing and correcting Employee Document Staging records.

11. After reviewing and determining the staging records look correct, click the **Start capture job** related link to start the import process.


**Parent Topic:**[Bulk imports in Employee Document Management](../concept/edm-bulk-uploads.md)

