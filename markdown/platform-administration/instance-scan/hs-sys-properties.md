---
title: Instance Scan properties
description: On the properties form, you can set parameters that control how the instance executes.
locale: en-US
release: australia
product: Instance Scan
classification: instance-scan
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Instance Scan references, Instance Scan, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Instance Scan properties

On the properties form, you can set parameters that control how the instance executes.

<table id="table_f14_32f_yhc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.scan.inactive\_records

</td><td>

-   Controls whether instance scan considers inactive records, where active=false
-   The default value is false. Instance Scan scans only the active records
-   When enabled, scans will include inactive records in the health check evaluation

</td></tr><tr><td>

glide.scan.max\_parallel\_scans

</td><td>

-   Defines the maximum number of instance scans that can run concurrently
-   The default value is 5
-   Used by the scan queue system to limit parallel scan execution

</td></tr><tr><td>

glide.scan.parallel\_scan\_enabled

</td><td>

-   Enables or disables the parallel scan feature
-   The default value is true
-   When enabled, it allows multiple scans to run simultaneously based on the max\_parallel\_scans limit

</td></tr><tr><td>

glide.scan.queue.enabled

</td><td>

-   Enables or disables the instance scan queue system
-   The default value is true
-   When enabled, scan requests are queued and processed based on available capacity

</td></tr><tr><td>

glide.scan.base\_system\_records

</td><td>

-   Controls whether instance scan checks out-of-box \(base system\) records
-   The default value is false. The Base system records are skipped

**Note:** The Base system records are determined by checking if they would be replaced during an upgrade using the CollisionAPI.

-   When enabled, scans will include records that would be replaced on upgrade \(non-customized ServiceNow delivered records\)

</td></tr><tr><td>

glide.scan.sn\_non\_standard\_scopes\_list

</td><td>

-   Comma-separated list of ServiceNow scopes that shouldn't be treated as third-party scopes
-   The default value is ""
-   Used to exclude specific non-standard ServiceNow scopes from being classified as ISV/third-party applications during scan classification

</td></tr></tbody>
</table>**Parent Topic:**[Instance Scan references](hs-references.md)

**Related topics**  


[Instance Scan roles](instance-scan-roles.md#)

