---
title: Create a new incident profile for Microsoft DLP integration
description: Create an incident profile in your  ServiceNow AI Platform instance to retrieve the data from the Microsoft Purview and add the data into the ServiceNow DLP IR incident table.
locale: en-US
release: yokohama
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Data Loss Prevention Incident Response with Microsoft, DLP integrations, Data Loss Prevention Incident Response, Security Operations]
---

# Create a new incident profile for Microsoft DLP integration

Create an incident profile in your  ServiceNow AI Platform instance to retrieve the data from the Microsoft Purview and add the data into the ServiceNow DLP IR incident table.

## Before you begin

Role required: sn\_dlir.admin\(Create, edit, and delete\)

sn\_dlir.analyst - View \(read-only\)

## About this task

Configure the ServiceNow AI Platform® to retrieve the events from the Microsoft Purview. Store these events on the DLP IR Incident table on your ServiceNow® instance.

## Procedure

1.  Navigate to **Microsoft DLP integration** &gt; **Incident Profile**.

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

The Microsoft DLP IR instance that you configured to ingest incidents. If you have multiple integration configurations, select the appropriate integration configuration record for the incident types that you are planning to ingest for the profile.

</td></tr><tr><td>

Active

</td><td>

Option to indicate if the profile is active. This field can only be enabled after you click the **Finish** field in the Scheduling section.When the profile is active, it implies that the  ServiceNow AI Platform is actively polling Microsoft DLP IR events based on the configuration defined in the profile.

</td></tr><tr><td>

Order

</td><td>

Order of the profile execution. The profile with the lowest order considered as the highest priority.By default, the value is 100.

</td></tr><tr><td>

Description

</td><td>

Unique description for the profile.

</td></tr></tbody>
</table>
## What to do next

To move to the Filtering section,  click **Continue**.

-   **[Microsoft purview endpoint storage configuration](../concept/microsoft-purview-endpoint.md)**  
Microsoft Purview endpoint evidence files storage configuration tells you where the endpoint evidence files are being stored by the purview- Custom managed store or Microsoft managed storage environments.
-   **[Define filters to apply for the Incident creation](define-filters-profile-microsoft.md)**  
Define and set filter conditions to filter the incoming  Microsoft DLP  events. Control which of these events should be created as DLP IR incidents on your ServiceNow instance.
-   **[Configure the match content for the incident](matching-content-configuration-microsoft.md)**  
Provide the configuration to store the sensitive information internally, on the ServiceNow® storage, or on the external cloud storage, such as Azure Storage or AWS S3 bucket. Retrieve the stored content while accessing the DLP IR Incident.
-   **[Schedule the DLP IR Microsoft incident retrieval](schedule-profile-microsoft.md)**  
Set a schedule to retrieve the incident data and ingest Microsoft DLP IR incidents that match the criteria in the profile. Configure the schedule to define how and when you pull incidents from Microsoft.

**Parent Topic:**[Data Loss Prevention Incident Response with Microsoft](../concept/dlp-integration-microsoft.md)

