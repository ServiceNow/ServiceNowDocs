---
title: Migrate to Contract Management Pro for Legal Service Delivery from Legal Simple Contracts
description: As a legal contracts administrator, migrate data from Legal Simple Contracts to Contract Management Pro for Legal Service Delivery using the migration script.
locale: en-US
release: zurich
product: Legal Simple Contracts
classification: legal-simple-contracts
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Migrate, Legal Simple Contracts, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Migrate to Contract Management Pro for Legal Service Delivery from Legal Simple Contracts

As a legal contracts administrator, migrate data from Legal Simple Contracts to Contract Management Pro for Legal Service Delivery using the migration script.

## Before you begin

Ensure you have prepared the ServiceNow instance for migration. For detailed information, see [Preparing for migration from Legal Simple Contracts to Contract Management Pro for Legal Service Delivery](prepare-for-migration.md).

Role required: sn\_lg\_cnt.contract\_admin

## About this task

-   Migrating a large number of records can take a significant amount of time, so consider running the migration during non-peak working hours.
-   The data related to Legal Simple Contracts will be available even after migration.
-   During migration, the following artifacts are copied to Contract Management Pro for Legal Service Delivery:

    -   Contract types
    -   Contract repository records
    For more information, see [Data copied to Contract Management Pro for Legal Service Delivery during migration from Legal Simple Contracts](lsc-migrate-cmpro-components.md)

    **Note:** Legal requests that are in progress are not migrated. Once a request is closed and the contract finalized, the contract repository records created are automatically copied to Contract Management Pro for Legal Service Delivery if you have run the migration script.

-   During migration, data related to Sales contract review will not be migrated.
-   During migration, contract revisions and intake forms will not be migrated.

## Procedure

1.  Navigate to **All** &gt; **Legal Administration** &gt; **Simple Contracts Admin** &gt; **Contract Types**.

2.  Note the contract types listed in the table.

3.  Navigate to **All** &gt; **Contracts Core** &gt; **Contracts Administration** &gt; **Contracts Types**.

4.  Create the contract types noted in step 2.

    While creating contract type ensure you associate it with a contract model. For more information, see [Create a contract type](../../contract-mgmt-pro/task/cncore-create-contract-type.md)

5.  Navigate to **All** &gt; **Legal Practice Apps** &gt; **Legal Contracts** &gt; **All Contracts**.

6.  Note the number of records in the list of contract repository records.

7.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

8.  Select the **Migrate Old Contracts** scheduled job.

9.  Select **Execute Now** to migrate the data.

10. Compare the number of records created in the Legal Contracts Repository \[sn\_lg\_cnt\_repository\] table to the number of records you noted to track the progress and the total migration success.

11. Access the log messages to check for any failures.

    1.  Check for error messages with the prefix **ContractMigrationUtils**, which indicates a failure to migrate a record.

    2.  For any failed records, check the **Migrate contract related records** and **Copy Contract Attachments** subflow to determine the cause of the failure.

    3.  Fix the errors and re-run the migration script.


-   **[Data copied to Contract Management Pro for Legal Service Delivery during migration from Legal Simple Contracts](lsc-migrate-cmpro-components.md)**  
A migration utility copies data from Legal Simple Contracts tables to Contract Management Pro for Legal Service Delivery tables.

**Parent Topic:**[Migrating to Contract Management Pro for Legal Service Delivery](migration-landing-page.md)

