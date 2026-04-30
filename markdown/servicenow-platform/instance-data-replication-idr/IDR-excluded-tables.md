---
title: Excluded tables in Instance Data Replication
description: You can't replicate certain tables in Instance Data Replication \(IDR\). Child tables of tables in the exclusion list are also excluded.
locale: en-US
release: xanadu
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Reference, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Excluded tables in Instance Data Replication

You can't replicate certain tables in Instance Data Replication \(IDR\). Child tables of tables in the exclusion list are also excluded.

## Excluded tables

These tables are excluded from IDR:

-   Tables with the prefixes V\_PREFIX, SYSX\_, sys, ts\_, ua\_, usageanalytics\_, wf\_, ecc\_, clone\_, jrobin\_, rrd\_, imp\_, pf\_, pfd\_, idr\_

    sys\_domain is an exception.

-   Rotated tables, including syslog, sys\_querystat, ecc\_queue, ecc\_event, cmdb\_metric, sysevent
-   Tables without a sys\_id
-   sso\_federation
-   saml2\_update1\_properties
-   sso\_properties
-   digest\_properties
-   Instance

Child tables that extend these tables are also excluded from IDR and should not be included in replication sets because replication fails if they are included. For example, sc\_cat\_item extends sys\_metadata, which is an excluded table. This makes sc\_cat\_item an excluded table due to inheritance.

Tables to avoid replicating:

-   cmdb
-   cmdb\_ci

If you determine the CMDB tables must be replicated, you must use conditions to constrain the count of replicated records and ensure all required columns are included in the replication set.

**Parent Topic:**[Instance Data Replication reference](../concept/reference-instance-data-replication.md)

**Related topics**  


[Data privacy in Instance Data Replication](../concept/data-privacy-consumers-idr.md)

[Adapter descriptions for Instance Data Replication](adapter-descriptions.md)

[Domain separation and IDR](instance-data-replication-domain-separation.md)

[Instance Data Replication system properties](instance-data-replication-properties.md)

[Instance Data Replication roles](instance-data-replication-roles.md#)

