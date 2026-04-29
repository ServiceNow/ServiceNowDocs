---
title: Run Certificate Discovery via port scans
description: When the TLS port probe \[tls\_ssl\_certs\] is enabled, Discovery automatically scans 14 pre-authorized ports as part of your existing CI Discovery schedules.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Visibility to TLS certificates, Configuring Certificate Inventory and Management, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Run Certificate Discovery via port scans

When the TLS port probe \[tls\_ssl\_certs\] is enabled, Discovery automatically scans 14 pre-authorized ports as part of your existing CI Discovery schedules.

## Before you begin

Role required: discovery\_admin or admin

## Procedure

1.  Activate the TLS port probe \[tls\_ssl\_certs\].

    1.  Navigate to **Discovery Definition** &gt; **Port Probes**.

    2.  Open **tls\_ssl\_certs**.

    3.  To enable the probe, select the **Active** check box.

        By default, the check box for any new installation is unchecked.

    4.  Save your changes.

2.  Add IP service to help configure the TLS port probe.

    1.  Navigate to **Discovery Definition** &gt; **IP Services**.

    2.  Create a new IP service with a port.

3.  Configure the TLS port probe.

    Edit the Port Probe definition to add up to 138 additional ports or remove existing ones.

    1.  Navigate to **Discovery Definition** &gt; **Port Probes**.

    2.  Open **tls\_ssl\_certs**.

    3.  Unlock the **Triggered by services** field by selecting the lock icon next to it.

    4.  Remove any ports from the list or add additional ones from the search area.

    5.  Save your changes.


## Result

Your existing Discovery schedules should then automatically scan for any certificates on the specified ports.

