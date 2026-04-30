---
title: View SRM reliability metrics
description: Learn about an existing service level objective \(SLO\) and service level indicator \(SLI\).
locale: en-US
release: zurich
product: Service Level Objective Management
classification: service-level-objective-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Using SLO Management, Service Level Objective Management, ITOM AIOps, IT Operations Management]
---

# View SRM reliability metrics

Learn about an existing service level objective \(SLO\) and service level indicator \(SLI\).

## Before you begin

Role required: srm\_manager, srm\_responder, or srm\_admin

**Note:** Administrators can view any Service Reliability Management \(SRM\) SLO.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the primary navigation, select the **Services** icon \(![Services icon](../image/icon-sr-services.png)\).

3.  Select a service, select the **Reliability metrics** tab, and then open an SLO.

4.  View the SLO header to get key information about the SLO, SLI, and state.

<table id="table_hft_kxd_hhc"><thead><tr><th>

Header element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

SLI type

</td><td>

-   **Availability**: Percentage of time the service is available.
-   **Errors**: Frequency of service errors.
-   **Latency**: Time taken to service a request.
-   **Saturation**: Fullness of the system, focusing on resource use.


</td></tr><tr><td>

SLO type

</td><td>

-   **Duration**: Measures the time that the service spends without breaching. The associated metrics are:
    -   **Objective \(percentage\)**: The target percentage of the SLI that the service is expected to meet.
    -   **Error budget**: The remaining error budget, shown in days and time, before the objective is breached.
-   **Count**: Measures the number of occurrences during a compliance period. The associated metrics are:
    -   **Limit \(occurrences\)**: The number of occurrences that triggers a breach.
    -   **Remaining breach occurrences**: The number of occurrences left before a breach occurs.


</td></tr><tr><td>

State

</td><td>

-   **Draft**: The SLO isn't active yet. You can add new SLIs, update existing ones, or delete the SLO.
-   **Running**: The SLO is active. You can edit, retire, or delete the SLO. Editing a running SLO automatically retires it and creates a new copy. See [Edit a reliability metric](../../slo-management/task/sr-edit-sli-slo.md) for more information.
-   **Retired**: The SLO is no longer active. You can reactivate it if needed.


</td></tr><tr><td>

Service

</td><td>

The service associated with the SLO.

</td></tr><tr><td>

Reliability

</td><td>

-   **Stable**: All SLOs have more than 25% of their error budget remaining.
-   **At risk**: All SLOs have some error budget remaining, but at least one SLO has less than 25% left.
-   **Critical**: At least one SLO has fully used its error budget.


</td></tr></tbody>
</table>    **Note:** From the header, you can delete, retire, or edit the SLO. Deleting an SLO also deletes the associated SLIs. Retiring an SLO changes its state, but you can reactivate it later from the SLO page or the Reliability metrics tab.

5.  Select the **Overview** tab to view summary metrics and performance charts for the SLO.

    -   Historic periods: Select a time range. The available periods span from the SLO creation date to the present in defined increments.
    -   Summary metrics: View details about SLO performance depending on the configured SLIs and error budget policy thresholds.
    -   Service level indicators: View the SLIs associated with the SLO.
    -   Service level objective \(SLO\) history:

        -   For duration SLOs, view charts for error budget used, error budget remaining, and burn rate.
        -   For count SLOs, view charts for cumulative breach occurrences, burn rate, and alerts, incidents &amp; changes impacting this service.
        You can point to the charts to view daily values.

6.  Select the **Details**, **Service level indicators**, and **Error budget policy** tabs to view key configuration details.

    For information about the details shown, see [Create SLO form](../reference/sr-create-slo-sli-form.md), [Create SLI form](../reference/sr-create-sli-form.md), and [Add an error budget policy form](../../slo-management/reference/sr-create-error-budget-form.md). On the Error budget policies tab, you can select **Add policy** to define actions based on performance data.

    The Details tab also includes a Work notes field and Activity panel to record and track changes to the reliability metric.


## What to do next

To learn how to create or edit SLOs, see [Create SLOs, SLIs, and error budget policies](../../slo-management/task/sr-create-slo-sli.md) and [Edit a reliability metric](../../slo-management/task/sr-edit-sli-slo.md).

**Parent Topic:**[Using SLO Management](../../slo-management/task/using-service-level-objective-management.md)

