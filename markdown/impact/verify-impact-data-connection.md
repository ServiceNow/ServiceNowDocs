---
title: Verify Impact data connection
description: During Impact Guided Setup automated registration, a status is provided to indicate a successful connection. Use the Verify the Connection step to track the progress.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-05-01"
reading_time_minutes: 1
breadcrumb: [Configure the Impact Store Application, Configuring Impact, Impact]
---

# Verify Impact data connection

During Impact Guided Setup automated registration, a status is provided to indicate a successful connection. Use the Verify the Connection step to track the progress.

## Before you begin

[Use automated registration to connect to the Impact Delivery Instance](start-automated-registration-IDI.md) before this procedure.

Role required: impact admin and IDI admin

## Procedure

1.  Navigate to **All** &gt; **Impact** &gt; **Configuration** &gt; **Guided Setup** &gt; **Verify the Connection**.

    The Verify connection table loads. Once the connection has been initiated, the status updates in the Provider connections record.

    **Note:** ![Verify connection table with the success statuses, Active Replication showing.](../image/verify-connection-status.png)

2.  Verify that the inbound and outbound statuses update to **Active Replication**.

<table id="table_fbs_gqq_zfc"><thead><tr><th>

Status

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Outbound status

</td><td>

-   Active replication: Status with successful connection and registration.
-   Not onboarded: The status before a successful connection to IDI and registration is completed.


</td></tr><tr><td>

Inbound status

</td><td>

-   Active replication: Status with successful connection and registration.
-   Not onboarded: The status before a successful connection to IDI and registration is completed.


</td></tr></tbody>
</table>    **Warning:** If either status does not update to Active Replication, contact your Impact Customer Success Manager for further assistance. In some cases, you may be instructed to continue with the manual registration process. See [Initiate the connection to the Impact Delivery Instance with manual registration](../concept/initiate-the-connection-impact-delivery-instance.md) for manual registration.


## What to do next

[Initiate data migration from IDI](initiate-migration-idi.md)

**Parent Topic:**[Configure the Impact Store Application](../concept/configuring-impact-platform.md)

**Previous topic:**[Use automated registration to connect to the Impact Delivery Instance](start-automated-registration-IDI.md)

**Next topic:**[Initiate data migration from IDI](initiate-migration-idi.md)

