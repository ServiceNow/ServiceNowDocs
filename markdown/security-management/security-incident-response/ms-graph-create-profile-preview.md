---
title: Preview the security incident for the Microsoft Graph Security API integration
description: After you complete the mapping step, preview the values that you mapped in a ServiceNow AI Platform SIR security incident. This preview step permits you to verify that you have mapped all the alert fields that you want displayed on the security incident.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create a profile, Microsoft Graph Security API alert ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Preview the security incident for the Microsoft Graph Security API integration

After you complete the mapping step, preview the values that you mapped in a ServiceNow AI Platform SIR security incident. This preview step permits you to verify that you have mapped all the alert fields that you want displayed on the security incident.

## Before you begin

Role required: sn\_si.admin

## About this task

As a user with the sn\_si.admin role, preview a security incident and edit the mapping again as required to fix fields with errors or to populate any missing data. If the preview is not successfully completed, you cannot proceed to the scheduling step. Previews of SIR security incidents are not saved as actual incidents in the Security Incident Response product.

## Procedure

1.  If the security incident preview is not displayed, click **Preview** in the progress bar.

    All the ingested alerts and the field mappings defined in the Mapping page are displayed.

2.  Click on an Alert ID to see a preview of the security incident.

    This view is a read-only view, and a record of this security incident is not saved.

3.  Review the field mapping of the alert values on the security incident.

    ![Microsoft Graph Security API: preview profile](../image/ms-graph-create-profile-5.png)

    The preceding image is an example of a preview with a mapping error of the samples that were ingested.

4.  To resolve this error, click **Mapping** in the progress bar.

5.  Edit the mapping to fix incorrect values or populate any missing data.

6.  Preview the mapping again and continue to fix any errors that are described in error messages.


## What to do next

If no error messages are displayed, and you are satisfied with the field mapping on the security incident, the next step is to define the schedule.

