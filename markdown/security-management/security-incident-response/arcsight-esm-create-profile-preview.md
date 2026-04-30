---
title: Preview the security incident for the ArcSight ESM event ingestion Integration
description: After you complete the mapping step, preview the values that you mapped in a ServiceNow AI Platform Security Incident Response \(SIR\) security incident. This preview step permits you to verify that you have mapped all the correlation fields that you want displayed on the security incident.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, Set up instance, ArcSight ESM Event Ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Preview the security incident for the ArcSight ESM event ingestion Integration

After you complete the mapping step, preview the values that you mapped in a ServiceNow AI Platform Security Incident Response \(SIR\) security incident. This preview step permits you to verify that you have mapped all the correlation fields that you want displayed on the security incident.

## Before you begin

Role required: sn\_si.admin.

## About this task

As a user with the sn\_si.admin role, preview a security incident and edit the mapping again as required to fix fields with errors or to populate any missing data. If the preview is not successfully completed, you cannot proceed to the scheduling step. Previews of security incidents are not saved as actual incidents in the Security Incident Response product.

## Procedure

1.  If the security incident preview is not displayed, click **Preview** in the progress bar.

2.  From the Sample Event IDs choice list, select an item.

    The security incident is displayed. Do not change any information in the fields. This view is a read-only view, and a record of this security incident is not saved.

3.  Review the field mapping of the correlation event values on the security incident.

    ![ArcSight ESM: Create Profile: Preview](../image/sir-arcsight-esm-profile-preview.png)

    The preceding image is an example of a preview with a mapping error. In this example, a field value from the correlation event does not have an acceptable value for the reference field on the SIR incident form. An error message is displayed that indicates an input value was not found for the `Category` field which is a reference field with a specific set of values. As a result, this mapped field value will not appear on the SIR security incident form without further modification.

4.  To resolve this error, click **Mapping** in the progress bar.

5.  Edit the mapping to fix incorrect values or populate any missing data.

6.  Preview the mapping again and continue to fix any errors that are described in error messages.

    The following figure is an example of the Incident Details tab on the bottom half of a security incident after all error messages are resolved. For this example, the Description and Work notes fields were mapped, and these fields are populated with the values from the value pairs pulled from the ArcSight ESM correlation event samples.

    ![ArcSight ESM: Create Profile: preview incident](../image/sir-arcsight-esm-profile-preview1.png)


## What to do next

If no error messages are displayed, and you are satisfied with the field mapping on the security incident, the next step is to define the schedule.

