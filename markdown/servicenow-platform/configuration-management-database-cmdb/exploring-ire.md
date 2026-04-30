---
title: Exploring CMDB Identification and Reconciliation \(IRE\)
description: The Identification and Reconciliation \(IRE\) module provides a centralized framework for identifying and reconciling data from different data sources. It helps maintain the integrity of the CMDB and some non-CMDB tables when multiple data sources are used to create and update CI records.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [CMDB Identification and Reconciliation \(IRE\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Exploring CMDB Identification and Reconciliation \(IRE\)

The Identification and Reconciliation \(IRE\) module provides a centralized framework for identifying and reconciling data from different data sources. It helps maintain the integrity of the CMDB and some non-CMDB tables when multiple data sources are used to create and update CI records.

The use of multiple data sources increases the risk of introducing inconsistencies through duplicate records. To maintain the integrity of the database, it is important to correctly identify CIs and services so that new records are created only for CIs that are truly new.

The Identification and Reconciliation Engine \(IRE\) helps maintain the data integrity as follows:

-   Prevent duplicate CIs by uniquely identifying CIs using sets of identification rules
-   Reconcile CI attributes by allowing only authoritative data sources to write to the CMDB or to a supported non-CMDB table
-   Reclassify CIs
-   Provide a centralized framework to perform identification and reconciliation across different data sources

Data sources such as ServiceNow Event Management, Horizontal Discovery, Import Sets, Cloud Insights, Pattern Discovery, and Manual Entry, use IRE APIs to perform CI identification and reconciliation. In addition, any 3rd party data source can leverage REST/Scriptable IRE APIs to also perform CI identification and reconciliation.

## Support for non-CMDB tables

IRE processes support some non-CMDB tables. You can create identification rules, reconciliation rules, and other IRE-related rules to ensure the integrity of data inserted or updated in supported non-CMDB tables. For details, see [IRE support for non-CMDB tables](ire-support-non-cmdb-tables.md).

-   **[Components and process](c_CompsandProcessIDandReconcil.md)**  
The CMDB Identification and Reconciliation functionality is supported by the Identification and Reconciliation engine \(IRE\), rules, and tasks. Identification rules, reconciliation rules, IRE data source rules, de-duplication tasks, and reclassification tasks determine how IRE identifies and reconciles CI.

**Parent Topic:**[CMDB Identification and Reconciliation \(IRE\)](c_CMDBIdentifyandReconcile.md)

