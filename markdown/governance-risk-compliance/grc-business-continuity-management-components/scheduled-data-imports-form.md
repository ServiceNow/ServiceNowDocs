---
title: Scheduled Data Imports form
description: Use the Scheduled Data Imports form in the BCM Configurable Workspace to add details about a Scheduled data imports record.
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure Scheduled Imports, Setup for Crisis map, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Scheduled Data Imports form

Use the Scheduled Data Imports form in the BCM Configurable Workspace to add details about a Scheduled data imports record.

<table id="table_dnn_4mf_dqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the scheduled data import, typically matching the alert source record name \(for example, GDAC Feed Source\). For information on configuring scheduled data imports, see [Configure Scheduled Data Imports records](../task/sched-data-imports-crisis-map-uib-ws.md).

</td></tr><tr><td>

Data source

</td><td>

Internal or external source of the threat and alert data used for import, for example, GDAC Feeds.

</td></tr><tr><td>

Run as

</td><td>

User who has the permission to import the threat alerts, for example, System Administrator.

</td></tr><tr><td>

Application

</td><td>

Read-only field. Application that helps distinguish items relevant to the Crisis map, for example, Threat and alert data feeds for Crisis Management application.

</td></tr><tr><td>

Run

</td><td>

Frequency at which the data is imported. Available options are:-   Daily
-   Weekly
-   Periodically
-   Monthly
-   After Parent Runs
-   Once

</td></tr><tr><td>

Active

</td><td>

Option to activate the scheduled import.

</td></tr><tr><td>

day

</td><td>

Day on which the import is scheduled to run. Visible only if you select **Active**.

</td></tr><tr><td>

Time

</td><td>

Time scheduled for the data import in Hours, Minutes, Seconds. Visible only if you select **Active**.

</td></tr><tr><td>

Conditional

</td><td>

Option to indicate if a conditional script is required for the threat alert import.

</td></tr><tr><td>

Condition

</td><td>

Script that evaluates whether an import should run. This field is visible only if you select **Conditional**.

</td></tr><tr><td>

Concurrent Import

</td><td>

Option for enabling concurrent imports. Splits data into multiple imports sets.

 A concurrent import splits the data into multiple import sets and runs the import sets concurrently to reduce processing time for large data sets.

</td></tr><tr><td>

Partition method

</td><td>

Method used to allocate each data set record to an import set. This field is visible only if you select **Concurrent Import**. Available options are:-   Custom script: Sets the partitions with a Partition Script that you provide.
-   Custom size: Sets the partition size to the Partition Size specified.
-   Round robin: Partitions set automatically by the system.

</td></tr><tr><td>

Partition script

</td><td>

Script used to return a partition key. The system ensures that data set rows with the same partition key go to the same import set.Visible only if you set Partition Method to **Custom Script**.

</td></tr><tr><td>

Execute pre-import script

</td><td>

Option to specify a script to run before the import is performed.

</td></tr><tr><td>

Prescript

</td><td>

Script to run before the data imports. Visible only if you select **Execute pre-import script**.

</td></tr><tr><td>

Execute post-import script

</td><td>

Option for enabling the execution of a post-import script.

</td></tr><tr><td>

Post script

</td><td>

Script to run after the import happens. Visible only if you select **Execute post-import script**.

</td></tr></tbody>
</table>**Parent Topic:**[Configure Scheduled Data Imports records](../task/sched-data-imports-crisis-map-uib-ws.md)

