---
title: DEX Score metric definitions
description: List of the base system DEX Score metric definitions.
locale: en-US
release: australia
product: Digital Experience Score
classification: digital-experience-score
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Digital Experience Score, Digital End-User Experience, IT Service Management]
---

# DEX Score metric definitions

List of the base system DEX Score metric definitions.

The DEX Score metrics are calculated for a specific application or device group within a defined time range and location.

|Metric|Application type|
|------|----------------|
|Application crashes|Installed|
|Average DNS lookup|Web|
|Average page load time|Web|
|Average response time|Web|
|CPU usage|Installed|
|Failed web requests|Web|
|Memory usage|Installed|

|Metric|
|------|
|Battery health|
|CPU usage|
|Disk usage|
|Memory usage|
|Wifi receive rate|
|Wifi RSSI|
|Wifi transmit rate|

|Metric|
|------|
|Application survey|
|Device survey|

<table id="table_z5j_shl_bgc"><thead><tr><th>

Metric

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Customer satisfaction scores for incident resolved

</td><td>

The score for customer satisfaction surveys sent to users for resolved incidents. Scores are calculated only for those surveys that have been successfully submitted by users.Normalized values for surveys are considered and surveys with normalized values greater than zero are assigned weights on a scale of 0–100. For more information, see [Normalized value for an assessment](https://www.servicenow.com/docs/access?context=example-normalized-value-calc&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

Number of resolved incidents

</td><td>

The number of incidents resolved or closed for an application or device group.For example, the number of Chrome application incidents resolved in the first week of July in New York.

</td></tr><tr><td>

Mean time to resolve an incident

</td><td>

The average time \(in hours\) taken to resolve incidents. It is calculated by averaging the differences between incident creation and resolution times for resolved incidents.

</td></tr><tr><td>

Number of closed major incidents

</td><td>

The number of major incidents resolved or closed for an application or device group.Major incidents are filtered by confirming that the Major Incident Management plugin \(com.snc.incident.mim\) is active and the **Major incident state** field on incident records is set to **Accepted**.

</td></tr><tr><td>

Percentage of first assignment resolution

</td><td>

This percentage is calculated by dividing the total number of first assignment resolution incidents \(incidents with **Reassignment count** of zero in incident records\) by the total number of incidents, and multiplying the result by 100.

</td></tr><tr><td>

Percentage of incidents that breached SLA

</td><td>

This percentage is calculated by dividing the number of incidents that have breached the SLA time by the total number of incidents, and multiplying the result by 100.The total number of incidents with SLA breach is the sum of incidents with the **Has breached** state marked as **true** in the Task SLA table of the incident records.

</td></tr><tr><td>

Percentage of reopened incidents

</td><td>

This percentage is calculated by dividing the number of incidents with **Reopened count** greater than zero in the incident records by the total number of incidents, and multiplying the result by 100.

</td></tr><tr><td>

Total outages due to incidents

</td><td>

The total duration of outages or degradation \(in hours\) caused by incidents.It is calculated as the sum of the durations of all outages recorded in the cmdb\_ci\_outage table.

</td></tr></tbody>
</table>The number of closed major incidents, resolved incidents, and total outages due to incidents are metrics that help evaluate service desk experience but don’t contribute to the experience score.

**Parent Topic:**[Digital Experience Score​ reference](../concept/dexscr-dex-score-reference.md)

