---
title: Managing CMDB data deletion
description: The Integration Commons for CMDB \(sn\_cmdb\_int\_util\) store app uses post-script and transform map methods to remove imported Configuration Management Database \(CMDB\) records that were deleted later from the source third-party application.
locale: en-US
release: australia
product: CMDB Integration Commons
classification: cmdb-integration-commons
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integration Commons for CMDB, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Managing CMDB data deletion

The Integration Commons for CMDB \(sn\_cmdb\_int\_util\) store app uses post-script and transform map methods to remove imported Configuration Management Database \(CMDB\) records that were deleted later from the source third-party application.

## Post-script method

The post-script method checks the Source \[sys\_object\_source\] table for configuration items \(CIs\) not updated in the last run for a specific source feed. It then removes any non-updated CIs from the associated target CMDB tables synchronously, handling the removal of target records one at a time.

Most Service Graph Connectors use the post-script method to manage the removal of any CMDB records.

The post-script method uses the `RecordRemoval` script to handle various record deletion strategies. Hard deletion involves permanently and completely removing records from the CMDB, making them unrecoverable and suitable for data that is no longer needed. Soft deletion marks records as deleted without actually removing them from the CMDB, allowing for potential recovery and preserving historical data. Optimized soft deletion, managed by the Identification and Reconciliation Engine \(IRE\), enhances this soft deletion approach by using a specialized table, such as the extension attributes table, and applying reconciliation rules to manage deleted records more efficiently. By default, the table can hold up to 100 records at a time, but as a user with the admin role, you can adjust this limit by setting the **sn\_cmdb\_int\_util.ire\_payload\_items\_size** system property. This property is not available by default and you must create this property of type integer within the Integration Commons for CMDB \(sn\_cmdb\_int\_util\) store app. For more information, see Add a system property.

## Transform map-based method

The transform map-based method checks the Source \[sys\_object\_source\] table for configuration items \(CIs\) not updated in the last run for a specific source feed. It then utilizes the multi-threaded deletion approach to remove any non-updated CIs from the associated target CMDB tables concurrently, handling the removal of all target records within an import set at once. Multiple import sets are created to store target record data within the Integration Commons Remove Record \[sn\_cmdb\_int\_util\_remove\_record\] staging table enabling multi-threaded deletion of records. Therefore, reducing the data processing time.

The Integration Commons Remove Record \[sn\_cmdb\_int\_util\_remove\_record\] staging table tracks non-updated CIs by storing target record details including the discovery source, source feed, target table sys\_id, and target table name of these CIs. The on-start script defined within the **Remove Record Transform Map** then deletes the records from the associated target tables.

The transform map-based method is used by a Service Graph Connector to improve the data processing time. For example, the SG-Tanium Remove Software data source within the Service Graph Connector for Tanium removes software data using the transform map-based method. See [Service Graph Connector for Tanium](cmdb-integration-tanium.md).

