---
title: Create SLO form
description: Learn about the available fields for adding a service level objective \(SLO\) to Service Reliability Management.
locale: en-US
release: australia
product: Service Level Objective Management
classification: service-level-objective-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [SLO Management reference, Service Level Objective Management, ITOM AIOps, IT Operations Management]
---

# Create SLO form

Learn about the available fields for adding a service level objective \(SLO\) to Service Reliability Management.

## Service level objective form

The following table describes the available options in the Service level objective form. For step-by-step instructions, see [Create SLOs, SLIs, and error budget policies](../../slo-management/task/sr-create-slo-sli.md).

<table id="id_sdb_v2n_y1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the SLO.

</td></tr><tr><td>

SLI type

</td><td>

-   **Availability**: Percentage of time the service is available.
-   **Errors**: Frequency of service errors.
-   **Latency**: Time taken to service a request.
-   **Saturation**: Fullness of the system, focusing on resource use.

</td></tr><tr><td>

How do you want to measure this objective?

</td><td>

You can measure this objective by:-   **Duration**: The amount of time the service spends without breaching. It's the only value available.
-   **Count**: The number of periods or occurrences in a given compliance period.

</td></tr></tbody>
</table><table id="id_xhm_y2n_y1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Objective \(%\)

</td><td>

The percentage of how available \(uptime\) you want the service to be over a length of time. If measuring by duration, an objective percentage of Five Nines \(99.999%\) means that the service wasn’t available for 26 seconds per month, or about 5 minutes and 35 seconds per year. This is used to calculate your error budget.

</td></tr><tr><td>

Compliance period

</td><td>

Period for which the metrics are calculated. The available options are:-   **Month**: The duration is considered to be the current month. For example, if the current date is 26th January, the duration will be considered from 1st January until 31st January.
-   **Rolling 7 days**: The duration is considered to be 7 days from the current date.
-   **Rolling 30 days**: The duration is considered to be 30 days from the current date. For example, if the current date is 26th January, the duration will be considered from 25th December.
-   **Rolling 90 days**: The duration is considered to be 90 days from the current date. For example, if the current date is 26th January, the duration will be considered from 25th October.

</td></tr><tr><td>

Error budget

</td><td>

Auto-populated. The maximum level of errors \(downtime\) allowed over a certain period. A percentage of total service availability. Once you set your objective \(%\), your error budget is automatically calculated using this formula: 1 – \(Desired\) Availability.

The error budget of a service will be calculated in days, hours, minutes, and seconds for a desired availability of 99.99% \(Four Nines\) of the year by:

1.  Calculating the total time in seconds in a year: 31536000 seconds.
2.  Determining the error budget as 1 – \(Desired\) Availability: 1 - 0.9999 = 0.0001.
3.  Converting the error budget to time units.

For example, if the error budget is 0.0001:

-   Error Budget in Seconds = 0.0001 \* 31,536,000 seconds = 3,153.6 seconds.
-   Error Budget in Minutes = 3,153.6 seconds / 60 = 52.56 minutes.
-   Error Budget in Hours = 52.56/60 = 0.875 hours.
-   Error Budget in Days = 52.56 minutes / \(24 \* 60\) ≈ 0.0364 days.

**Note:** Your error budget appears in units of days, hours, minutes, and seconds only when you measure your SLO by duration.

</td></tr></tbody>
</table><table id="id_hnl_w2n_y1c"><thead><tr><th>

SLO type

</th><th>

Count by periods or Count by occurrences

</th></tr></thead><tbody><tr><td>

Limit occurrences

</td><td>

The number of occurrences after which a breach occurs.Limit occurrences act as an error budget.

</td></tr><tr><td>

Compliance period

</td><td>

Period for which the metrics are calculated. The available options are:-   **Month**: The duration is considered to be the current month. For example, if the current date is 26th January, the duration will be considered from 1st January until 31st January.
-   **Rolling 7 days**: The duration is considered to be 7 days from the current date.
-   **Rolling 30 days**: The duration is considered to be 30 days from the current date. For example, if the current date is 26th January, the duration will be considered from 25th December.
-   **Rolling 90 days**: The duration is considered to be 90 days from the current date. For example, if the current date is 26th January, the duration will be considered from 25th October.

</td></tr></tbody>
</table>**Note:** The **Assignment group** is auto-populated.

**Parent Topic:**[SLO Management reference](../../slo-management/reference/service-level-objective-management-reference.md)

