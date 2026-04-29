---
title: Data migration from SIR TI to TISC
description: Data Migration Job Configuration in TISC enables you to move the existing Threat intelligence plugin data to TISC plugin data directly.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Data migration in TISC, Use, Threat Intelligence Security Center, Security Operations]
---

# Data migration from SIR TI to TISC

Data Migration Job Configuration in TISC enables you to move the existing Threat intelligence plugin data to TISC plugin data directly.

## Before you begin

Role required: sn\_sec\_tisc.admin

## About this task

-   **Selective Record Migration**: Only records from the selected table that meet specified conditions are migrated.
-   **Include Relationships**: Related records are migrated only if the **Include Relationships** check box is selected.
-   **Entity Migration Status**: Once an entity \(observable or object\) is migrated, it won't be included in further migrations unless it is being migrated as a related record.

    **Note:** **Records exclusion criteria for migration utility**

    The migration utility excludes certain records based on the following criteria:

    -   **Observables**: Observables of type **file** that contain secure file attachments will not be migrated.
    -   **Indicators**: Indicators with blank values in either the pattern or pattern type fields will not be migrated.
    -   **Objects**: Objects ingested from the MITRE TAXII profile within threat intelligence data will not be migrated to the Threat Intelligence Security Center.
-   **Case Records**: Only active records are migrated by default, unless the **Include Closed Cases** check box is selected.

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence Security Center** &gt; **Data Migration Job Configuration**.

2.  Click **New**.

3.  On the form, fill the fields as appropriate.

<table id="table_ttk_y52_ddc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the data migration.

</td></tr><tr><td>

Table

</td><td>

Select the table from which the records should be migrated to TISC.The TISC table options for migration are:

-   Observable\(sn\_ti\_observable\)
-   Indicator of Compromise\(sn\_ti\_indicator\)
-   Security Case\(sn\_ti\_case\)
-   STIX V2 objects \(sn\_ti\_stix2\_object\) \(options such as attack patterns, campaigns, course of action\)
**Note:**

-   When you select the STIX V2 option then all the STIX objects are migrated except the MITRE ATT&amp;CK as TISC has a different framework to migrate the MITRE ATT&amp;CK.
-   When you select to migrate security case then the closed cases won’t be migrated but only the active cases are migrated.
For example, select **Observable** migration table.

</td></tr><tr><td>

Active

</td><td>

Select this check box if the data migration process is active.

</td></tr><tr><td>

Include Relationships

</td><td>

Select the check box to migrate the relationships of threat intelligence records to TISC records.**Note:** When you select this check box all the related entities are migrated along with the observable and If the check box is not selected, only the single observable will be migrated, without any related entities.

</td></tr><tr><td>

Include Closed Cases

</td><td>

Select this check box if you want to include the closed cases as part of case records migration.

</td></tr><tr><td>

Only Migrate Observables Associated to Security Incident

</td><td>

Select the check box for migrating the observables that are associated with the security incidents and if the check box is not selected, all the observables will be migrated, regardless of their association with security incidents.

</td></tr><tr><td>

Conditions

</td><td>

Option to select the conditions that can be used to filter data being migrated.

</td></tr><tr><td colspan="2">

**Additional Configurations**

</td></tr><tr><td>

Confidence

</td><td>

Enter the confidence for the migrated TISC entities \(observables or objects or indicators\).The confidence should be between 0-100 range.

</td></tr><tr><td>

Expiry period \(days\)

</td><td>

The expiry period for the migrated TISC entities.

</td></tr></tbody>
</table>    **Note:** The system ignores or skips the records that are already migrated to TISC when fetched again.

4.  Click **Submit**.

5.  Click **Execute Now** to execute the data migration.

    When you execute the data migration then a background job is run and the migration job gets created. This job creates a migration process and the batch size of these migration records is 5000.

6.  Verify the migration job status under the **Migration Job Runs** section.

    The job status will be queued and the maximum limit of the batch size should not be exceeding 5000 records. Click on the record to view the objects that are all migrated for that specific entity.

7.  Verify the migration job status under the **Migration Job Runs** related list.

8.  Click on the record to view the processing status.

9.  Verify the batch migration status under the **Migration Processing Queue** records related list section in the migration job run record.

    The batch size for migration of records is 5000.

10. Verify the TISC entities created as part of batch migration under respective related lists in **Migration Processing Queue** record.


