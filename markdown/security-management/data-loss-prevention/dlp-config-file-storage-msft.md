---
title: Configure evidence file storage for Microsoft
description: Configure evidence file storage to securely store the evidence file in the ServiceNow instance for the Microsoft incidents of type OneDrive, Exchange and SharePoint.
locale: en-US
release: xanadu
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2024-11-20"
reading_time_minutes: 1
breadcrumb: [Data Loss Prevention Incident Response with Microsoft, DLP integrations, Data Loss Prevention Incident Response, Security Operations]
---

# Configure evidence file storage for Microsoft

Configure evidence file storage to securely store the evidence file in the ServiceNow instance for the Microsoft incidents of type OneDrive, Exchange and SharePoint.

## Before you begin

Role required: sn\_dlir.admin

## About this task

You can configure the evidence file storage to securely store files. This provides an option for internal storage in ServiceNow instance, ensuring that files are stored and encrypted using ServiceNow Column Level Encryption. For more information, see Encryption Support on ServiceNow AI Platform documentation.

When a DLP analyst or approver performs the Download evidence files for DLP Incidents action from analyst workspace, the file will be downloaded from the selected storage if evidence file storage option is enabled. Otherwise, the file will be downloaded directly from the Microsoft source and will not be persisted in the ServiceNow instance. For more information, see [Download files for DLP incidents of type Exchange Online, OneDrive, and SharePoint](download-file-dlp-microsoft.md).

## Procedure

1.  Select **Evidence Storage** section on the **Incident Profile** form.

2.  Select **Evidence File Storage** check box to enable the file storage.

3.  Select the preferred storage type.

<table id="choicetable_tq4_n1g_ldc"><thead><tr><th align="left" id="d52621e119">

Field

</th><th align="left" id="d52621e122">

Description

</th></tr></thead><tbody><tr><td id="d52621e128">

**Evidence file storage**

</td><td>

Option to enable the evidence file storage.

</td></tr><tr><td id="d52621e137">

**Storage type**

</td><td>

Option to select the preferred storage type.**ServiceNow Storage**: Option that stores the evidence files in the ServiceNow instance in an encrypted format.

</td></tr></tbody>
</table>4.  Click **Continue** and move to the **Scheduling** section.


## Result

If the **Evidence File Storage** option is enabled and ServiceNow and the **Storage** option is selected then the evidence files will be stored internally in the ServiceNow instance in an encrypted format. The **Download file** action will get the file from the ServiceNow instance after the files are stored.

**Parent Topic:**[Data Loss Prevention Incident Response with Microsoft](../concept/dlp-integration-microsoft.md)

