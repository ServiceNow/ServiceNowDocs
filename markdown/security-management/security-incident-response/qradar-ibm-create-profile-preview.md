---
title: Preview security incident
description: After you complete the mapping step, preview the values that you mapped in a SIR security incident. This preview permits you to verify that you have mapped all the offense fields that you want displayed on the security incident.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setup IBM QRadar profile, Set up instance, IBM QRadar Offense Ingestion Integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Preview security incident

After you complete the mapping step, preview the values that you mapped in a SIR security incident. This preview permits you to verify that you have mapped all the offense fields that you want displayed on the security incident.

## Before you begin

Role required: sn\_si.admin

## About this task

As a user with the sn\_si.admin role, preview a security incident and edit the mapping again as required to fix fields with errors or to populate any missing data. If the preview is not successfully completed, you cannot proceed to the scheduling step. Previews of SIR security incidents are not saved as actual incidents in the Security Incident Response product.

## Procedure

1.  If the security incident preview is not displayed, click **Preview** in the progress bar.

2.  From the Sample Offense IDs choice list, select an item.

    The security incident is displayed. This view is a read-only view, and a record of this security incident is not saved.

3.  Review the field mapping of the offense values on the security incident.

    ![IBM QRadar: Create Profile: Preview](../image/ibm-qradar-profile-preview-1.png)

    The preceding image is an example of a preview with a mapping error of the samples that were ingested.

4.  To resolve this error, select **Mapping** in the progress bar.

5.  Edit the mapping to fix incorrect values or populate any missing data.

6.  Preview the mapping again and continue to fix any errors that are described in error messages.

    The following figure is an example of the Incident Details tab on the bottom half of a SIR security incident after all error messages are resolved.

    ![Work note and Description fields on the security incident preview.](../image/ibm-qradar-profile-preview-2.png)

    **Note:** The Profile Preview section displays related items for **Unmatched Affected User** and **Unmatched Configuration Item** when matching CMDB or identity records are not found. After ingestion, Security Incident records show **Unmatched CI** in the **Configuration Items** related list and **Unmatched Affected Users** in a dedicated related list, ensuring complete visibility of affected entities throughout the incident life-cycle.

7.  Select **Continue**.


## What to do next

If no error messages are displayed, and you are satisfied with the field mapping on the security incident, the next step is to define the schedule. For more information, see [Define schedule](qradar-ibm-create-profile-schedule.md).

