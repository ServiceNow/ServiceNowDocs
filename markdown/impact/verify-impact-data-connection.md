---
title: Verify Impact data connection
description: During Impact Guided Setup automated registration, a status is provided to indicate a successful connection. Use the Verify the Connection step to track the progress. If you used manual registration, verify your connection through the Provider Connections page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/verify-impact-data-connection.html
release: brazil
topic_type: task
last_updated: "2026-09-24"
reading_time_minutes: 1
breadcrumb: [Sync your Impact data, Impact Guided Setup, Configuring Impact, Impact]
---

# Verify Impact data connection

During Impact Guided Setup automated registration, a status is provided to indicate a successful connection. Use the Verify the Connection step to track the progress. If you used manual registration, verify your connection through the Provider Connections page.

## Before you begin

[Use automated registration to IDI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/start-automated-registration-IDI.md) before this procedure.

Role required: impact app admin, impact admin \(IDI\)

## Procedure

1.  Navigate to **All** &gt; **Impact** &gt; **Configuration** &gt; **Guided Setup** &gt; **Verify the Connection**.

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
</table>    **Warning:** If either status does not update to Active Replication, contact your Impact Customer Success Manager before proceeding. In some cases, you may be instructed to continue with the manual registration process. However, if the automated registration failed, the manual configuration may also fail if the root cause is unresolved. See [Initiate the connection to Impact data with manual registration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/initiate-the-connection-impact-delivery-instance.md) for manual registration.


## What to do next

[Initiate data migration from IDI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/initiate-migration-idi.md)

**Parent Topic:**[Use automated registration to IDI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/start-automated-registration-IDI.md)

