---
title: Run Instance Data Replication diagnostics
description: Verify the status of services and the connection between your instance and the Instance Data Replication \(IDR\) message queue.
locale: en-US
release: australia
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: task
last_updated: "2026-03-12"
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

<table id="choicetable_h22_qgv_4nb"><tbody><tr><td id="d469044e86">

**Key Management Framework**

</td><td>

Verifies the KMF configuration by checking the Certificate Management Service and the EJBCA Service status.-   **Certificate Management Service**

Checks for valid certificates in the sys\_certificate table.

-   **EJBCA Service**

Checks the status and setup of the PKI used between instances for secure communication.

</td></tr><tr><td id="d469044e115">

**IDR Scheduled Jobs**

</td><td>

Verifies that scheduled jobs used by IDR are operational.-   **Sys Auto Table**

Checks the Scheduled Job \[sysauto\] table for duplicate entries or missing jobs.

-   **Sys Trigger Table**

Checks the Schedule Item \[sys\_trigger\] table for duplicate entries or missing jobs.

</td></tr><tr><td id="d469044e146">

**Hermes**

</td><td>

Verifies whether the Hermes Messaging Service is available.-   **Hermes Enabled**

Determines whether Hermes is enabled by verifying that the Glide Hermes Message Queue plugin \(com.glide.hermes\) is activated.

-   **Hermes Cluster Configuration**

Checks the Hermes Cluster configuration by verifying that the Hermes Cluster Config \[hermes\_cluster\_config\] table is populated.

</td></tr></tbody>
</table>3.  Test the connection to the message queue and confirm the replicator is working by selecting **Run Message Queue Connection Test**.

    A test message is sent to and received from the Hermes cluster.


## Result

The resulting messages validate enabled services or the connection to the message queue.

**Parent Topic:**[Resolving data replication errors in Instance Data Replication](../reference/common-issues-idr.md)

