---
title: Apache HBase instance discovery
description: Discovery creates or updates a CMDB record when it detects a running instance of HBase on a UNIX server.
locale: en-US
release: xanadu
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Operating systems discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Apache HBase instance discovery

Discovery creates or updates a CMDB record when it detects a running instance of HBase on a UNIX server.

**Note:** See the knowledge article [KB0687582](https://support.servicenow.com/kb_view.do?sysparm_article=KB0687582) for information on model\_id and manufacturer.

In the following table, the `HBase Instance@*hostname*` source may contain the information on whether the instance is a primary or a secondary instance. The name contains *Hmaster* if the instance is a primary instance. The name contains *HRegionServer* if the name is a secondary instance.

|Label|Table Name|Field Name|Source|
|-----|----------|----------|------|
|Name|cmdb\_ci\_db\_hbase\_instance|name|HBase Instance@*hostname*|
|Root Directory|cmdb\_ci\_db\_hbase\_instance|root\_dir|hbase-site.xml|
|TCP port|cmdb\_ci\_db\_hbase\_instance|tcp\_port|running process|
|Site XML|cmdb\_ci\_db\_hbase\_instance|site\_xml|hbase-site.xml|
|Version|cmdb\_ci\_db\_hbase\_instance|version|HBase shell|
|HBase Home|cmdb\_ci\_db\_hbase\_instance|hbase\_home|running process|
|ZooKeeper Quorum|cmdb\_ci\_db\_hbase\_instance|zookeeper|hbase-site.xml|

**Parent Topic:**[Operating systems discovery](../concept/c_Computers.md)

