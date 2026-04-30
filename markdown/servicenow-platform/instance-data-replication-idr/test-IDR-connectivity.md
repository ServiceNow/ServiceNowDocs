---
title: Run Instance Data Replication diagnostics
description: Verify the status of services and the connection between your instance and the Instance Data Replication \(IDR\) message queue.
locale: en-US
release: zurich
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: task
last_updated: "2025-07-31"
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

<table id="choicetable_h22_qgv_4nb"><tbody><tr><td id="d462000e86">

**Certificate Management Service**

</td><td>

Checks the status and setup of your certificate management service.**Note:** IDR requires a certificate management service to be up and running.

</td></tr><tr><td id="d462000e100">

**EJBCA Service Status**

</td><td>

Checks the status and setup of the EJBCA service as part of the Key Management Framework \(KMF\) health.

</td></tr><tr><td id="d462000e115">

**Hermes Enabled**

</td><td>

Checks whether the Hermes Messaging Service is available.

</td></tr><tr><td id="d462000e127">

**Hermes Cluster Configuration**

</td><td>

Checks the status of the Hermes cluster.

</td></tr></tbody>
</table>3.  Test the connection to the message queue and confirm the replicator is working by selecting **Run Message Queue Connection Test**.

    A test message is sent to and received from the Hermes cluster.


## Result

The resulting messages validate enabled services or the connection to the message queue.

**Parent Topic:**[Resolving data replication errors in Instance Data Replication](../reference/common-issues-idr.md)

