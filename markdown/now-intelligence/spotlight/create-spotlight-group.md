---
title: Create a Spotlight group
description: Create a Spotlight group to define the records to evaluate. In the Spotlight group, you also set the threshold that the score of a record must exceed to trigger the creation of a Spotlight.When a Spotlight job runs, it either evaluates a snapshot of collected records or it collects and evaluates data directly from the platform.
locale: en-US
release: xanadu
product: Spotlight
classification: spotlight
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Setting up Spotlight, Ranking records with Spotlight, Configure Performance Analytics advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Create a Spotlight group

Create a Spotlight group to define the records to evaluate. In the Spotlight group, you also set the threshold that the score of a record must exceed to trigger the creation of a Spotlight.

## Before you begin

An administrator must have activated the Spotlight plugin.

Role required: pa\_spotlight or admin

## About this task

Spotlight groups specify a set of records to evaluate and a threshold. If the score of a record in the data set exceeds the threshold, a spotlight is created for that record. The score of a record is the total weight from all applicable spotlight criteria in the spotlight group.

The set of records to evaluate must be associated with a Performance Analytics indicator. The Spotlight group specifies this indicator. A Spotlight group can reference only one facts table: both the main indicator and all Spotlight criteria for the group must refer to the same table.

**Note:** You can change the main indicator of an existing Spotlight group. However, after you select criteria for the group, you can change the main indicator only to another indicator that uses the same facts table.

If you have domain separation enabled, you create the Spotlight group in whichever domain you are logged in to when you create it. After you configure the Spotlight group, you can copy it to multiple domains, as described in [Copy a Spotlight group to domains](copy-spotlight-group-domain.md).

**Warning:** If you create a Spotlight group in the Global domain, every domain has access to the group.

## Procedure

1.  Navigate to **All** &gt; **Spotlight** &gt; **Spotlight Groups** and click **New**.

2.  Fill in the fields:

<table id="table_h1m_1sb_r2b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Threshold

</td><td>

The sum of the weights of the Spotlight criteria that a record must meet to trigger the creation of a Spotlight.Consider revisiting this value when you assign weights to Spotlight criteria.

</td></tr><tr><td>

Main Indicator

</td><td>

The indicator that collects the records that you want this Spotlight group to evaluate.The main indicator must meet the following requirements:

-   It must be an [automated indicator](../concept/performance-analytics-glossary.md#).
-   The collect\_records property of the indicator must be set to true. This property is set in the Source tab of the indicator form.
-   The indicator source for the indicator must refer to an actual table, not a database view.
 All criteria for evaluating this Spotlight group use the same facts table as the indicator source of the main indicator.

</td></tr></tbody>
</table>3.  To filter the records to evaluate, select a **Breakdown** and an **Element**.

    **Important:** Spotlight group creation respects the Access Control List \(ACL\) on the breakdown source table. Therefore, depending on the ACL, you may not see all existing elements of a breakdown, even with an admin role.

    After you complete the Spotlight group, you can copy the completed Spotlight group to other elements in the same breakdown. Click **Copy Spotlight group for breakdown**. For more information, see [Copy a Spotlight group to breakdown elements](copy-spotlight-group-element.md).

4.  In the **Evaluate scores from** field, select whether the Spotlight job evaluates scores from a snapshot or from the platform.

    |Option|Description|
    |------|-----------|
    |**Performance Analytics snapshot**|A snapshot of records from when the relevant Performance Analytics [data collection jobs](../concept/performance-analytics-glossary.md#) last ran.|
    |**Platform data**|Data from the platform at the time that the Spotlight job runs.|

    For more information, see [Evaluating a snapshot or platform data](create-spotlight-group.md#).

5.  In the context menu, select **Save**.


## Result

You have created a Spotlight group with an indicator and a threshold, and you have defined whether to collect scores based on a snapshot or on platform data.

## What to do next

-   Create Spotlight criteria for the Spotlight group and set the schedule for collecting Spotlight scores. See [Create Spotlight criteria](create-spotlight-criteria.md).
-   If you are using domain separation, the Spotlight group is created in the domain that you are in when you create the group. After you complete configuring the Spotlight group, including criteria and scheduling, you can copy the Spotlight group to another domain by clicking **Copy to domain**.
-   If you have specified a breakdown and element for the main indicator, you can copy the Spotlight group to other elements in the same breakdown. To do so, click **Copy Spotlight group for breakdown**. First complete the Spotlight group, including criteria and scheduling.

**Note:** If you copy a Spotlight group to other domains or other breakdown elements, no Spotlight job results that were already generated for the original Spotlight group are copied.

**Parent Topic:**[Setting up Spotlight](../concept/setting-up-spotlight.md)

**Related topics**  


[Domain separation with Spotlight](../concept/domain-separation-spotlight.md)

[Spotlight interactive analysis](../concept/spotlight-interactive-analysis.md)

[Performance Analytics indicators](../concept/c_Indicators.md)

[Collecting indicator scores](../concept/c_ClctData.md)

## Evaluating a snapshot or platform data

When a Spotlight job runs, it either evaluates a snapshot of collected records or it collects and evaluates data directly from the platform.

**Note:** New Spotlight scores overwrite previous scores, regardless of whether the scores are from a snapshot or from platform data.

### Evaluating snapshot records

By default, a new Spotlight group uses a snapshot of records. Snapshots are the lists of records \(sys\_ids\) that are collected at the time that the scores for those records are collected. A snapshot is made only for automated indicators with **Collect records** selected. The Performance Analytics [data collection jobs](../concept/performance-analytics-glossary.md#) for the main indicator and the criteria indicators of the Spotlight group create the snapshots. These jobs must run, collecting records, before the Spotlight evaluation job runs.

For a Spotlight group to use snapshot records, the data collection and Spotlight evaluation jobs must meet the following conditions:

-   The main indicator and all the indicators used in the criteria of the Spotlight group have record collection enabled.

    **Note:** The **Collect Records** option on the Indicator form enables record collection, as described in [Create an automated indicator](t_CreateAnAutomatedIndicator.md#).

-   The main indicator and all the indicators used in the criteria of the Spotlight group have the same data collection frequency.
-   The data collection jobs for all the Spotlight group indicators run as closely together as possible, to keep the data synchronized. The snapshots of the criteria indicators must have the same date as the last score date of the main indicator. Ideally, the main indicator and all the criteria indicators are in the same data collection job.
-   The Spotlight score collection job runs at the same frequency as the data collection jobs, and as soon as possible after those jobs complete. Scheduling Spotlight score collection in this way ensures that the results are up-to-date and meaningful.

**Note:** Only indicator-based Spotlight criteria evaluate snapshot records. Query-based criteria always evaluate platform data, even if you set the group to evaluate data from a snapshot.

### Evaluating platform data

Spotlight can collect and evaluate records directly from the platform at the time that the Spotlight job runs. The resulting Spotlight scores reflect the state of the platform at the time of the latest Spotlight job.

Spotlight scores based on platform data are not truly in "real time." A record may change in the platform, but the Spotlight score of the record will not reflect this change until the next time a Spotlight job runs.

Evaluating platform data requires more system resources to query the indicator data than evaluating records from a snapshot does.

Also, indicator-based criteria cannot be used to evaluate platform data when scripted breakdowns are applied. The specific restrictions are:

-   If the indicator of a criterion uses a breakdown that is based on a script, this specific criterion cannot be used. Either collect snapshot instead of platform data or create query-based criteria in place of indicator-based criteria.
-   If the main indicator of the Spotlight group uses a breakdown that is based on a script, you cannot evaluate platform data. Configure the Spotlight group to collect data based on snapshots only.

