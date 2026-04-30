---
title: Create a Profile for Proofpoint DLP integration
description: Create an incident profile in your  ServiceNow AI Platform instance. Determine the  Proofpoint DLP incidents that are suitable for creating DLP incidents.
locale: en-US
release: xanadu
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Data Loss Prevention Incident Response Integration with Proofpoint, DLP integrations, Data Loss Prevention Incident Response, Security Operations]
---

# Create a Profile for Proofpoint DLP integration

Create an incident profile in your  ServiceNow AI Platform instance. Determine the  Proofpoint DLP incidents that are suitable for creating DLP incidents.

## Before you begin

Role required: sn\_dlir.admin

## About this task

Configure the ServiceNow AI Platform to populate DLP alerts of Proofpoint. Store the alerts as DLP incidents in your ServiceNow instance.

## Procedure

1.  Navigate to **Proofpoint DLP integration** &gt; **Incident Profile**.

2.  Click **New**.

3.  On the form, fill the fields in the **Name** section.

<table id="table_jxg_fb2_ltb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the profile. This name helps you to identify the profile.**Note:** The name must be unique for each profile.

</td></tr><tr><td>

Source

</td><td>

The Proofpoint DLP instance that you configured to ingest incidents. If you have multiple instances configured, select the appropriate instance for the incident types that you are planning to ingest for the profile.

</td></tr><tr><td>

Active

</td><td>

Option to make the profile active.When the profile is active, your ServiceNow AI Platform instance is ready to receive the incidents from Proofpoint.

</td></tr><tr><td>

Description

</td><td>

Description to help distinguish this profile from other profiles.

</td></tr></tbody>
</table>    ![Create a profile for Proofpoint DLP integration.](../../data-loss-prevention/image/dlp-proofpoint-name.gif)

4.  Click **Continue** and move to the Filtering section.


-   **[Define filters to apply for the Incident creation](../concept/define-filters-incident-creation-proofpoint.md)**  
Define and set filter conditions to filter the incoming  Proofpoint DLP  incidents. Control which DLP incidents should be created on ServiceNow®.
-   **[Configure evidence file storage](configure-evidence-file-storage.md)**  
Configure evidence file storage to securely store the evidence files in the ServiceNow instance or external for the Proofpoint email DLP Incidents.
-   **[Download DLP incidents evidence files on Proofpoint](download-proofpoint-evidence-files.md)**  
Download DLP incident evidence files that violate the DLP policy on Proofpoint.
-   **[Preview evidence files](preview-file-proofpoint.md)**  
Preview Data Loss Prevention Incident Response evidence files in the DLP IR Analyst workspace.
-   **[Email remediation actions](email-actions.md)**  
Perform the remediation action on the email quarantined for Proofpoint.

**Parent Topic:**[Data Loss Prevention Incident Response Integration with Proofpoint](../concept/dlp-incident-response-integration-proofpoint.md)

