---
title: Using software counters with the legacy Oracle Process Pack
description: There are two distinct ways to count Oracle software through the legacy Oracle Process Pack. Be sure that your Oracle models are set up accurately.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Legacy Oracle process pack, Legacy Software Asset Management plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Using software counters with the legacy Oracle Process Pack

There are two distinct ways to count Oracle software through the legacy Oracle Process Pack. Be sure that your Oracle models are set up accurately.

**Note:** Oracle license calculation types are available in the Software Counter form after you activate the legacy Oracle process pack.

Oracle software that uses the **Oracle Processor** license calculation type counts by the number of processors on a server. This license calculation type must exist in the Software Installation \[cmdb\_sam\_sw\_install\] table. A software installation record must be inserted with a discovery model that matches the correct Oracle software. For an install to be counted by an Oracle processor counter, the **Installed on** field on the Software Installation form should reference a configuration item with a **Metric type** of **Oracle Processor**.

Oracle software that uses the **Oracle Named User** or **Oracle Named User Plus** license calculation types count by number of unique users or number of unique users plus devices. This license calculation type must exist in the Software Usage \[cmdb\_sam\_sw\_usage\] table. A software installation record must be inserted with a discovery model that matches the correct Oracle software. For a usage to be counted by an Oracle New User or Oracle New User Plus counter, the **Target host** field on the Software Usage \[cmdb\_sam\_sw\_usage\] table should reference a configuration item with a **Metric type** of **Oracle NU** or **Oracle NUP**.

**Parent Topic:**[Legacy Oracle process pack](c_OracleProcessPack.md)

