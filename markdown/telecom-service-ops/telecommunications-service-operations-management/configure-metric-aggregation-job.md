---
title: Configure a metric aggregation job
description: Configure a scheduled job to aggregate raw metrics into a calculated metric on a parent or anchor configuration item \(CI\). Aggregated metrics let you view performance data at a higher level of the network.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/configure-metric-aggregation-job.html
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 3
keywords: [configure metric aggregation job, scheduled job, metric aggregation, TSOM]
breadcrumb: [Configure Telecom Assurance, Configure, Telecommunications Service Operations Management]
---

# Configure a metric aggregation job

Configure a scheduled job to aggregate raw metrics into a calculated metric on a parent or anchor configuration item \(CI\). Aggregated metrics let you view performance data at a higher level of the network.

## Before you begin

A pull connector must be configured and collecting metrics for the source resources to aggregate.

Role required: tsom\_assurance\_admin

## About this task

Each scheduled job handles one aggregation. The job script defines the source data, aggregation method, and result destination.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Select **New**.

3.  Select **Automatically run a script of your choosing**.

4.  In the **Name** field, enter a meaningful name for the aggregation.

5.  Set the run schedule for the job.

    For example, to run the aggregation periodically, set **Run** to **Periodically**, set the repeat interval, and set the start date and time.

6.  In the **Script** field, enter the script that runs the aggregation.

    The script calls the metric aggregation scripted extension point and passes a configuration object that defines the aggregation. The following example aggregates a per-cell metric into an average value on each Baseband Unit.

    ```
    var impls = new GlideScriptedExtensionPoint()
        .getExtensions('sn_tsom_em_conns.TSOMMetricAggregatorSEP');
    
    if (!impls || !impls.length) {
        gs.warn('TSOMMetricAggregator: No implementations registered for TSOMMetricAggregatorSEP');
    } else {
        impls[0].aggregate({
            mode: 'hierarchy',
            targetCIClass: 'cmdb_ci_baseband_unit',
            sourceCIClass: 'cmdb_ci_mobile_cell',
            sourceMetric: 'NR_5076b',
            aggregate: 'avg',
            calculatedMetricName: 'NR_5076b_avg_bbu',
            unit: 'Mbps',
            level: 4
        });
    }
    ```

    For a flat, range-based aggregation, set the mode to flat, identify the source resources by range, and optionally apply field filters. Provide the anchor CI that holds the result, as shown in the following example.

    ```
    var impls = new GlideScriptedExtensionPoint()
        .getExtensions('sn_tsom_em_conns.TSOMMetricAggregatorSEP');
    
    if (!impls || !impls.length) {
        gs.warn('TSOMMetricAggregator: No implementations registered for TSOMMetricAggregatorSEP');
    } else {
        impls[0].aggregate({
            mode: 'flat',
            sourceCIClass: 'cmdb_ci_sim',
            rangeStart: 'SIM010',
            rangeEnd: 'SIM050',
            filters: [
                { field: 'operational_status', operator: '=', value: '1' }
            ],
            sourceMetric: 'sim_throughput',
            aggregate: 'avg',
            calculatedMetricName: 'sim_throughput_avg_global',
            anchorCiSysId: '<sys_id>',
            unit: 'Mbps'
        });
    }
    ```

    To roll up only a subset of source CIs into a parent CI, use hierarchy mode. Narrow the source resources by range and field filters, as shown in the following example. This example averages a metric across a range of SIM cards with an active operational status. The result is published to the parent mobile private network \(MPN\) service.

    ```
    var impls = new GlideScriptedExtensionPoint()
        .getExtensions('sn_tsom_em_conns.TSOMMetricAggregatorSEP');
    
    if (impls && impls.length) {
        impls[0].aggregate({
            mode: 'hierarchy',
            targetCIClass: 'cmdb_ci_network_service_instance',
            sourceCIClass: 'cmdb_ci_sim_card',
            rangeStart: 'PLMN-PLMN/SST-1/SD-000011',
            rangeEnd: 'PLMN-PLMN/SST-1/SD-000015',
            filters: [
                { field: 'operational_status', operator: '=', value: '1' }
            ],
            sourceMetric: 'NR_5076b',
            aggregate: 'avg',
            calculatedMetricName: 'NR_5076b_avg_11_to_15_per_MPN_Service',
            unit: 'Mbps',
            level: 4
        });
    }
    ```

    To reference the scripted extension point by its fully qualified scoped name and log a warning when no implementation is registered, use the following pattern.

    ```
    var impls = new GlideScriptedExtensionPoint()
        .getExtensions('sn_tsom_em_conns.TSOMMetricAggregatorSEP');
    
    if (!impls || !impls.length) {
        gs.warn('TSOMMetricAggregator: No implementations registered for TSOMMetricAggregatorSEP');
    } else {
        impls[0].aggregate({
            mode: 'hierarchy',
            targetCIClass: 'cmdb_ci_network_service_instance',
            sourceCIClass: 'cmdb_ci_sim_card',
            rangeStart: 'PLMN-PLMN/SST-1/SD-000011',
            rangeEnd: 'PLMN-PLMN/SST-1/SD-000015',
            filters: [
                { field: 'operational_status', operator: '=', value: '1' }
            ],
            sourceMetric: 'NR_5076b',
            aggregate: 'avg',
            calculatedMetricName: 'NR_5076b_avg_11_to_15_per_MPN_Service',
            unit: 'Mbps',
            level: 4
        });
    }
    ```

7.  Select **Submit**.

    **Note:** For a description of each configuration value, see [Metric aggregation configuration reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/metric-aggregation-configuration-reference.md).


## Result

The scheduled job runs on the defined schedule. Each run produces the calculated metric and raises an event to bind the metric to a CI. After the metric-to-CI binding completes, the calculated metric is stored in the metric base and is available to view in the Insight Explorer.

**Parent Topic:**[Configure Telecom Assurance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/set-up-fault-management.md)

**Related topics**  


[Metric aggregation modes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/metric-aggregation-modes.md)

[Create a custom metric aggregation implementation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/create-custom-metric-aggregation-implementation.md)

[Metric-to-CI binding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/metric-to-ci-binding-tsom-sgc.md)

