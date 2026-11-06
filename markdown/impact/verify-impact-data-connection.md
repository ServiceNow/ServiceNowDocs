---
title: Verify Impact data connection
description: During Impact Guided Setup automated registration, a status is provided to indicate a successful connection. Use the Verify the Connection step to track the progress. If you used manual registration, verify your connection through the Provider Connections page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/impact/verify-impact-data-connection.html
release: australia
topic_type: task
last_updated: "2026-11-06"
reading_time_minutes: 1
breadcrumb: [Register and connect to the data provider, Configuring Impact, Impact]
---

# Verify Impact data connection

During Impact Guided Setup automated registration, a status is provided to indicate a successful connection. Use the Verify the Connection step to track the progress. If you used manual registration, verify your connection through the Provider Connections page.

## Before you begin

**Important:** Navigation to reach this step differs depending on whether you're using the [Impact Setup Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/use-impact-setup-hub.md) or the legacy [Guided Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/guided-setup-impact-in-app.md). See whichever one applies to you for the exact path.

Complete registration before this procedure.

Role required: impact app admin, impact admin \(IDI\)

## Procedure

1.  Check the connection status.

    The Verify connection table loads. Once the connection has been initiated, the status updates in the Provider connections record.

    **Note:** \[Omitted image "verify-connection-status.png"\] Alt text: Verify connection table with the success statuses, Active Replication showing.

    **Note:** If you used manual registration, the registration status tracker does not apply. To verify your connection, navigate to **All** &gt; **Impact** &gt; **Configuration** &gt; **Provider connections** and confirm that both the inbound and outbound statuses show **Active Replication**.

2.  Verify that the inbound and outbound statuses update to **Active Replication**.

<table id="table_fbs_gqq_zfc"><thead><tr><th>

Status

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Outbound status

</td><td>

-   **Active replication**: Status with successful connection and registration.
-   **Not onboarded**: The status before a successful connection to IDI and registration is completed.


</td></tr><tr><td>

Inbound status

</td><td>

-   **Active replication**: Status with successful connection and registration.
-   **Not onboarded**: The status before a successful connection to IDI and registration is completed.


</td></tr></tbody>
</table>
## What to do next

[Initiate data migration from IDI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/initiate-migration-idi.md)

**Parent Topic:**[Register and connect to the data provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/initiate-registration.md)

