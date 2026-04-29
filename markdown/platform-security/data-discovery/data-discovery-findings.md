---
title: Data Discovery job results
description: The Data Discovery Findings page shows details on the data found by a job. You can use the Findings page to review the results of a job and begin classifying data.Classify data in Data Discovery directly from a job's results page.
locale: en-US
release: australia
product: Data Discovery
classification: data-discovery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Exploring Data Discovery \(Classic\), Data Discovery, Platform Privacy]
---

# Data Discovery job results

The Data Discovery Findings page shows details on the data found by a job. You can use the Findings page to review the results of a job and begin classifying data.

The Data Discovery Findings page displays the following details after a completed job.

|Column|Description|
|------|-----------|
|Dictionary Entry|Column of the target table where the data was|
|Table|Target table where the data was found|
|Data Pattern|Data pattern used to find the data|
|Data Pattern Match Count|Number of data entries that match the data pattern|
|Total Row Scan Count|Number of rows scanned during the job|
|Percentage of Matching Rows|Percentage of rows in the target table that match the data pattern|
|Data Discovery Job|Job used on the target table|
|Status|Status of the entry|

After you run a Data Discovery job, the results have a status of New. If no action is necessary, you can leave the data alone, which automatically sets the status to Ignored. Otherwise, you can classify the data, such as by creating user-defined data classifications, to prepare for data anonymization using the [Data Classification](data-classification.md) tool.

## Granular Findings

Users may select the **Track Granular Findings** action to use the [Granular Findings](granular-findings.md) page to take action on specific discovered records. See [Granular Findings](granular-findings.md) for more information.

## Available Protections

Select the **Available Protections** button to review an entries control service, status, notes, and last check in. As of Xanadu this feature supports only [Field Encryption](../../encryption/concept/field-encryption.md).

Protecton services can also be accessed from the Dashboard. For more information on the dashboard see, [Data Discovery](data-discovery-landing.md).

## Consolidate findings

Job results can be consolidated using the **Consolidate Findings** button. Job results shared between two separate jobs will then be consolidated under the most recently run job.

**Note:** Only finished full scan jobs may be consolidated

## Classify data in the Data Discovery job results page

Classify data in Data Discovery directly from a job's results page.

### Before you begin

Role required: data\_discovery\_admin and admin

A job must complete a successful run before any result data can appear to be classified.

### Procedure

1.  Go to **System Security** &gt; **Data Discovery** &gt; **Data Discovery Job**.

2.  Select the entry that you want to classify.

3.  In the Data Discovery Findings list, select **Classify**.

4.  Select the data classifications that you want to associate with the table entries.

5.  Select **Classify**.


