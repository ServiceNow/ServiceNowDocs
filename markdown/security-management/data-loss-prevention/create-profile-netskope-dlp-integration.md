---
title: Create a Profile for Netskope DLP integration
description: Create an incident profile in your ServiceNow AI Platform instance.
locale: en-US
release: yokohama
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Data Loss Prevention Incident Response Integration with Netskope, DLP integrations, Data Loss Prevention Incident Response, Security Operations]
---

# Create a Profile for Netskope DLP integration

Create an incident profile in your ServiceNow AI Platform instance.

## Before you begin

Role required: sn\_dlir.admin

## About this task

Configure ServiceNow AI Platform to retrieve the DLP incidents from the Netskope endpoint. Store the incidents into your ServiceNow instance as DLP incidents.

## Procedure

1.  Navigate to **Netskope DLP integration** &gt; **Incident Profile**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_ljq_lf2_ltb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the profile. The name must be unique for each profile. This name helps you to identify the profile.

</td></tr><tr><td>

Source

</td><td>

Netskope DLP instance that you configured to ingest incidents. If you have multiple instances configured, select the appropriate instance for the incident types that you are planning to ingest for the profile.**Note:** Only one active profile is allowed per source.

</td></tr><tr><td>

Active

</td><td>

Indicator that the profile is active.**Note:** This field is available only after you click **Finish** in the last Scheduling section.

When the profile is active, your ServiceNow AI Platform instance is actively polling Netskope DLP incidents.

Corresponding DLP incidents are created as ServiceNow DLP incidents when the filtering conditions are matched based on the Scheduling parameters you have provided.

</td></tr><tr><td>

Order

</td><td>

Order of the profile execution. The profile with the lowest order considered as the highest priority.By default, the value is 100.

</td></tr><tr><td>

Description

</td><td>

Description to help you distinguish this profile from other profiles.

</td></tr></tbody>
</table>4.  Click **Continue** and move to the Filtering section.


-   **[Define Filters to apply for the Incident creation](define-filters-incident-creation-netskope.md)**  
Define and set filter conditions to filter the incoming  Netskope DLP  incidents. Control which of these incidents should be created as DLP incidents on your ServiceNow instance.
-   **[Schedule the Netskope DLP incidents retrieval](schedule-netskope-dlp-alerts-retrieval.md)**  
Set a schedule to retrieve Netskope DLP incidents that match the criteria in the profile.

**Parent Topic:**[Data Loss Prevention Incident Response Integration with Netskope](../concept/dlp-incident-response-integration-netskope.md)

