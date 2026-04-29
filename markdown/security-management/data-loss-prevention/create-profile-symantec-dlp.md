---
title: Create a profile for Symantec DLP integration
description: Create an incident profile in your  ServiceNow AI Platform instance. Determine the  Symantec DLP incidents that are suitable for creating DLP incidents.
locale: en-US
release: australia
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Symantec Integration for Data Loss Prevention Incident Response, Integrate, Data Loss Prevention Incident Response, Security Operations]
---

# Create a profile for Symantec DLP integration

Create an incident profile in your  ServiceNow AI Platform instance. Determine the  Symantec DLP incidents that are suitable for creating DLP incidents.

## Before you begin

Role required: sn\_dlir.admin

## About this task

Configure the ServiceNow AI Platform® to fetch the DLP incidents from the Symantec endpoint. Store these incidents into your ServiceNow® instance as DLP incidents.

## Procedure

1.  Navigate to **Symantec DLP integration** &gt; **Incident Profile**.

2.  Click **New**.

3.  On the form, fill the fields in the Name section.

<table id="table_dq5_sbz_2tb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the profile. This field helps you to identify the profile.**Note:** The name must be unique for each profile.

</td></tr><tr><td>

Source

</td><td>

Symantec DLP instance that you configured to ingest incidents. If you have multiple instances configured, select the appropriate instance for the incident types that you are planning to ingest for the profile.

</td></tr><tr><td>

Active

</td><td>

Option to indicate if the profile is active. This field can only be enabled after you click the **Finish** in the Scheduling section.When the profile is active, it implies that the  ServiceNow AI Platform is actively polling Symantec DLP incidents. The corresponding DLP incidents are created in  DLP  when the filtering conditions are matched based on the Scheduling parameters that you have provided.

</td></tr><tr><td>

Symantec Enforce Server Timezone

</td><td>

Select the time zone for symantec enforce server in the profile so that incidents are not missed due to the time zone issues.

</td></tr><tr><td>

Consider Daylight Saving Time

</td><td>

Select this check box if the enforce server follows the daylight saving time.

</td></tr><tr><td>

Order

</td><td>

Order of the profile execution. The profile with the lowest order considered as the highest priority.By default, the value is 100.

</td></tr><tr><td>

Description

</td><td>

Unique description for this profile.

</td></tr></tbody>
</table>    ![DLP incident profile](../image/dlp-incident-profile.png)


## What to do next

To move to the Filtering section,  click **Continue**.

-   **[Define filters to apply for the Incident creation](define-filters-symantec.md)**  
Define and set filter conditions to drill down the incoming  Symantec DLP  incidents. Determine the incidents that should be created as DLP incidents in ServiceNow®.
-   **[Configure evidence file storage](config-evidence-file.md)**  
Configure evidence file storage to securely store the evidence file for the DLP Incidents.
-   **[Download evidence files](download-evidence-files.md)**  
Download DLP incident evidence files that violate the DLP policy on Symantec.
-   **[Preview evidence files](preview-file-symantec.md)**  
Preview Data Loss Prevention Incident Response evidence files in the DLP IR Analyst workspace.
-   **[Schedule the Symantec DLP Incident Retrieval](schedule-dlp-incident-retrieval.md)**  
Set a schedule to retrieve the incident data and ingest Symantec DLP incidents that match the criteria in the profile. Configure the schedule to define how and when you pull incidents from Symantec.
-   **[Mapping Symantec DLP incident statuses with ServiceNow incident Status](map-symantec-dlp.md)**  
Synchronize the status of the DLP incidents ingested on the ServiceNow with the DLP incidents of the Symantec. Map the **ServiceNow Incident Status** field with the **Symantec Incident Status** field.

**Parent Topic:**[Symantec Integration for Data Loss Prevention Incident Response](../concept/symantec-dlp-integration.md)

