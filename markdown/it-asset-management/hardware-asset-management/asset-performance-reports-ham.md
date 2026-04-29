---
title: Asset performance reports in the Hardware Asset Workspace
description: Gain insights into the overall operational efficiency of your organization's hardware assets by using the asset performance reports available in the Asset analytics view.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Exploring Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Asset performance reports in the Hardware Asset Workspace

Gain insights into the overall operational efficiency of your organization's hardware assets by using the asset performance reports available in the Asset analytics view.

Asset performance involves assessing how effectively and efficiently assets fulfill their intended functions within an organization. The evaluation includes measuring and analyzing key performance indicators \(KPIs\), such as:

-   Asset availability to determine when the asset is operational
-   Mean time between failures \(MTBF\) to measure reliability
-   Mean time to repair \(MTTR\) to measure repair efficiency
-   Total asset task time summary to measure the total time worked on the related tasks for an asset and its child assets.

## Benefits of tracking asset performance

-   **Reduce unplanned downtime**

    Monitoring asset health in real-time help prevent and predict issues before they cause downtime.

-   **Improve maintenance efficiency**

    Metrics like MTTR and MTBF help you schedule maintenance more effectively, reducing wasted time, and improving technician efficiency.

-   **Maximize asset life and return on investment \(ROI\)**

    By detecting early signs of wear and tear and scheduling timely repairs, organizations can make their equipment last longer and delay the need for replacements.

-   **Enhance financial planning**

    Insights into performance help identify models or locations that aren't performing well or have ongoing problems, guiding better investment choices.

-   **Align operations with service levels**

    Tracking availability helps assets meet the required uptime targets set by service level agreements \(SLAs\), compliance standards, or production schedules.


## Considerations, requirements, and limitations

-   Asset key performance indicators \(KPIs\) aren't calculated for pallets, consumable, and bundle assets.
-   Asset KPIs aren't calculated by default.
-   To track the asset KPIs that include Asset availability, MTBF, and MTTR, you must perform the following configurations:
    1.  [Opt in to the model categories of the assets for which you want to monitor the KPIs](../task/opt-in-kpi-tracking-ham.md).

        **Note:** If a model category has child categories, selecting the parent category for performance tracking doesn’t automatically include the child categories. You need to opt in to the specific child categories you want to track.

    2.  Define an operation schedule, which is a collection of schedule entries that specify the operational status and total operational duration for any entity that references the schedule. The schedule entries define calendar hours of operation within a schedule.

        For details, see [Create an operational schedule for hardware assets](../task/create-operational-schedule-ham.md).

        **Note:** If an operational schedule isn't defined, the Default operation schedule is applied.

    3.  [Create an Asset schedule to associate the hardware assets with an operational schedule](../task/create-asset-schedule-ham.md).

        **Note:** If an asset isn't associated with an operational schedule, the Default asset schedule will be applied.

-   The calculation of asset KPIs for hardware assets begins when the asset transitions to the In use state for the first time.
-   KPIs are tracked until the state of the asset changes to Retired or Missing.

## Calculation of asset KPIs

The KPIs are calculated based on the tasks associated with the asset and the operational schedule of the asset. The KPI values are stored in the Asset availability \[sn\_ent\_asset\_availability\] table, which extends the Service Availability table.

Performance tracking for assets that belong to a model category opted in for performance tracking begins when the asset’s state changes to In use for the first time. A record is then created in the Asset Availability table with **Asset availability %** set to **100**. The Asset availability % value decreases when the asset experiences an outage.

-   **Outage record creation**

    An outage record is created in the Outages \[cmdb\_ci\_outage\] table in the following unplanned outage scenarios:

    -   The state of an asset changes from In use to any of the following:
        -   In stock - Pending repair
        -   In stock - Pending disposal
        -   In stock - Defective
    -   An incident is created
    The outage record is closed when:

    -   The status of the asset changes back to In use.
    -   The incident is closed.
    The duration of the outage is calculated when the repair task is closed.

