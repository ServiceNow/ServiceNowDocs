---
title: Domain Migration Tool
description: Use the Domain Migration Tool to move a customer from a domain-separated environment to their own dedicated instance.Move a customer from a domain-separated environment into their own dedicated instance environment.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Setup and administration, Domain separation for service providers, Access Management]
---

# Domain Migration Tool

Use the Domain Migration Tool to move a customer from a domain-separated environment to their own dedicated instance.

## Domain Migration Tool plugin

The Domain Migration Tool plugin \(com.glide.domain.migration\_tool\) simplifies the task of moving a customer from a domain-separated environment to a more flexible dedicated instance. Customers may want to migrate to a separate instance to take greater advantage of the ServiceNow AI Platform capabilities. Although the Domain Separation plugin is installed, the data and process separation properties are turned off.

**Note:** You must request a cloned instance and request activation of the Domain Migration Tool plugin before you can use it.

The Domain Migration Tool runs only if both data and process separation are enabled in the domain-separated instance:

-   The **glide.sys.domain.partitioning** data property must be set to **true**.
-   The **glide.sys.domain.delegated\_administration** process property must be set to **true**.

## What the migration tool does

-   Automates much of the migration process, especially cleaning up data.
-   Migrates the domain-separated instance to a new dedicated instance.
-   Deletes data from the dedicated instance.

    **Note:** The tool doesn't delete data that is global, in the target domain, or in additional data domains \(if specified\).

-   Collapses process data, or if unable to collapse, deletes process data
-   Keeps process records that are visible to the target domain
-   Updates the sys\_choice, sys\_ui\_list, and sys\_ui\_related\_list special tables
-   Cleans up records added by domain separation plugins:
    -   Business rules
    -   UI actions
    -   Scheduled jobs
    -   Installation exits
    -   Navigation modules
-   Disables domain separation and removes domains from the cloned instance:
    -   Sets these properties to **false** in the cloned instance:
        -   **glide.sys.domain.partitioning**
        -   **glide.sys.domain.delegated\_administration**
        -   **glide.sys.domain.enabled**
    -   Deletes all domains except the target domain and any additional specified data domains.
-   Updates the **Status** field in the domain\_migration\_tool\_status table.

    |Status|Description|
    |------|-----------|
    |Pending|Default status of domain separated tables during migration. The tables are scheduled to be migrated, but have not yet started the migration.|
    |Failure|Table level failure. If the migration process is finished with errors, this status indicates which tables have errors.|
    |Running|The status of the table that is currently migrating. Only one table can have this status and currently migrating.|
    |Successful|The status of the tables that have successfully migrated.|
    |Finished successfully|The migration process is finished without errors.|
    |Finished with errors|The migration process is finished with errors.|

-   Logs progress and status to syslog\_domain

    The source is **MigrationTool** for all log entries associated with migration.

    -   Logs each data table and how many data tables remain
    -   Logs each process table and which domain’s records are currently being inactivated or deleted

## What the migration tool doesn't do

-   Clone the instance
-   Create another domain-separated instance
-   Migrate records \(data or process\) if either data or process separation properties are disabled before you run the tool
-   Alter any data on the source instance
-   Delete data that is global, in the target domain, or in additional data domains \(if specified\)

## What you must do after running the tool

The Domain Migration Tool automates the removal of data outside the desired domains \(the target domain, any additional data domains, and the global domain\). You must evaluate all the remaining configurations to ensure that they are appropriate and work for your dedicated instance. For example, if you had a business rule that set the domain field on records, you might want to disable this business rule, since it no longer serves a purpose.

## Migrate a domain-separated instance to a dedicated instance

Move a customer from a domain-separated environment into their own dedicated instance environment.

### Before you begin

Role required: admin

### Procedure

1.  Elevate to the security\_admin role.

    See [Elevate to a privileged role](../../security/task/t_ElevateToAPrivilegedRole.md) for details.

2.  Navigate to **All** &gt; **Domain Admin** &gt; **Domain Migration Tool**.

    Also access with **domain\_migration\_tool\_status.list**.

3.  Click **New**.

