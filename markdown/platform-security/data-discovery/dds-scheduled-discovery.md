---
title: Data Discovery scheduled discovery
description: Set up and schedule data discovery jobs to scan your instance for sensitive information.
locale: en-US
release: australia
product: Data Discovery
classification: data-discovery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Data Discovery Store, Data Discovery, Platform Privacy]
---

# Data Discovery scheduled discovery

Set up and schedule data discovery jobs to scan your instance for sensitive information.

## Discovery Jobs

The **Discovery Jobs** table lists all discovery jobs. See [Create discovery job](../task/dds-create-new-job.md) to create a new discovery job.

<table id="table_fhd_dhg_cgc"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the job

</td></tr><tr><td>

Description

</td><td>

The job description

</td></tr><tr><td>

Percent Complete

</td><td>

The percentage completion of the job

</td></tr><tr><td>

Scan Type

</td><td>

Scan type of the job. Possible states are as follows:-   **Sample**: Scans 10,000 entries.
-   **Full**: Scans all entries.

</td></tr><tr><td>

Start Date

</td><td>

The start date of the job

</td></tr><tr><td>

Updated

</td><td>

When the job was last updated.

</td></tr><tr><td>

State

</td><td>

State of the Data Discovery job. The possible states are as follows:-   **Ready to Schedule**: Default state for new jobs.
-   **Scheduled**: The job is scheduled to run.
-   **In Progress**: Job is actively running.
-   **Completed**: Job has finished running successfully.
-   **Error**: The job has stopped running due to an error.
-   **Canceled**: The job has been canceled.
-   **Paused**: The job is paused.

</td></tr><tr><td>

Run

</td><td>

How often the job is scheduled to run.

</td></tr></tbody>
</table>## Discovery Findings

The **Discovery Findings** table lists all the discovered findings from discovery jobs. See [Review discovery findings](../../task/concept/dds-review-discovery-findings.md) to review and classify findings from discovery jobs.

|Label|Description|
|-----|-----------|
|Dictionary Entry|Column of the target table where the data was in|
|Table|Target table where the data was found|
|Data Pattern|Data pattern used to find the data|
|Data Pattern Match Count|Number of data entries that match the data pattern|
|Total Row Scan Count|Number of rows scanned during the job|
|Percentage of Matching Rows|Percentage of rows in the target table that match the data pattern|
|Data Discovery Job|Job used on the target table|
|Status|Status of the entry|

## Granular Configuration

The **Granular Configuration** table lists all granular discovery jobs. See [Create granular job](../task/dds-create-granular-job.md) to learn how to create a granular discovery job.

<table id="table_jmf_q4g_cgc"><thead><tr><th>

Label

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Table of the granular discovery job

</td></tr><tr><td>

Column label

</td><td>

Column label of the granular discovery job

</td></tr><tr><td>

Scan Start Point

</td><td>

Sensitive data will only be discovered for the day of and after the scan start point.**Note:** If the scan start point is left empty, all entries in the column are scanned.

</td></tr><tr><td>

Active

</td><td>

The state of the granular discovery job.

</td></tr></tbody>
</table>## Granular Findings

The **Granular Findings** table lists all the granular findings from granular discovery jobs. See [Review granular findings](../task/dds-review-granular-findings.md) to review the findings from granular discovery jobs.

<table id="table_h3c_2pg_cgc"><thead><tr><th>

Label

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Record

</td><td>

Discovered record

</td></tr><tr><td>

Table

</td><td>

Parent table of the record

</td></tr><tr><td>

Data Pattern

</td><td>

Pattern used to discover the record

</td></tr><tr><td>

Action

</td><td>

Action to be taken on the record-   **Review**

Record is pending review. This is assigned to new granular discoveries

-   **Ignore**

No action will be taken on the record

-   **Anonymize**

Record will be anonymized


</td></tr><tr><td>

Status

</td><td>

The status of the record-   **New**

Status assigned to finding when it is first reported

-   **Processed**

When user chosen action has been successfully applied on the finding

**Note:** Processed findings are store for 3 days in the Granular Findings table before deletion

-   **Manual Review**

When applying user chosen action has failed

**Warning:** Findings in Manual Review should be deleted by users after taking appropriate actions.


</td></tr></tbody>
</table>