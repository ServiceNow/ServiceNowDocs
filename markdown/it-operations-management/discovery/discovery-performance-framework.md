---
title: Discovery performance metrics
description: This Discovery enhancement collects performance metrics on probe/pattern and sensor processing times and then aggregates that data over time. You can use the roll-up data to monitor the performance of specific discoveries or to compare performance between versions after an upgrade. By default, Discovery tracks the performance of individual probes, sensors, and patterns by measuring the processing time. When patterns are used, Discovery measures the Identification and Reconciliation Engine \(IRE\) processing time. Use the roll-up by build data to ensure that the processing times for Discovery components remain consistent for discoveries in a 24 hour period. View aggregate build data before and after an upgrade to compare the performance of the old and new versions. All aggregated performance data is read-only.Use the roll-up by status data to ensure that the processing times for probes/patterns and sensors remain consistent for a specific Discovery. All aggregated performance data is read-only.Use the roll-up by target data to ensure that the processing times for probes/patterns and sensors remain consistent for each Discovery of a specific IP address. All aggregated performance data is read-only.Discovery performance metrics can accumulate data for probes, patterns, and sensors each time Discovery runs. Discovery calculates processing times and increments the number of times a component runs for each roll-up profile: status, target, or build. All aggregated performance data is read-only.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 10
breadcrumb: [Discovery monitoring and issue resolution, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery performance metrics

This Discovery enhancement collects performance metrics on probe/pattern and sensor processing times and then aggregates that data over time. You can use the roll-up data to monitor the performance of specific discoveries or to compare performance between versions after an upgrade.

## Metrics

Discovery provides these individual performance metrics:

-   Probe and pattern processing time.
-   Sensor processing time.
-   Identification and Reconciliation Engine \(IRE\) processing time for Discovery patterns. This processing time is already included in the sensor processing time, but is isolated here to provided more insight into the identification and reconciliation of pattern payloads.

Discovery can aggregate individual metrics for these attributes:

-   Builds/versions
-   Discovery status
-   Target IP address

## How metric aggregations are triggered

Metric roll-ups are initiated as follows:

-   **Aggregated by build**: Implemented by the **Aggregate Discovery Probe And Sensor Metrics By Build** scheduled job. This job runs at 0200, local time.
-   **Aggregated by status**: Implemented by the **Rollup Probe/Sensor Metrics by Status** Script Action, which is triggered by the **discovery.complete** or **discovery.cancelled** registered events.
-   **Aggregated by target**: Implemented by the **Rollup Probe/Sensor Metrics by Target** Script Action that is triggered by the **discovery.device.complete** registered event.

**Note:** If Discovery execution is cancelled before it completes, Discovery cannot update the IP target metric aggregation table. This is because the **discovery.device.complete** event that triggers aggregation does not run. IP target data for an interrupted Discovery is collected when subsequent discoveries run successfully on the target. Cancelling Discovery execution does not affect the aggregation of other metrics, which are triggered differently.

## Tables

Discovery performance metrics data is stored in these tables:

|Table|Description|
|-----|-----------|
|Probe and Sensor Metrics \(Individual\) \[discovery\_perf\_metric\_probe\_sensor\]|Stores the individual performance metrics for probes/patterns, sensors, and IRE processing times.|
|Probe and Sensor Metrics \(Aggregate\) \[discovery\_perf\_metric\_probe\_sensor\_rollup\]|This is the base table for the metric aggregations and does not store data itself. The three roll-up tables, by-build, by-status, and by-target all extend this table.|
|Probe and Sensor Metrics \(Aggregated by Build\) \[discovery\_perf\_metric\_probe\_sensor\_rollup\_by\_build\]|Stores the aggregated performance metrics for probes/patterns, sensors, and IRE by build and version.|
|Probe and Sensor Metrics \(Aggregated by Status\) \[discovery\_perf\_metric\_probe\_sensor\_rollup\_by\_status\]|Stores the aggregated performance metrics for probes/patterns, sensors, and IRE by Discovery status.|
|Probe and Sensor Metrics \(Aggregated by Target\) \[discovery\_perf\_metric\_probe\_sensor\_rollup\_by\_target\]|Stores the aggregated performance metrics for probes/patterns, sensors, and IRE by IP address.|

## Discovery properties

Performance metrics properties control whether or not aggregation occurs, but not what data is included in the aggregation. Status and IP target data is collected as follows:

-   Rollups for status always contain new data. Discovery continuously collects data on all probes and sensors during the discovery execution for that discovery status and stores it in the Probe and Sensor Metrics \(Individual\) \[discovery\_perf\_metric\_probe\_sensor\] table. Aggregation rolls up all probe and sensor data for that particular status after **discovery.cancel** and **discovery.complete** events are fired for that status, but only if the aggregation property for status roll-ups is enabled.
-   Discovery continuously collects data on IP targets and stores it in the Probe and Sensor Metrics \(Individual\) \[discovery\_perf\_metric\_probe\_sensor\] table. Aggregation rolls up all existing IP target data after the **glide.discovery.perf.metrics.rollup\_by\_target** property is enabled and creates records in the Probe and Sensor Metrics \(Aggregated by Target\) \[discovery\_perf\_metric\_probe\_sensor\_rollup\_by\_target\] table.

These properties control the gathering of probe and sensor metrics:

<table id="table_hq4_lwt_kfb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.discovery.perf.metrics.enable\_collection

</td><td>

Enables collection of performance metrics.-   **Type**: true \| false
-   **Default**: true

</td></tr><tr><td>

glide.discovery.perf.metrics.rollup\_by\_build

</td><td>

Enables aggregation of individual discovery performance metrics into a roll-up table that groups by build.-   **Type**: true \| false
-   **Default**: true

</td></tr><tr><td>

glide.discovery.perf.metrics.rollup\_by\_status

</td><td>

Enables aggregation of individual discovery performance metrics into a roll-up table that groups by discovery status.-   **Type**: true \| false
-   **Default**: false

</td></tr><tr><td>

glide.discovery.perf.metrics.rollup\_by\_target

</td><td>

Enables aggregation of individual discovery performance metrics into a roll-up table that groups by target IP address. By default, Discovery continuously collects individual IP address metrics, even when aggregation by target IP is disabled. When you enable IP target aggregation, Discovery includes all target metrics in the roll-up table.-   **Type**: true \| false
-   **Default**: false

</td></tr></tbody>
</table>## View Discovery performance metrics for probes, sensors, and patterns

By default, Discovery tracks the performance of individual probes, sensors, and patterns by measuring the processing time. When patterns are used, Discovery measures the Identification and Reconciliation Engine \(IRE\) processing time.

### Before you begin

Role required: discovery\_admin or admin

### Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Discovery Performance Metrics** &gt; **Probe/Sensor \(Individual\)**.

2.  Sort the list by Discovery status to see the list of probes and patterns that ran in a specific Discovery.

3.  You can view the metrics for each probe, sensor, or pattern in the list or open the record.

    All probe and sensor metrics data are read-only.

    ![Individual probe and sensor metrics](../image/DiscoPerformanceMetricProbe.png)

    The Probe and Sensor Metrics \(Individual\) form provides these fields:

    |Field label|Field name|Description|
    |-----------|----------|-----------|
    |Build/version|build\_version|Build on which the Discovery was run.|
    |Discovery status|discovery\_status|ID number of the Discovery status from which the metrics were collected.|
    |Target IP address|target\_ip|IP address of the target for this Discovery.|
    |ECC queue input|ecc\_queue\_input|Identifies a particular ECC input record in the ECC queue table.|
    |ECC queue topic \*|ecc\_queue\_topic|Identifies the Java class in the MID Server that executes the probe.|
    |ECC queue name \*|ecc\_queue\_name|Identifies the probe/pattern evaluated for performance in this aggregation.|
    |Probe \*|probe|Name of the probe used for this Discovery.|
    |Probe processing time|probe\_time|Interaction time of the MID Server with the target, including construction of the payload that is sent back to the instance. The time is in milliseconds.|
    |IRE processing time|ire\_time|Time required to process the pattern payload on the instance by the Identification and Reconciliation Engine \(IRE\). IRE time is useful because it shows the part of the sensor time used by the pattern. The time is in milliseconds.|
    |Sensor processing time|sensor\_time|Time it took the sensor to process the payload on the instance for a Discovery. The time is in milliseconds.|

    \* Used to uniquely identify a probe/pattern and accompanying sensor when gathering metrics for a Discovery.


## View Discovery performance metrics aggregated by build

Use the roll-up by build data to ensure that the processing times for Discovery components remain consistent for discoveries in a 24 hour period. View aggregate build data before and after an upgrade to compare the performance of the old and new versions. All aggregated performance data is read-only.

### Before you begin

Role required: discovery\_admin or admin

### Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Discovery Performance Metrics** &gt; **Probe/Sensor \(Rollup-By-Build\)**.

2.  Sort the list by **Build/version**.

    ![Filtering the list of performance data aggregated by build](../image/DiscoPerformanceBuildFilter.png)

3.  Filter by a specific build to see the aggregated processing times for the probes and patterns that performed a Discovery on that build.

4.  Open a record to see the probe/pattern statistics for the selected build.

    The form displays additional fields not visible on the list. Roll-up calculations are over a 24 hour period, beginning every night at 0200.

5.  See the table of performance aggregation data for descriptions of additional metrics displayed on the form for roll-ups by build.


## View Discovery performance metrics aggregated by status

Use the roll-up by status data to ensure that the processing times for probes/patterns and sensors remain consistent for a specific Discovery. All aggregated performance data is read-only.

### Before you begin

Role required: discovery\_admin or admin

### About this task

### Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Discovery Performance Metrics** &gt; **Probe/Sensor \(Rollup-By-Status\)**.

2.  Sort the list by **Discovery status** to see the aggregated processing times for the probes and patterns that ran during a specific Discovery.

    ![Filtering the list of performance data aggregated by status](../image/DiscoPerformanceStatusFilter.png)

3.  Filter by a specific status to display metrics available for probes and patterns that ran in that status.

4.  Open a record to see the probe/pattern statistics for the selected status.

    The form displays additional fields not visible on the list. Roll-ups are only created for a completed or cancelled status.

5.  See the table of performance aggregation data for descriptions of additional metrics displayed on the form for roll-ups by status.


## View Discovery performance metrics aggregated by IP address

Use the roll-up by target data to ensure that the processing times for probes/patterns and sensors remain consistent for each Discovery of a specific IP address. All aggregated performance data is read-only.

### Before you begin

Role required: discovery\_admin or admin

### Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Discovery Performance Metrics** &gt; **Probe/Sensor \(Rollup-By-Target\)**.

2.  Sort the list by **Target IP address**.

    ![Filtering the list of performance data aggregated by target IP address](../image/DiscoPerformanceTargetFilter.png)

3.  Filter by a specific IP address to see the aggregated processing times for the probes and patterns that performed the Discovery of that IP address.

4.  Open a record to see the statistics about the selected probe/pattern for the specific IP address.

    The form displays additional fields not visible on the list. Roll-ups are performed after IP Discovery has completed successfully.

5.  See the table of performance aggregation data for descriptions of additional metrics displayed on the form for roll-ups by target.


## Aggregated data for Discovery performance metrics

Discovery performance metrics can accumulate data for probes, patterns, and sensors each time Discovery runs. Discovery calculates processing times and increments the number of times a component runs for each roll-up profile: status, target, or build. All aggregated performance data is read-only.

### Sample roll-up form

This is an example of an aggregation record for probe and sensor metrics. The metrics fields shown here are used for each aggregation.

![Sample roll-up by Status form](../image/PerfFrameworkStatusRollup.png "Sample roll-up by Status form")

### Performance Framework aggregated data

Except where noted, these fields are common to all aggregation records.

<table id="table_kxl_yd2_mfb"><thead><tr><th>

Field label

</th><th>

Field name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Build/version

</td><td>

build\_version

</td><td>

Name of the build running on the instance. This name identifies the version, patch level, and release date of the ServiceNow platform.

</td></tr><tr><td>

Discovery status

</td><td>

discovery\_status

</td><td>

ID number of the Discovery status record for this aggregation. **Note:** This field only appears on the form for roll-ups by status.

</td></tr><tr><td>

Target IP address

</td><td>

target\_ip\_address

</td><td>

IP address of the target for this Discovery.**Note:** This field only appears on the form for roll-ups by target.

</td></tr><tr><td>

Aggregation cutoff

</td><td>

aggregation\_cutoff

</td><td>

The cutoff time varies, depending on the roll-up profile. -   **By-build**: Occurs daily at 02:00, by default.
-   **By-status**: Closing time of the last aggregation for that Discovery status, which might have run the last time **discovery.complete** or **discovery.cancelled** ran for that status.
-   **By-target**: Closing time of the last aggregation for that target IP address, which might have run the last time **discovery.device.complete** ran for that IP address.

</td></tr><tr><td>

ECC queue topic \*

</td><td>

ecc\_queue\_topic

</td><td>

Identifies the Java class in the MID Server that executes the probe.

</td></tr><tr><td>

ECC queue name \*

</td><td>

ecc\_queue\_name

</td><td>

Identifies the probe/pattern evaluated for performance in this aggregation.

</td></tr><tr><td>

Probe \*

</td><td>

probe

</td><td>

Name of the probe used for this Discovery.

</td></tr><tr><td>

Probe time \(count\)

</td><td>

probe\_time\_count

</td><td>

Number of times a probe ran for a given roll-up profile.

</td></tr><tr><td>

Probe time \(average\)

</td><td>

probe\_time\_average

</td><td>

Average time a probe took to gather data on the target and format the payload for a given roll-up profile.

</td></tr><tr><td>

Probe time \(minimum\)

</td><td>

probe\_time\_min

</td><td>

Minimum time a probe took to gather data on the target and format the payload for a given roll-up profile.

</td></tr><tr><td>

Probe time \(maximum\)

</td><td>

probe\_time\_max

</td><td>

Maximum time a probe took to gather data on the target and format the payload for a given roll-up profile.

</td></tr><tr><td>

Probe time \(total\)

</td><td>

probe\_time\_total

</td><td>

Total time used by a probe to gather data on the target and format the payload for a given roll-up profile.

</td></tr><tr><td>

Sensor time \(count\)

</td><td>

sensor\_time\_count

</td><td>

Number of times a sensor processed payloads for a given roll-up profile.

</td></tr><tr><td>

Sensor time \(average\)

</td><td>

sensor\_time\_average

</td><td>

Average time a sensor took to process payloads on the instance for a given roll-up profile.

</td></tr><tr><td>

Sensor time \(minimum\)

</td><td>

sensor\_time\_min

</td><td>

Minimum time a sensor took to process a payload on the instance for a given roll-up profile.

</td></tr><tr><td>

Sensor time \(maximum\)

</td><td>

sensor\_time\_max

</td><td>

Maximum time a sensor took to process a payload on the instance for a given roll-up profile.

</td></tr><tr><td>

Sensor time \(total\)

</td><td>

sensor\_time\_total

</td><td>

Total time used by a sensor to process payloads on the instance for a given roll-up profile.

</td></tr><tr><td>

IRE time \(count\)

</td><td>

ire\_time\_count

</td><td>

Number of times a pattern's payload was processed by the Identification and Reconciliation Engine \(IRE\) for a given roll-up profile.

</td></tr><tr><td>

IRE time \(average\)

</td><td>

ire\_time\_average

</td><td>

Average time used for IRE processing of a pattern's payload for a given roll-up profile.

</td></tr><tr><td>

IRE time \(minimum\)

</td><td>

ire\_time\_min

</td><td>

Minimum time used for IRE processing of a pattern's payload for a given roll-up profile.

</td></tr><tr><td>

IRE time \(maximum\)

</td><td>

ire\_time\_max

</td><td>

Maximum time used for IRE processing of a pattern's payload for a given roll-up profile.

</td></tr><tr><td>

IRE time \(total\)

</td><td>

ire\_time\_total

</td><td>

Total time used for IRE processing of a pattern's payload for a given roll-up profile.

</td></tr></tbody>
</table>\* Together, these values uniquely identify a probe/sensor pair \(a "probe execution"\) that is used for a Discovery.