4.  Complete the form.

    |Field|Description|
    |-----|-----------|
    |Target domain|Specify the domain used for both process and data that you want to migrate. Only the target domain is retained, not any of its children, unless specified in the **Additional data domains** field.|
    |Additional data domains|Optionally, specify any additional data domains you want to migrate. If you want to migrate the target domain and all of its children, you must specify all children.|

5.  Select **Submit**.

6.  Open the form you just submitted.

7.  Navigate to **All** &gt; **Domain Separation Center** &gt; **Configure Audits** .

    See [Domain Separation Center](../reference/domain-separation-center.md) for additional information.

8.  Set the **Validate Domain Separated Table Schema** audit to **Active** and assign a schedule.

    This is a precautionary domain audit to pre-check the schema for the health of domain separated tables. This enables you to fix errors before running the migration.

9.  Run the **Audit Schedule** that includes the schema.

    See [Execute audits immediately](../task/execute-audits-immediately.md) for details.

10. Address issues returned from the audit.

    ![Error example from schema check.](../image/validate-domain-schema-error.png)

11. Select **Start Migration**.

    -   The execution tracker progress bar and the domain migration tool are triggered.![Domain migration progress bar.](../image/domain0migration-progress-bar.png)
    -   The current progressing migrating table is displayed along with the total percentage of successfully migrated tables.
    -   The table where all of the domain separated tables are recorded with the migration status, total number of records in each table, and the number of records migrated.
    -   The count of tables where migration failed is also recorded.
    -   The **Status** is updated as the tool performs its functions.
    -   Domain Migration is still running in the background if you close the progress bar. Access the sys\_execution\_tracker table and look for **Running Migration on Tables** to check the migration process running in the background.
    The Domain Migration Tool Status displays the following fields:

<table id="table_ydj_vzw_fwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Status

</td><td>

Displays the migration status. -   **Migrating data tables...**: In progress status.
-   **Migration successful**: The updated status after a successful migration.
-   **Misconfiguration is observed on one of the domain separated tables**: Indicates a failure of data migration. A schema error has been found, the migration won’t start. Run the audit **Validate domain separated table schema**. The audit will fail and show the tables that don't follow the schema standard.
-   **Finished with Errors in Revisit Tables**: The number of tables to address schema migration is listed. Locate the failures in the Revisit tables count and address schema issues.
-   **Domain Migration Failed for Tables...**: Non target records should be deleted manually from failed tables.
-   **Finished Successfully**: When all tables have migrated.


</td></tr><tr><td>

Target domain

</td><td>

The selected target domain for migration.

</td></tr><tr><td>

Additional data domains

</td><td>

Populates if multiple migration domains have been selected.

</td></tr><tr><td>

Revisit Tables Count

</td><td>

This field populates only if a table fails to migrate. If there are no failures, this count is zero. In this case, the tables will be revisited to reattempt the migration. If there are no failures, no need to revisit the tables or reattempt the migration.

</td></tr><tr><td>

Current Progressing Table

</td><td>

Displays the name of the table that is currently being migrated. After successful migration, this field will be empty.

</td></tr></tbody>
</table>12. Select the **Click here** link on the Domain Migration Tool Status page to open the Execution Tracker.![Link to reopen the Domain Migration tool progress bar.](../image/relaunch-progress-bar.png)

    You can also access the sys\_execution\_tracker table and look for **Running Migration on Tables** to check the migration process running in the background.

13. Select **Show status** in the Related Links section to access the progress bar any time during the migration.![Displays the Show status link on the Execution Tracker.](../image/show-status-execution-tracker.png)

    In the case that a table failed the schema check, the Migration Status of Domain Separated Tables overall status will be **Failed**.![The overall migration status shows failed.](../image/failed-status.png)

    There will be **Failed** entries for each corresponding table.

    ![Displays the tables that failed the migration.](../image/domain-migration-failure-status-table.png)

    The remainder of the migration continues and a summary of all failed tables and the total number of **Revisit Tables Count** will be populated in the Domain Migration Tool Status.![Shows the number of tables that failed and require a tables revisit count.](../image/revisit-tables-count.png)

    The **Status** is **Finished Successfully** when the migration is complete. ![Shows successful migration status.](../image/migration-successful.png)


