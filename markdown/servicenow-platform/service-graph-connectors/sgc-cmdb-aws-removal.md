---
title: Record removal process in Service Graph Connector for AWS
description: The Service Graph Connector for AWS uses the optimized deletion approach to manage removal of records.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, AWS, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Record removal process in Service Graph Connector for AWS

The Service Graph Connector for AWS uses the optimized deletion approach to manage removal of records.

Record removal is the process of handling data that is no longer needed. For any discovered resources deleted later after pulling data, the Service Graph Connector for AWS automatically updates the **Install Status** field of the associated CMDB CI classes to indicate any retired or deleted records.

Deletion of records in Service Graph Connector for AWS involves marking the install status of a record as **retired** rather than permanently deleting it from the system. The record remains in the database, making it possible to reference or restore it later. Deletion for Service Graph Connector for AWS relies on the Source \[sys\_object\_source table\], which can become inefficient with large datasets.

To enhance the deletion process, you can enable the optimized deletion method that leverages the SG-AWS Extension Attributes \[sn\_aws\_extension\_attributes\] table. This table is regularly purged of obsolete records, improving performance and efficiency. The process still marks the install status of a record as **retired** but the streamlined data structure reduces overhead, ensuring quicker processing and better system performance. See [Enable optimized deletion of retired CIs in AWS](../task/sgc-cmdb-aws-delete-cis.md).

Optimized deletion is enabled for all tables in the Service Graph Connector for AWS, except for the following tables:

-   Hardware Type \[cmdb\_ci\_compute\_template\]
-   Availability Zone \[cmdb\_ci\_availability\_zone\]
-   AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]
-   Running Process \[cmdb\_running\_process\]
-   TCP Connections \[cmdb\_tcp\]
-   Application \[cmdb\_ci\_appl\]

**Parent Topic:**[Service Graph Connector for AWS reference](sgc-cmdb-aws-reference.md)

