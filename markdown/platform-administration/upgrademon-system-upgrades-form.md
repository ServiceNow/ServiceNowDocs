---
title: System Upgrades form
description: When an upgrade is complete, the System Upgrades form displays key statistics about the upgrade and a related list of skipped records \(the skipped list\).
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Process the skipped records list, Upgrade Monitor module: Upgrade an individual instance, Upgrades and conversions, Upgrade, Administer the ServiceNow AI Platform]
---

# System Upgrades form

When an upgrade is complete, the System Upgrades form displays key statistics about the upgrade and a related list of skipped records \(the skipped list\).

![Upgrade Details form](../image/upgrade-system-upgrades-small.png "System Upgrades form")

|Screen element|Description|
|--------------|-----------|
|From|The version of the instance before upgrading.|
|To|The version of the instance after upgrading.|
|Upgrade started|The time upgrade started.|
|Upgrade finished|The time the upgrade finished.|
|Skipped|The number of records the system did not upgrade because of conflicts between customizations and the upgrade.|
|Unchanged|The number of records in the instance unchanged by the upgrade.|
|Unchanged and customized|The number of customized records in the instance unchanged by the upgrade.|
|Skipped error|The number of records the system did not upgrade because of one or more errors.|
|Inserted|The number of records the system inserted.|
|Updated|The number of records the system successfully updated.|
|Deleted|The number of records the system deleted.|
|Total|The total number of records the system inspected and/or processed for this upgrade.|

**Parent Topic:**[Process the skipped records list](../task/upgrademon-process-skip-list.md)

