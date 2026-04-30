---
title: Create a profile for ICAP DLP integration
description: Create an incident profile in your  ServiceNow AI Platform instance. Determine the  ICAP DLP alerts that are suitable for creating DLP incidents.
locale: en-US
release: xanadu
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2024-09-11"
reading_time_minutes: 1
breadcrumb: [Internet Content Adaption Protocol \(ICAP\) integration for DLP IR, DLP integrations, Data Loss Prevention Incident Response, Security Operations]
---

# Create a profile for ICAP DLP integration

Create an incident profile in your  ServiceNow AI Platform instance. Determine the  ICAP DLP alerts that are suitable for creating DLP incidents.

## Before you begin

Role required: sn\_dlir.admin

## About this task

Configure the NowPlatform to fetch the DLP alerts from Amazon S3 configuration. Store these alerts into your ServiceNow instance as DLP incidents.

## Procedure

1.  Navigate to **All** &gt; **ICAP DLP Integration** &gt; **Incident Profile**.

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

Amazon S3 configuration that you configured to ingest incidents. If you have multiple sources configured, select the appropriate source for the incident type that you are planning to ingest for the profile.**Note:** Only a single source is allowed for the active profile.

</td></tr><tr><td>

Active

</td><td>

Option to indicate if the profile is active. This field can only be enabled after you click the **Finish** in the Scheduling section.When the profile is active, it implies that the  ServiceNow AI Platform is actively polling ICAP DLP alerts. The corresponding DLP alerts are created in  DLP  when the filtering conditions are matched based on the Scheduling parameters that you have provided.

</td></tr><tr><td>

Order

</td><td>

Order of the profile execution. The profile with the lowest order considered as the highest priority.By default, the value is 100.

</td></tr><tr><td>

Description

</td><td>

Description for this profile.

</td></tr></tbody>
</table>    ![ICAP DLP incident profile](../image/dlp-icap-incident-profile.png)


## What to do next

To move to the Filtering section,  click **Continue**.

-   **[Define filters to apply for the Incident creation](define-filters-for-incidents.md)**  
Define and set filter conditions to filter the incoming  DLP  alerts. Determine the alerts that should be created as DLP incidents in ServiceNow.
-   **[Schedule the ICAP DLP incidents retrieval](schedule-icap-dlp-incidents-retrieval.md)**  
Set a schedule to retrieve ICAP DLP alerts that match the criteria in the profile.

**Parent Topic:**[Internet Content Adaption Protocol \(ICAP\) integration for DLP IR](../concept/icap-dlp-integration.md)

