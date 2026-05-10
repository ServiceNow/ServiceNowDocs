---
title: Preview security incident
description: After you complete the mapping step, preview the values that you mapped in a ServiceNow AI Platform Security Incident Response \(SIR\) security incident. This preview step permits you to verify that you have mapped all the notable fields that you want displayed on the security incident.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Set up a profile for scheduled notable event ingestion, Create an event profile, Splunk Enterprise Security event ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Preview security incident

After you complete the mapping step, preview the values that you mapped in a ServiceNow AI Platform® Security Incident Response \(SIR\) security incident. This preview step permits you to verify that you have mapped all the notable fields that you want displayed on the security incident.

## Before you begin

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin, as the sn\_si.admin role inherits the required permissions by default.

## About this task

Preview a security incident and edit the mapping again as required to fix fields with errors or to populate any missing data. If the preview is not successfully completed, you cannot proceed to the scheduling step. Previews of SIR security incidents are not saved as actual incidents in the SIR product.

## Procedure

1.  If the security incident preview is not displayed, select **Preview** in the progress bar.

2.  From the Event Name choice list, select an item if multiple Events were used.

3.  Select event IDs from the Sample Notable Event IDs choice list.

4.  From the Sample Notable Event IDs choice list, select an item.

    ![Select event choice list expanded.](../image/new-images/splunk-es-preview.png)

    The security incident is displayed. Do not change any information in the fields. This view is a read-only view, and a record of this security incident is not saved.

5.  Review the field mapping of the notable event values on the security incident.

    ![Error message on a security incident in the preview.](../image/new-images/preview-select-event.png)

    The preceding image is an example of a preview with a mapping error. In this example, a field value from the notable event does not have an acceptable value for the reference field on the SIR incident form. An error message is displayed that indicates an input value was not found for **Priority** field. As a result, this mapped field value will not appear on the SIR security incident form without further modification.

6.  To resolve this error, select **Mapping** in the progress bar.

7.  Edit the mapping to fix incorrect values or populate any missing data.

8.  Preview the mapping again and continue to fix any errors that are described in error messages.

    The following figure is an example of the Incident Details tab on the bottom half of a SIR security incident after all error messages are resolved. For this example, the Description and Work notes fields were mapped, and these fields are populated with the values from the value pairs pulled from the Splunk Enterprise Security notable event samples. The first Work notes field has no value. This field was left blank on the mapping grid during the mapping step. The additional Work Note fields that have values were added to the mapping section.

    ![Work note and Description fields on the security incident preview](../image/previewsplunk_es_worknote_security.png)

    **Note:** The Profile Preview section displays related items for **Unmatched Affected User** and **Unmatched Configuration Item** when matching CMDB or identity records are not found. After ingestion, Security Incident records show **Unmatched CI** in the **Configuration Items** related list and **Unmatched Affected Users** in a dedicated related list, ensuring complete visibility of affected entities throughout the incident life-cycle.

9.  After you have fixed any errors and verified that the fields are the way you want them, choose one option to continue.

<table id="choicetable_svs_ttl_kdb"><thead><tr><th align="left" id="d331584e209">

Option

</th><th align="left" id="d331584e212">

Description

</th></tr></thead><tbody><tr><td id="d331584e218">

**Continue**

</td><td>

The Scheduling form is displayed for profiles with scheduled notable events. **Scheduling** is selected on the progress bar.

</td></tr><tr><td id="d331584e232">

**Finish**

</td><td>

For profiles with configured for manual event forwarding, click **Finish**. There is no scheduling step for profiles with event data that are exported on-demand directly from the Splunk Enterprise Security console.

</td></tr><tr><td id="d331584e247">

**Update**

</td><td>

Your data is saved, and you are returned to the Splunk Event Profiles list.

</td></tr><tr><td id="d331584e259">

**Previous**

</td><td>

The Mapping step on the progress bar is displayed.

</td></tr><tr><td id="d331584e269">

**Delete**

</td><td>

Delete this event profile and the Splunk Event Profiles list is displayed.

</td></tr></tbody>
</table>
## What to do next

If no error messages are displayed, and you are satisfied with the field mapping on the security incident, the next step is to [Schedule and retrieve alerts for the Splunk Enterprise Event Ingestion integration](splunk-event-ingest-schedule.md).

