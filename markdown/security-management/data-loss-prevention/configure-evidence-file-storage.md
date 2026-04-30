---
title: Configure evidence file storage
description: Configure evidence file storage to securely store the evidence files in the ServiceNow instance or external for the Proofpoint email DLP Incidents.
locale: en-US
release: yokohama
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2024-09-19"
reading_time_minutes: 2
breadcrumb: [Create a Profile for Proofpoint DLP integration, Data Loss Prevention Incident Response Integration with Proofpoint, DLP integrations, Data Loss Prevention Incident Response, Security Operations]
---

# Configure evidence file storage

Configure evidence file storage to securely store the evidence files in the ServiceNow instance or external for the Proofpoint email DLP Incidents.

## Before you begin

Role required: sn\_dlir.admin

## About this task

You can configure the evidence file storage to securely store files. This provides an option for internal storage in ServiceNow instance or store externally, ensuring that files are stored and encrypted using Column Level Encryption. For more information, see [Field Encryption](https://servicenow.com/docs/bundle/xanadu-platform-security/page/administer/encryption/concept/column-level-encryption-landing.html) on NowPlatform documentation.

When a DLP analyst performs the Download evidence files for DLP Incidents action from analyst workspace, the file will be downloaded from the selected storage if evidence file storage option is enabled. Otherwise, the file will be downloaded directly from the Proofpoint source and will not be persisted in ServiceNow instance. For more information, see [Download DLP incidents evidence files on Proofpoint](download-proofpoint-evidence-files.md).

## Procedure

1.  Select **Evidence Storage** section on the Incident Profile form.

2.  Select **Evidence File Storage** check box to enable the file storage.

3.  Select the preferred storage type.

<table id="choicetable_yhz_yvv_tcc"><thead><tr><th align="left" id="d173613e102">

Field

</th><th align="left" id="d173613e105">

Description

</th></tr></thead><tbody><tr><td id="d173613e111">

**Evidence file storage**

</td><td>

Option to enable the evidence file storage.

</td></tr><tr><td id="d173613e120">

**Storage type**

</td><td>

Option to select the preferred storage type. You can use either internal or external storage to store the evidence files.-   **ServiceNow Storage**: This will store the evidence files in the ServiceNow instance in an encrypted format.
-   **Evidence File Storage**:

This storage provides a flexibility to manage the evidence files, allows you to choose the preferred storage method. Internal storage offers quick access within the application, while external storage supports both Blob storage and Amazon S3 storage options and allows the increased capacity and backup options. When you select this storage type, a new field is displayed: **External File Storage Source**.

</td></tr><tr><td id="d173613e146">

**External File Storage Source**

</td><td>

This field supports both Blob storage and Amazon S3 storage options. This is in reference to the existing DLP Core configuration tiles for S3 or blob storage which are being used in Microsoft integration for match content storage.

</td></tr></tbody>
</table>4.  **Internal Storage**

    ![Internal storage view](../image/dlp-proofpoint-internal-storage.png)

    **External Storage**

    ![DLP Proofpoint external storage view.](../image/dlp-proofpoint-external-storage.png)

5.  Click **Finish**.


## Result

If the **Evidence File Storage** option is enabled and ServiceNow Storage is selected then the evidence files will be stored internally in an encrypted format, after the incidents from Proofpoint are fetched and if you perform **Download File** action for any of these Proofpoint incident then the system will get the evidence file from this table.

**Parent Topic:**[Create a Profile for Proofpoint DLP integration](create-profile-proofpoint-dlp-integration.md)