-   **Handling overlapping outages**

    Outages can overlap due to multiple events being logged within the same time window. To maintain accurate KPI calculations, overlaps between unplanned outages are handled with these rules:

    -   When multiple unplanned outages, such as an asset moving from In use to In stock - pending repair state and an incident being created on the same asset, occur during overlapping time periods, they are not treated as separate outages. Instead, they are merged into a single outage to avoid overstating downtime.
    -   The total duration of this combined outage is calculated by merging all overlapping time intervals.
    -   A sample outage calculation is here:
        1.  Outage A: 10:00 AM – 12:00 PM
        2.  Outage B: 11:30 AM – 1:00 PM

            Result: The resulting outage window is 10:00 AM – 1:00 PM \(a single 3-hour outage\).

-   **Passing on outages through the asset hierarchy**

    In an asset hierarchy, outage on assets or their child assets are handled as follows:

    -   If a child asset with the **Required** field set to **true** experiences an outage, its parent asset will also have the outage.
    -   If a parent asset has an outage, all its child assets will also have the outage.

<table id="table_jcy_3k5_wfc"><thead><tr><th>

Asset KPI

</th><th>

Formula

</th></tr></thead><tbody><tr><td>

Asset availability \(in %\)

</td><td>

```
(Operating hours - Total planned downtime - Total unplanned downtime)/(Operating hours - Total planned downtime)
```

</td></tr><tr><td>

Mean time between failures \(MTBF\) \(in hours\)

</td><td>

```
(Operating hours - Total planned downtime - Total unplanned downtime)/(Total unplanned outages)
```

</td></tr><tr><td>

Mean time to repair \(MTTR\) \(in hours\)

</td><td>

```
(Total unplanned downtime)/(Total unplanned outages)
```

</td></tr></tbody>
</table>Definition of the variables used in the KPI calculations is as follows:

<table id="table_drp_cwx_vfc"><thead><tr><th>

Variable

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Operating hours

</td><td>

The duration from when the asset first transitioned to the In use state until the current date and time within the asset schedule.

</td></tr><tr><td>

Planned downtime

</td><td>

The duration from when the asset transitioned from the Work in progress state to the Closed complete state.

</td></tr><tr><td>

Unplanned downtime

</td><td>

The duration from when the asset transitions from the In use state to any repair state, such as In stock - Pending repair, In stock - Pending disposal, or In stock - Defective, until it returns to the In use state, within the asset schedule.If there are overlapping durations between the repair state and an incident on the same asset, the combined duration of both is considered. The asset schedule is also considered when determining the outage duration.

</td></tr><tr><td>

Total unplanned outages

</td><td>

The count of total outage records for an asset. Overlapping and concurrent outages are consolidated as one outage.

</td></tr></tbody>
</table>## Accessing asset KPI reports

-   Contextual sidebar of the asset Form: You can view the following reports by using the options available in the contextual sidebar of the asset form.
    -   [Asset availability and related KPIs report for an individual asset](../task/view-availability-for-hardware-aaset.md).
    -   [Asset task time summary report for all hardware assets](../task/view-total-time-spent-on-asset-ham.md).
-   Asset performance tab on the Asset analytics view: You can view the average values of the KPIs, including Average availability, Average MTTR, and Average MTBF, for all the assets that are being tracked. Additionally, you can see a list of the assets that contributed to the calculation of these KPIs. For details, see [Asset analytics view in the Hardware Asset Workspace](asset-analytics-view.md).

## Scheduled job for calculation of asset KPIs

-   The **Calculate asset performance KPIs** scheduled weekly job runs every Saturday to calculate the KPIs for the assets that belong to the model categories opted in for performance tracking. These KPIs are then reflected in the Asset availability and related KPIs report, which displays the most recent KPI values.

    **Note:** To track historical KPIs for existing assets in the opted-in model categories, run the **Calculate availability for historical data** job. This job considers the following tasks associated with an asset to calculate the outages and KPIs:

    -   RMA task
    -   Repair task
    -   Troubleshoot task
    -   Evaluate task
    -   Recall task
-   The **Asset availability data collection** scheduled weekly job runs every Sunday to calculate the average values of the KPIs that includes Average availability, Average MTTR, and Average MTBF. The job then generates the reports in the Asset performance tab of the Asset analytics view.

