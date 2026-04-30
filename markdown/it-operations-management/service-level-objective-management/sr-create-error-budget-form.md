---
title: Create Error budget policies form
description: Create an SLO, an SLI, and Error budget policies to help you and your team track your service health and take necessary actions when required.
locale: en-US
release: xanadu
product: Service Level Objective Management
classification: service-level-objective-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [SLO Management reference, Service Level Objective Management, ITOM Health, IT Operations Management]
---

# Create Error budget policies form

Create an SLO, an SLI, and Error budget policies to help you and your team track your service health and take necessary actions when required.

## Error budget policies form

Set up your error budget policies form. For more information, see [Create SLO, SLI, and Error budget policies](../task/sr-create-slo-sli.md).

<table id="table_rqy_bnq_ybc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Threshold for

</td><td>

-   **Burn rate \(count\)**: Percentage rate at which an error budget is consumed.
-   **Error budget remaining \(%\)**: Percentage of error budget left to spend for the specified period.

**Note:** **Burn rate** and **Error budget remaining** values support up to 4 decimal places and then round up.

You can add multiple thresholds for a policy. But you can't add duplicate thresholds. If you try adding duplicate thresholds, you see an error message.


</td></tr><tr><td>

Threshold value

</td><td>

-   For **Burn rate**: The Ideal burn rate is 1 or below because it indicates that the error budget is being consumed at an expected pace. The threshold is breached when the burn rate is equal to or greater than the specified value.
-   For **Error budget remaining**: The threshold is breached if the percentage remaining is equal to or less than what is specified.

</td></tr><tr><td>

If threshold is breached then

</td><td>

Action you want to take when a breach occurs.-   Create incident
-   Send an email

</td></tr></tbody>
</table>**Parent Topic:**[SLO Management reference](service-level-objective-management-reference.md)

