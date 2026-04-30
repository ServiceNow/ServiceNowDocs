---
title: DEX Score metric definitions
description: List of the base system DEX Score metric definitions.
locale: en-US
release: zurich
product: Digital Experience Score
classification: digital-experience-score
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Reference, Digital Experience Score, Digital End-User Experience, IT Service Management]
---

# DEX Score metric definitions

List of the base system DEX Score metric definitions.

The DEX Score metrics are calculated for a specific application or device group within a defined time range and location. Device and application metrics that are aggregated periodically at daily, weekly, or monthly intervals are normalized on a scale of 0-100. For more information, see [DEX Score normalization for metric scores](dexscr-dex-score-normalization.md).

## Application Metrics

<table id="table_b13_fwp_c2c"><thead><tr><th>

Metric

</th><th>

Application type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Application crashes

</td><td>

Installed

</td><td>

The number of times an application stops functioning during the selected period.

</td></tr><tr><td>

Average DNS lookup

</td><td>

Web

</td><td>

Average time taken to complete a Domain Name System \(DNS\) lookup during the selected period.

 A lower average DNS lookup contributes to faster web page loading and improved overall internet performance.

</td></tr><tr><td>

Average page load time

</td><td>

Web

</td><td>

Average time taken to load a page, from initiation to load completion during the selected period.

</td></tr><tr><td>

Average response time

</td><td>

Web

</td><td>

Average time taken to respond to user requests during the selected period.

</td></tr><tr><td>

CPU usage

</td><td>

Installed

</td><td>

Amount of processing power consumed by an application, measured in percentage.

</td></tr><tr><td>

Failed web requests

</td><td>

Web

</td><td>

Set of all requests that either return an Error Code or an HTTP 408 status code or fail to return a Success Code during the selected period.

</td></tr><tr><td>

Memory usage

</td><td>

Installed

</td><td>

Amount of memory or RAM consumed by an application, measured in percentage.

</td></tr></tbody>
</table>## Device metrics

<table id="table_kpp_rlm_ngc"><thead><tr><th>

Metric

</th><th>

Operating system

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Battery health

</td><td>

Windows

 macOS

</td><td>

The battery health of a device typically measured using metrics such as battery capacity, cycle count, and impedance.

</td></tr><tr><td>

CPU usage

</td><td>

Windows

 macOS

</td><td>

The percentage of processing power consumed by the device.

</td></tr><tr><td>

Disk usage

</td><td>

Windows

 macOS

</td><td>

The proportion of the device's disk storage capacity consumed by data and applications.

</td></tr><tr><td>

Memory usage

</td><td>

Windows

 macOS

</td><td>

The amount of memory or RAM consumed by the device.

</td></tr><tr><td>

Wifi receive rate

</td><td>

Windows

 macOS

</td><td>

The speed at which a device receives data from the network.

</td></tr><tr><td>

Wifi RSSI

</td><td>

macOS

</td><td>

WiFi Received Signal Strength Indicator \(RSSI\) measures the strength of wireless signal received by a device. RSSI value is higher when close to 0. Lower negative values mean a weaker connection.

</td></tr><tr><td>

Wifi transmit rate

</td><td>

Windows

 macOS

</td><td>

The speed at which a device sends data to the network.

</td></tr></tbody>
</table>## User sentiment metric

The user sentiment metric is calculated based on survey ratings collected from application and device users. Users rate their experiences in the range of 1-5. These ratings are then normalized on a scale of 0-100 based on weightage defined in the survey calculation table. For more information, see [DEX Score normalization for metric scores](dexscr-dex-score-normalization.md).

You can configure the DEX Score survey configuration to identify the recipients, methods, and timing for sending surveys. For more information, see [Update DEX Score survey configuration](../task/dexscr-set-survey-config.md).

|Metric|Description|
|------|-----------|
|Application survey|Application surveys are sent periodically to randomly selected users based on application usage.|
|Device survey|Device surveys are sent to users every six months.|

## Service desk metrics

<table id="table_z5j_shl_bgc"><thead><tr><th>

Metric

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Customer satisfaction scores for incident resolved

</td><td>

The score for customer satisfaction surveys sent to users for resolved incidents. Scores are calculated only for those surveys that have been successfully submitted by users.Normalized values for surveys are considered and surveys with normalized values greater than zero are assigned weights on a scale of 0–100. For more information, see [Normalized value for an assessment](https://www.servicenow.com/docs/access?context=example-normalized-value-calc&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

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

