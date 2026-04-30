---
title: Preview the security incident for the Splunk Enterprise Event Ingestion integration
description: After you complete the mapping step, preview the values that you mapped in a ServiceNow AI Platform Security Incident Response \(SIR\) security incident. This preview step permits you to verify that you have mapped all the alert fields that you want displayed on the security incident.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Create and name an event profile for the Splunk Enterprise Event Ingestion integration, Splunk Enterprise Event Ingestion integration for Security Operations by ServiceNow, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Preview the security incident for the Splunk Enterprise Event Ingestion integration

After you complete the mapping step, preview the values that you mapped in a ServiceNow AI Platform® Security Incident Response \(SIR\) security incident. This preview step permits you to verify that you have mapped all the alert fields that you want displayed on the security incident.

## Before you begin

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin, as the sn\_si.admin role inherits the required permissions by default.

## About this task

Preview a security incident and edit the mapping again as required to fix fields with errors or to populate any missing data. If the preview is not successfully completed, you cannot proceed to the scheduling step. Previews of SIR security incidents are not saved as actual incidents in the SIR product.

## Procedure

1.  If the security incident preview is not displayed, click **Preview** in the progress bar.

2.  Select the **Alert Name** and then select an item from the **Sample Alert IDs** list.

    ![Select alert choice list expanded.](../image/214_select_ID_previewsplunk.png)

    The security incident is displayed. Do not change any information in the fields. This view is a read-only view, and a record of this security incident is not saved.

3.  Review the field mapping of the alert values on the security incident.

    ![Error message on a security incident in the preview.](../image/214SplunkProfilePreviewPage.png)

    The preceding image is an example of a preview with a mapping error. In this example, a field on the security incident does not exist for a value, or the field does not support the value that you mapped. An error message is displayed that indicates an input value was not found for the `Configuration item` field.

4.  To resolve this error, click **Mapping** in the progress bar.

5.  Edit the mapping to fix incorrect values or populate any missing data.

6.  Preview the mapping again and continue to fix any errors that are described in error messages.

    The following figure is an example of the Incident Details tab on the bottom half of a SIR security incident after all error messages are resolved. For this example, the Description and Work notes fields were mapped, and these fields are populated with the values from the value pairs pulled from the Splunk Enterprise console. The first Work notes field has no value. This field was left empty on the mapping grid during the mapping step. The additional Work Note fields that have values were added to the mapping grid during the mapping step.

    ![Work note and Description fields on the security incident preview.](../image/splunk226_si-preview.png)

7.  After you have fixed any errors and verified that the fields are the way you want them, choose one option to continue.

<table id="choicetable_svs_ttl_kdb"><thead><tr><th align="left" id="d279850e190">

Option

</th><th align="left" id="d279850e193">

Description

</th></tr></thead><tbody><tr><td id="d279850e199">

**Continue**

</td><td>

The Scheduling form is displayed for profiles with scheduled alerts. **Scheduling** is selected on the progress bar.

</td></tr><tr><td id="d279850e213">

**Finish**

</td><td>

For profiles with configured for manual event forwarding, click **Finish**. There is no scheduling step for profiles with event data that are exported on-demand directly from the Splunk Enterprise console.

</td></tr><tr><td id="d279850e228">

**Update**

</td><td>

Your data is saved, and you are returned to the Splunk Event Profiles list.

</td></tr><tr><td id="d279850e240">

**Previous**

</td><td>

The Mapping step on the progress bar is displayed.

</td></tr><tr><td id="d279850e250">

**Delete**

</td><td>

Delete this event profile and the Splunk Event Profiles list is displayed.

</td></tr></tbody>
</table>
## What to do next

If no error messages are displayed, and you are satisfied with the field mapping on the security incident, the next step is to [Schedule and retrieve alerts for the Splunk Enterprise Event Ingestion integration](splunk-event-ingest-schedule.md).

**Parent Topic:**[Create and name an event profile for the Splunk Enterprise Event Ingestion integration](splunk-event-ingest-create-profile.md)

