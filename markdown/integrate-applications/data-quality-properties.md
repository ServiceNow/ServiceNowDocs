---
title: Data quality properties
description: System property that controls how long data quality records are retained in the data quality audit and unmatched resource queue tables.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/data-quality-properties.html
release: australia
topic_type: reference
last_updated: "2026-06-23"
reading_time_minutes: 1
breadcrumb: [Reference, Data Catalog, Workflow Data Fabric]
---

# Data quality properties

System property that controls how long data quality records are retained in the data quality audit and unmatched resource queue tables.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the filter navigator.

<table><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**sn\_dcg\_core.dq.purge\_retention\_days**

</td><td>

Number of days that records in the data quality audit \[sn\_dcg\_core\_dq\_audit\] and unmatched resource queue \[sn\_dcg\_core\_dq\_unmatched\_resource\_queue\] tables are retained before the **DCG Core - DQ Daily Maintenance** scheduled job deletes them. Values that are empty, non-numeric, or outside the valid range fall back to the default of 7, and the job records a warning in the system log. -   Type: integer
-   Default value: 7
-   Other possible values: Any integer from 1 to 90

</td></tr></tbody>
</table>**Parent Topic:**[Data catalog reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/data-catalog-reference.md)

