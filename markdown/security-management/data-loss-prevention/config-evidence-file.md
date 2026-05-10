---
title: Configure evidence file storage
description: Configure evidence file storage to securely store the evidence file for the DLP Incidents.
locale: en-US
release: australia
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a profile for Symantec DLP integration, Symantec Integration for Data Loss Prevention Incident Response, Integrate, Data Loss Prevention Incident Response, Security Operations]
---

# Configure evidence file storage

Configure evidence file storage to securely store the evidence file for the DLP Incidents.

## Before you begin

Role required: sn\_dlir.admin

Verify that the Symantec user that you are configuring for ServiceNow Symantec DLP integration must have Body, Attachments and Original Message options enabled from Roles configuration page on Symantec DLP portal. For more information, see Display Attributes section available on [Configuring Roles](https://techdocs.broadcom.com/us/en/symantec-security-software/information-security/data-loss-prevention/16-0-1/Manage-the-Enforce-Server/managing-users-and-rules/configuring-roles-id-sf0b0167317a-d297e3139.html) document for more information.

## About this task

You can configure the evidence file storage to securely store files. This provides an option for internal storage in ServiceNow instance, ensuring that files are stored and encrypted using ServiceNow's Field Encryption. For more information, see [Field Encryption](https://servicenow.com/docs/bundle/washingtondc-platform-security/page/administer/encryption/concept/c_EncryptionSupport.html) on NowPlatform documentation.

When DLP analyst performs the Download evidence files for DLP Incidents action from analyst workspace, the file will be downloaded from the selected storage if evidence file storage option is enabled. Otherwise, the file will be downloaded directly from the Symantec source and will not be persisted in ServiceNow instance.

**Note:** When a DLP analyst performs the Download evidence files for DLP Incidents action from analyst workspace, the file will be downloaded from the selected storage if evidence file storage option is enabled. Otherwise, the file will be downloaded directly from the Symantec source and will not be persisted in ServiceNow instance.

## Procedure

1.  Navigate to **All** &gt; **Symantec DLP Integration** &gt; **Incident Profile**.

2.  Click on **Evidence Storage** section on the Incident Profile form.

3.  Select **Evidence File Storage** check box to enable the file storage.

4.  Select the preferred storage type.

<table id="choicetable_hl4_mjf_jcc"><thead><tr><th align="left" id="d453460e119">

Type

</th><th align="left" id="d453460e122">

Description

</th></tr></thead><tbody><tr><td id="d453460e128">

**Evidence File Storage**

</td><td>

Option to enable the Evidence file storage.

</td></tr><tr><td id="d453460e137">

**Storage Type**

</td><td>

Option to select the preferred storage type.**Note:** **ServiceNow Storage**: This will store the evidence files in the ServiceNow instance in an encrypted format.

</td></tr></tbody>
</table>5.  Click **Continue** and move to the **Scheduling** section.


## Result

The evidence files are stored as per the configuration, after the incident ingestion is completed.

**Parent Topic:**[Create a profile for Symantec DLP integration](create-profile-symantec-dlp.md)

