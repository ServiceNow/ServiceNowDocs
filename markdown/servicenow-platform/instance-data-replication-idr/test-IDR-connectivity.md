---
title: Run Instance Data Replication diagnostics
description: Verify the status of services and the connection between your instance and the Instance Data Replication \(IDR\) message queue.
locale: en-US
release: yokohama
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Resolving errors, Administer, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Run Instance Data Replication diagnostics

Verify the status of services and the connection between your instance and the Instance Data Replication \(IDR\) message queue.

## Before you begin

Role required: admin or idr\_admin

## Procedure

1.  Navigate to **All** &gt; **Instance Data Replication** &gt; **Diagnostics**.

    The dashboard loads and the IDR diagnostic tests run automatically.

2.  View the following diagnostic tests.

<table id="choicetable_h22_qgv_4nb"><tbody><tr><td id="d425538e86">

**Certificate Management Service**

</td><td>

Checks the status and setup of your certificate management service.**Note:** IDR requires a certificate management service to be up and running.

</td></tr><tr><td id="d425538e100">

**EJBCA Service Status**

</td><td>

Checks the status and setup of the EJBCA service as part of the Key Management Framework \(KMF\) health.

</td></tr></tbody>
</table>3.  Test the connection to the message queue and confirm the replicator is working by running the Message Queue Connection Test.

<table id="choicetable_y42_xvl_pvb"><tbody><tr><td id="d425538e124">

**Test the connection to the Legacy message queue**

</td><td>

1.  Select **Legacy**.
2.  In the Legacy Message Queue Test Configuration section, select **Local** or **Remote** to run diagnostics on a local or remote instance. For a remote instance, enter the URL of the remote instance, and a username and password for any of the following roles:

    -   idr\_rest
    -   idr\_read
    -   idr\_admin
**Note:** The local datacenter to your producer instance regional proximity is the default.

3.  Select **Run Legacy Message Queue Test**.


</td></tr><tr><td id="d425538e171">

**Test the connection to the V2 message queue**

</td><td>

1.  Select **V2**.
2.  Confirm that Hermes is enabled and that the Hermes cluster configuration is operational.
3.  Select **Run Message Queue Connection Test**.


</td></tr></tbody>
</table>
## Result

The resulting messages validate enabled services or the connection to the message queue.

**Parent Topic:**[Resolving data replication errors in Instance Data Replication](../reference/common-issues-idr.md)

