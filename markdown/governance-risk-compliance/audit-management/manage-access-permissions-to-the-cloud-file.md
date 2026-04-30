---
title: Create a Cloud file configuration record
description: Create a cloud file configuration record to manage the access permissions on the cloud document.
locale: en-US
release: yokohama
product: Audit Management
classification: audit-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a Cloud file configuration on engagements and audit tasks, Manage your documents and work papers with Audit Management as cloud files, Using Audit Management, Audit Management, Governance, Risk, and Compliance]
---

# Create a Cloud file configuration record

Create a cloud file configuration record to manage the access permissions on the cloud document.

## Before you begin

Role required: sn\_grc\_workspace.admin \(CRUD\), sn\_grc\_workspace.user \(Read\)

## Procedure

1.  Navigate to **All** &gt; **GRC Administration** &gt; **Cloud file configuration**.

2.  Select **New**.

3.  On the Cloud file configuration form, fill in the fields.

    For more information on the fields in the form, see [Cloud file configuration record form](../reference/document-access-configuration-record-form.md). Once the parent cloud file configuration is active, you can configure the File access permissions for the Cloud file configuration record as shown in the example.

    ![Cloud file configuration record.](../image/cloud-file-configuration-record.png)

    Cloud file and folders are validated based on the following:

    -   **Folder structure**

        You can either dynamically configure the folder structure or enter a static folder structure.

        In the folder path, the name of the engagement `${name}` may change, which might change the folder path too. However, the folder path to which the first file was uploaded for this record is picked for all subsequent uploads, even if the values in the dynamic fields change.

    -   **Folder access**
        -   If you have access to the folder but no access to the file in the folder, then you cannot view the particular file but can view the other files in the folder that you have access to.
        -   If you do not have access to the folder but can access the file in the folder, then you can view only that particular file in the folder that you have access to.
    -   **Folder name**

        If you change the name of the folder or the folder path, then you must manually migrate all the files from the older file path to the new file path. The same must be changed in the cloud folder structure as well.

        The folder path where the file is uploaded is stored against every ServiceNow record in the Cloud folder path \[sn\_grc\_workspace\_cloud\_folder\_path\] table.

        ![Folder path to upload a file in cloud.](../image/cloud-folder-path.png)

4.  Select **Submit**.


