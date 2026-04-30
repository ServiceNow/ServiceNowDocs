---
title: Publisher optimizations for SAP
description: View licensing optimizations for SAP by selecting SAP from the Publisher drop-down list.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [References, Software Asset Management, IT Asset Management]
---

# Publisher optimizations for SAP

View licensing optimizations for SAP by selecting **SAP** from the **Publisher** drop-down list.

<table id="table_a3c_hst_2xb"><thead><tr><th>

Report

</th><th>

Source

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Inactive users

</td><td>

SAP System Users\[samp\_sap\_system\_user​\]

</td><td>

SAP system users who last logged in over 90 days ago​.

</td></tr><tr><td>

System users without a named user assignment

</td><td>

SAP System Users\[samp\_sap\_system\_user\]

</td><td>

SAP system users without a named user assignment​.

</td></tr><tr><td>

Locked out licensed SAP users

</td><td>

SAP System Users\[samp\_sap\_system\_user\]

</td><td>

Locked SAP users consuming a license.

</td></tr><tr><td>

Licensed non dialog users

</td><td>

SAP System Users\[samp\_sap\_system\_user\]

</td><td>

SAP non-dialog users with a named user assignment.

</td></tr><tr><td>

Un-used engines

</td><td>

License Metric Results\[samp\_license\_metric\_result\]

</td><td>

Number of SAP engines that haven’t been used, but have active software entitlements.

</td></tr><tr><td>

Users for role based license optimization

</td><td>

SAP System Users\[samp\_sap\_system\_user\]

</td><td>

Number of SAP users that can have their role changed to optimize license consumption.

</td></tr><tr><td>

Users for transaction based license optimization

</td><td>

SAP System Users\[samp\_sap\_system\_user\]

</td><td>

Number of SAP users for which Software Asset Management plugin has detected user transaction-based license optimizations.

</td></tr><tr><td>

HANA database monthly peak usage

</td><td>

SAP License Metric Measurements\[samp\_sap\_license\_metric\_measurement\]

</td><td>

Monthly peak usage of HANA database in gigabytes \(GB\) over the last 12 months.

</td></tr><tr><td>

Digital access usage by client/system

</td><td>

SAP Digital Access\[samp\_sap\_digital\_access\]

</td><td>

Total count of Digital Access licenses consumed, grouped by the SAP client.

</td></tr><tr><td>

Digital access usage by document type

</td><td>

SAP Digital Access\[samp\_sap\_digital\_access\]

</td><td>

Total count of Digital Access licenses consumed, grouped by the document type created.

</td></tr><tr><td>

SAP S/4HANA cloud usage by use type

</td><td>

Software Subscriptions\[samp\_sw\_subscription\]

</td><td>

Number of users by their SAP cloud use type in SAP S/4HANA Public Cloud.

</td></tr></tbody>
</table>**Parent Topic:**[Software Asset Management references](references.md)

