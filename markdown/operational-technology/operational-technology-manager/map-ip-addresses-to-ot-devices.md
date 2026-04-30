---
title: Map IP addresses to OT devices
description: You can use the SyncIPAddressToOT scheduled job to update and synchronize the IP address information for all the available OT devices. The SyncIPAddressToOT scheduled job acquires the IP address information from the IP address \(cmdb\_ci\_ip\_address\) table and adds it to the IP address field of the CI.
locale: en-US
release: xanadu
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [OT device related items and related lists, Edit or view OT devices after import or discovery, Use, Operational Technology Manager, Operational Technology]
---

# Map IP addresses to OT devices

You can use the `SyncIPAddressToOT` scheduled job to update and synchronize the IP address information for all the available OT devices. The `SyncIPAddressToOT` scheduled job acquires the IP address information from the IP address \(cmdb\_ci\_ip\_address\) table and adds it to the IP address field of the CI.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  In the **Scheduled Jobs** page, type `SyncIPAddressToOT` in the **Search** filter and hit enter to find the scheduled job.

3.  Select `SyncIPAddressToOT`.

4.  In the Scheduled Script ExecutionSyncIPAddressToOT page, select **Execute Now**.


**Parent Topic:**[OT device related items and related lists](../reference/ot-assets-related-links-and-lists.md)

