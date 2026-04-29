---
title: Exploring CMDB Coverage
description: Learn about CMDB Coverage and review the benefits it can provide for users in your organization.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [explore]
breadcrumb: [CMDB Coverage, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Exploring CMDB Coverage

Learn about CMDB Coverage and review the benefits it can provide for users in your organization.

## CMDB Coverage overview

Organizations often can't identify whether their CMDB data is complete despite using discovery tools because the discovery data and IPAM data aren't correlated. CMDB Coverage provides an automated solution that continuously measures CMDB discovery completeness by correlating IP addresses from IPAM systems with discovered configuration items \(CIs\).

The CMDB Coverage application includes the following features:

-   Reconciliation and correlation of IPAM data with discovered configuration items \(CIs\).
-   Identification of missing data and highlighting the gaps in IP address coverage to ensure compliance with enterprise standards.
-   Continuous coverage tracking.
-   Discovery schedule gap detection, where the IPAM subnet data is compared to the scheduled discovery ranges \(IPv4 and IPv6 addresses\) to identify missing scheduled discovery ranges.


## Supported versions

Supported ServiceNow versions:

-   Zurich
-   Australia

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## CMDB Coverage users

<table id="table_byq_5fv_l3c"><thead><tr><th>

User role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_cmdb\_admin

</td><td>

Users with the sn\_cmdb\_admin role can configure the application. These users can create, read, write, and delete records in the following tables:-   CMDB Coverage Initialization Tracker \[sn\_cmdb\_ip\_cov\_init\_tracker\]
-   Binary IP Address \[sn\_cmdb\_ip\_cov\_binary\_ip\_address\]
-   IP Coverage CI Table Configuration \[sn\_cmdb\_ip\_cov\_ci\_config\]
-   IP Address Staging \[sn\_cmdb\_ip\_cov\_ip\_staging\]
-   Discovery schedule gap \[sn\_cmdb\_ip\_cov\_discovery\_schedule\_gap\]
-   Discovery schedule gaps to allocated IP \[sn\_cmdb\_ip\_cov\_m2m\_discovery\_schedule\_gap\]

**Note:** The sn\_cmdb\_ip\_cov\_m2m\_discovery\_schedule\_gap table is not populated by default. For information about how to populate data in this table, see [Custom system property](../reference/cmdb-coverage-properties.md#section_d4d_xmw_l3c).


</td></tr><tr><td>

sn\_cmdb\_user

</td><td>

Users with the sn\_cmdb\_user role can read the data in the tables and view the dashboard.​

</td></tr></tbody>
</table>## CMDB Coverage benefits

<table id="table_qg4_j14_l3c"><thead><tr><th>

Benefit

</th><th>

Feature

</th></tr></thead><tbody><tr><td>

Identify potential gaps between IPAM data and what is scheduled to be discovered in the configured discovery tools.

</td><td>

[Find missing IPAM IP addresses in discovery](../reference/cmdb-coverage-scheduled-jobs.md#section_hyl_mpv_l3c)

</td></tr><tr><td>

Understand the completeness of the CMDB discovery data.

</td><td>

[Reconcile and correlate IPAM data with discovered CIs](../reference/cmdb-coverage-scheduled-jobs.md#section_m5f_xtv_l3c)

</td></tr><tr><td>

Identify the number of free, reserved, and allocated IP addresses per subnet.

</td><td>

[Analyze IP address usage per subnet](../reference/cmdb-coverage-scheduled-jobs.md#section_l1x_c5v_l3c)

</td></tr></tbody>
</table>## CMDB Coverage dashboard

The CMDB Coverage dashboard provides the following information:

-   **Infrastructure coverage**: The percentage of allocated IP addresses that are associated with CIs in the CMDB. The total coverage count and coverage gap count are displayed.
-   **IP-to-CI association**​: Breakdown of how allocated IP addresses map to CMDB CIs. The distribution across single match, multiple matches, and no match categories are displayed.
-   **Discovery schedule gap count**​: The number of allocated IP addresses that exist in IPAM but are not covered by any active discovery schedule.
-   **Network coverage**
    -   **Total number of networks**: The number of operational managed networks that are configured in the CMDB.
    -   **Total number of subnets**​: The number of operational IP network subnets that are defined in the CMDB.
    -   **Total number of IP address​es**: The number of allocated IP addresses that are imported from IPAM sources.
-   **Discovery schedule gap**
    -   **Missing IP addresses \(Allocated IPs without discovery schedule\)**: The number of allocated IP addresses from IPAM that are not covered by any active discovery schedule, indicating potential gaps in discovery coverage.
    -   **Percentage of missing IP addresses**: The percentage of total allocated IP addresses that lack discovery schedule coverage.

## What to explore next

To learn more about configuring and using CMDB Coverage, see:

-   [Configure CMDB Coverage](../task/cmdb-coverage-configure-initialize.md)
-   [Using CMDB Coverage dashboard](cmdb-coverage-use.md)
-   [CMDB Coverage reference](cmdb-coverage-reference.md)

