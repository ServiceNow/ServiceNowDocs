---
title: Configure KPIs in Digital Portfolio Management with service availability example
description: Configure key performance indicators \(KPIs\) in Digital Portfolio Management \(DPM\) to surface performance information in the context of your solutions. This procedure uses the example of configuring service availability to display the availability score in the Run life-cycle phase.
locale: en-US
release: xanadu
product: Digital Portfolio Management
classification: digital-portfolio-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Configure KPI groups in Digital Portfolio Management, Configuring Digital Portfolio Management, Digital Portfolio Management, IT Service Management]
---

# Configure KPIs in Digital Portfolio Management with service availability example

Configure key performance indicators \(KPIs\) in Digital Portfolio Management \(DPM\) to surface performance information in the context of your solutions. This procedure uses the example of configuring service availability to display the availability score in the Run life-cycle phase.

## Before you begin

-   Plugins required: sn\_team\_perf\_kpi\_group and com.snc.service\_portfolio
-   Role required: sn\_dpm.dpm\_admin

## About this task

As a user with the sn\_dpm.dpm\_admin role, you can configure KPIs to display in DPM. This task uses the Outage and Availability KPI group to show how to configure the service availability KPI.

**Note:** You must have Service Portfolio Management premium subscription to perform this task. This premium subscription automatically installs if you have DPM installed.

For general information about KPI groups, see [KPI groups in Digital Portfolio Management](../concept/dpm-configure-kpi.md).

To create KPI groups, see [Create KPI groups, mappings, and visualizations](dpm-create-kpi-groups.md).

This procedure includes the following tasks:

1.  Create the KPI group mapping.
2.  Create the service commitment.
3.  Associate the service commitment to the service offering.
4.  Create an outage for the service offering.
5.  Run the data collection job and verify.
6.  Ensure that the KPI displays in DPM.

## Procedure

1.  Create the KPI group mapping.

    The mapping you create sets up the service offering that you want to view availability.

    1.  Navigate to **Digital Portfolio Management Workspace** &gt; **KPI Group Mappings**.
    2.  Select **New**.
    3.  On the form, fill in the fields.

<table id="table_n3z_2v5_2sb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

KPI Group

</td><td>

KPI group name to add the mapping. For this example, map to the Outage and Availability KPI group. This mapping may already be done as part of the base DPM system.

</td></tr><tr><td>

-   Service portfolio
-   Taxonomy node
-   Service
-   Offering
-   Application service


</td><td>

Mapping that you want to associate with this KPI group. The fields that are displayed depend on the type of KPI group that you selected. For this example, the mapping is **Offering**.

</td></tr></tbody>
</table>    4.  Select **Submit**.
2.  Create the service commitment.

    For this example, select a service portfolio that you want to configure the service availability KPI. You can select a personal portfolio or an enterprise portfolio.

    1.  Navigate to **All** &gt; **Service Portfolio Management** &gt; **Commitments**.
    2.  Select **New** to set up availability data.
    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Commitment name.|
        |Type|Type of commitment. The **Availability** type sets up availability data.|
        |Percentage available|Percentage that the commitment is available. For example, 90%.|
        |Schedule|Duration that the commitment is available. For example, 24 x 7 sets the commitment for every day.|
        |Time zone|Time zone for the commitment.|
        |Description|Description of the commitment.|

    4.  Select **Submit**.
3.  Associate the service commitment to the service offering.

    1.  Navigate to **All** &gt; **Service Portfolio Management** &gt; **Service commitment**.

        **Note:** If the plugin is not installed, then enter the table name in the filter navigator: **service\_offering\_commitment.list**, and then press **Enter**.

    2.  Select **New**.
    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Service offering|The service offering associated with the service commitment.|
        |Service commitment|The service commitment associated to the service offering.|

    4.  Select **Submit**.
4.  Create an outage for the service offering.

    Set the service availability for the past seven days prior to creating the outage record.

    1.  Navigate to **All** &gt; **Service Portfolio Management** &gt; **Outages**.
    2.  Select **New**.
    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Number|System-generated number for the outage record.|
        |Configuration Item|The service offering associated with the outage.|
        |Begin|The start date of the outage.|
        |End|The end date of the outage.|

    4.  Select **Submit**.

        **Note:** The outage that you create for the service offering also generates a service availability record for the service offering.

5.  Run the data collection job and verify.

    The job collects data from all Performance Analytics indicators on the scheduled jobs list. This step also provides you with verification steps to ensure that the job ran successfully.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.
    2.  In the Name column, search for **SPM Data Collection job for PA**.
    3.  Select **edit**.
    4.  Ensure that the **Relative start** is set to the number of days to collect data \(default is **1**\).
    5.  Select **Execute now**.
    6.  Refresh the screen to see your job log on the **Job Logs** tab. Review the created date and ensure that the **State** is **Collected**.
    7.  Open the **Indicators** tab and under the Name column, search for the **SPM Availability** indicator.
    8.  Select **SPM Availability**, and then select **edit**.
    9.  On the form, open the SPM Availability indicator record to verify that you created the job successfully.
    10. Select the **Show Analytics Hub** related link to verify that the availability score is displayed for the offering. If several values are displayed, then search for the offering name to verify that you set the availability score properly for that offering.
6.  Ensure that the KPI is displayed in DPM.

    1.  Navigate to **Workspace** &gt; **Digital Portfolio Management**.
    2.  Find the service portfolio that has the availability KPI that you created.
        -   If you created the availability KPI for a personal portfolio, then open the personal portfolio card that has the availability KPI.
        -   If you created the availability KPI for an enterprise portfolio, then use the enterprise portfolio tree structure to find the service offering record.
    3.  On the **Run** tab, ensure that the Performance snapshot Availability card displays the correct percentage value.

**Parent Topic:**[Configure KPI groups in Digital Portfolio Management](../concept/dpm-configure-kpi-groups.md)

**Related topics**  


[Create KPI groups and mappings in Digital Portfolio Management](dpm-create-kpi-groups.md)

