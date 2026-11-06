---
title: Initiate data migration from IDI
description: After the connection is established between your Impact Store Application and the Impact Delivery Instance, next migrate your data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/impact/initiate-migration-idi.html
release: australia
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Register and connect to the data provider, Configuring Impact, Impact]
---

# Initiate data migration from IDI

After the connection is established between your Impact Store Application and the Impact Delivery Instance, next migrate your data.

## Before you begin

**Important:** Navigation to reach this step differs depending on whether you're using the [Impact Setup Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/use-impact-setup-hub.md) or the legacy [Guided Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/guided-setup-impact-in-app.md). See whichever one applies to you for the exact path.

Complete registration prior to migrating data.

Role required: impact app admin, admin

## Procedure

1.  On the Impact Data Migration overviews table, select **Start Data Migration**.

    **Note:** See [Table and field level mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/table-field-level-mapping.md) for the available tables for migration.

    \[Omitted image "initiate-data-migration.png"\] Alt text: Initiate migration step with the Start data migration button highlighted.

2.  Check the migration status for each table in the Impact Data Migration Overviews table.

3.  Refresh the page to re-populate the migration statuses in the table data.

    -   The **Overall Migration Status** for each table will update to `Completed` when successfully transferred.
    -   Select to **Re-migrate Data** for added tables or missed tables.
    **Important:** Reach out to your Impact Squad if you require assistance or a table failed to migrate.

4.  Select **Mark as configured** when the data transfer is complete.


## What to do next

-   See [Scan Engine integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/instance-integration-scan-engine.md) to connect instances and external agile systems to synchronize definitions, manage exception reasons, create user stories, and enforce governance over app deployments.
-   [Grant temporary instance access to your Impact Squad](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/hop-access-impact-squad.md)
-   With successful connection and registration, see [Using Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/impact-in-app.md) to get started with your Impact Store Application.

**Parent Topic:**[Register and connect to the data provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/initiate-registration.md)

