---
title: Initiate data migration from IDI
description: After the connection is established between your Impact Store Application and the Impact Delivery Instance, next migrate your data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/initiate-migration-idi.html
release: australia
topic_type: task
last_updated: "2026-07-24"
reading_time_minutes: 1
breadcrumb: [Run Impact Guided Setup, Configuring Impact, Impact]
---

# Initiate data migration from IDI

After the connection is established between your Impact Store Application and the Impact Delivery Instance, next migrate your data.

## Before you begin

**Note:** [Use automated registration to connect to the Impact Delivery Instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/start-automated-registration-IDI.md) prior to migrating data.

Role required: impact app admin, admin

## Procedure

1.  Navigate to **All** &gt; **Impact** &gt; **Configuration** &gt; **Guided Setup** &gt; **Initiate sync &amp; migration**.

2.  Select **Initiate migration** from the listed tasks.

3.  On the Impact Data Migration overviews table, select **Start Data Migration**.

    **Note:** See [Table and field level mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/table-field-level-mapping.md) for the available tables for migration.

    \[Omitted image "initiate-data-migration.png"\] Alt text: Initiate migration step with the Start data migration button highlighted.

4.  Check the migration status for each table in the Impact Data Migration Overviews table.

5.  Refresh the page to re-populate the migration statuses in the table data.

    -   The **Overall Migration Status** for each table will update to `Completed` when successfully transferred.
    -   Select to **Re-migrate Data** for added tables or missed tables.
    **Important:** Reach out to your Impact Squad if you require assistance or a table failed to migrate.

6.  Select **Mark as Complete** on the Initiate Migration page when the data transfer is complete.


## What to do next

-   See [Configure Scan Engine integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/instance-integration-scan-engine.md) to connect instances and external agile systems to synchronize definitions, manage exception reasons, create user stories, and enforce governance over app deployments.
-   [Grant temporary instance access to your Impact Squad](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/hop-access-impact-squad.md)
-   With successful connection and registration, see [Using Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/impact-in-app.md) to get started with your Impact Store Application.

**Parent Topic:**[Run Impact Guided Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/guided-setup-impact-in-app.md)

