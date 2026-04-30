---
title: Differences between OT and standard IT networks
description: There are differences in how the Configuration Management Database \(CMDB\) handles the devices located in Operational Technology networks and those in standard Information Technology \(IT\) networks.
locale: en-US
release: xanadu
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Explore, Operational Technology Manager, Operational Technology]
---

# Differences between OT and standard IT networks

There are differences in how the Configuration Management Database \(CMDB\) handles the devices located in Operational Technology networks and those in standard Information Technology \(IT\) networks.

Configuration items \(CIs\) managed under Information Technology Operations Management \(ITOM\) are classified as type IT in the CMDB. They exist in Levels 4 and 5 of the Purdue Model, or at the Enterprise level.

Devices managed under the OT data model exist in Levels 0 to 3.5 of the Purdue Model, and there are two primary components of OT devices:

1.  A CI class record. This can be an IT or an OT class CI.
2.  An OT device details record. This describes the OT device type \(function\) and other OT-specific attributes.

**Note:** For more information about the OT data model and extension classes, see [Operational Technology \(OT\) extension classes](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models-operation-technology&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

The following graphic depicts these differences.

![Operational Technology CMDB Class Models support Purdue levels.](../image/ot-assets-alignment-cmdb.png "Operational Technology CMDB Class Models support Purdue levels")

**Note:** To learn more about Purdue levels, see [https://subscription.packtpub.com/book/networking\_and\_servers/9781788395151/1/ch01lvl1sec10/the-purdue-model-for-industrial-control-systems](https://subscription.packtpub.com/book/networking_and_servers/9781788395151/1/ch01lvl1sec10/the-purdue-model-for-industrial-control-systems).

**Parent Topic:**[Exploring the Operational Technology Manager](exploring-operational-technology-manager.md)

