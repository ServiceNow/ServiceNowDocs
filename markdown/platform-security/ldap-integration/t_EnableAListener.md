---
title: Enable an LDAP listener and set system properties
description: Enabling a listener is optional. If enabled, a listener notifies the system to process LDAP records soon after there is an update on the LDAP server.
locale: en-US
release: zurich
product: LDAP integration
classification: ldap-integration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [LDAP integration setup, LDAP integration, Authentication, Access Management]
---

# Enable an LDAP listener and set system properties

Enabling a listener is optional. If enabled, a listener notifies the system to process LDAP records soon after there is an update on the LDAP server.

## Before you begin

Role required: admin.

## About this task

A listener is a dedicated process that periodically searches for changes on the LDAP server.

The listener can be deployed on a Microsoft Active Directory server that supports persistent queries \(ADNotify\), or on an LDAP server that supports persistent search request control \(with OID 2.16.840.1.113730.3.4.3\).

If the LDAP server supports a persistent search, the LDAP listener recognizes any user and group changes made to any of the applicable LDAP accounts and forwards them to your instance within approximately 10 seconds. This allows the instance to have a nearly real-time copy of your users' account details without having to wait for the next scheduled refresh. The LDAP listener can only synchronize objects that map to the User \[sys\_users\] and Group \[sys\_user\_group\] tables.

**Note:** If a user is added via the listener, but the user does not meet the requirements as defined by the OU filter, then the instance ignores the record on the LDAP server. If it meets the criteria, the user is added to the instance.

To enable a listener:

## Procedure

1.  Navigate to **All** &gt; **System LDAP** &gt; **LDAP Servers**.

2.  Select the LDAP server to configure.

3.  Select the **Listener** check box.

4.  Click **Update**.

    **Note:**

    The system only imports user records that match the LDAP OU filter. Incoming user records that do not meet the filter requirements are flagged as invalid and ignored by the import. Administrators can enable verbose LDAP logging to determine if incoming records are not matching the LDAP OU filter.

5.  Navigate to the System Properties \[sys\_properties\] table and set LDAP listener system properties.

<table id="table_dds_vgz_nz"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.ldap.listener.use\_background\_transaction

</td><td>

When true, the LDAP listener is started as a background transaction. By running the LDAP listener as a background transaction, the quota rule LDAP Listener Start/Stop Transaction can cancel the transaction after the maximum duration is reached, 5 minutes by default. This behavior prevents an LDAP listener from waiting indefinitely.**Note:** This property applies only to LDAP connections that do not use a MID Server. Use **glide.ldap.listener.mid.use\_background\_transaction** to control the behavior of LDAP connections that go through a MID Server.

 -   Type: true \| false
-   Default value: false
-   Location: Add to the System Properties \[sys\_properties\] table


</td></tr><tr><td>

glide.ldap.listener.mid.use\_background\_transaction

</td><td>

When true, the LDAP listener is started as a background transaction. By running the LDAP listener as a background transaction, the quota rule LDAP Listener Start/Stop MID Transaction can cancel the transaction after the maximum duration is reached, 5 minutes by default. This behavior prevents an LDAP listener from waiting indefinitely.**Note:** This property applies only to LDAP connections that use a MID Server. Use **glide.ldap.listener.use\_background\_transaction** to control the behavior of LDAP connections that do not go through a MID Server.

 -   Type: true \| false
-   Default value: false
-   Location: Add to the System Properties \[sys\_properties\] table


</td></tr><tr><td>

glide.ldap.listener.mid.one\_listener

</td><td>

When true, only a single ECC queue message is created to start or stop the LDAP listener through a MID Server. When false, multiple ECC queue messages can be created, leading to the creation of multiple threads to start or stop the LDAP listener.-   Type: true \| false
-   Default value: true
-   Location: Add to the System Properties \[sys\_properties\] table


</td></tr></tbody>
</table>
