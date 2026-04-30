---
title: CMDB Coverage scheduled jobs
description: CMDB Coverage uses scheduled jobs to identify stale and missing data.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2026-03-02"
reading_time_minutes: 2
breadcrumb: [Reference, CMDB Coverage, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB Coverage scheduled jobs

CMDB Coverage uses scheduled jobs to identify stale and missing data.

To view the list of scheduled jobs, enter `sysauto_script.list` in the navigation filter.

## PopulateBinaryTable

The **PopulateBinaryTable** scheduled job is a one-time initialization job that processes the historical records that existed before the CMDB Coverage was configured. All historical IP addresses \(IPv4 addresses\) are converted into binary format for fast matching. The records are added to the Binary IP Address \[sn\_cmdb\_ip\_cov\_binary\_ip\_address\] table. IPv6 addresses are processed as is.

## InitializeAllocatedIPTable

The **InitializeAllocatedIPTable** scheduled job is another one-time initialization job that runs after the **PopulateBinaryTable** job. This scheduled job performs the following tasks and populates records in the CMDB Coverage Initialization Tracker \[sn\_cmdb\_ip\_cov\_init\_tracker\] table:

-   Processes the historical records in the Allocated IP Address \[cmdb\_ci\_allocated\_ip\_address\] table.
-   Updates the value of the `ci_match_status` attribute for the records in the Allocated IP Address \[cmdb\_ci\_allocated\_ip\_address\] table.
-   Creates relationships between the discovered CIs and the records in the Allocated IP Address \[cmdb\_ci\_allocated\_ip\_address\] table. That is, corresponding records are created in the CMDB \[cmdb\_ci\_rel\] table.

The possible values of the `ci_match_status` attribute are:

-   none: No CI matches the IP​ address, which indicates a discovery gap.
-   single: Exactly one CI matches​ the IP address.
-   multiple: Multiple CIs match​ the IP address.
-   not\_evaluated: The record isn’t processed yet.

## ProcessStagingTable

The **ProcessStagingTable** scheduled job processes the records that are created by the DB Listener after the CMDB Coverage application is configured.

You can configure the list of tables that the DB Listener should monitor in the IP Coverage CI Table Configuration \[sn\_cmdb\_ip\_cov\_ci\_config\] table. The `Validate IP Coverage CI Config` business rule validates the records that are created in the IP Coverage CI Table Configuration \[sn\_cmdb\_ip\_cov\_ci\_config\] table to verify that only the IP address field is updated.

The DB Listener performs the following tasks:

-   Detects real-time changes in IP address information.
-   Monitors the tables that are configured in the IP Coverage CI Table Configuration \[sn\_cmdb\_ip\_cov\_ci\_config\] table.
-   Identifies new and updated IP addresses and creates corresponding records in the IP Address Staging \[sn\_cmdb\_ip\_cov\_ip\_staging\] table.
-   Pushes changes to the Allocated IP Address \[cmdb\_ci\_allocated\_ip\_address\] table.

The Platform DB Listener doesn’t rely on polling. Therefore, all updates to IP addresses are identified.

The **ProcessStagingTable** scheduled job identifies the new records that were added by the DB Listener to the IP Address Staging \[sn\_cmdb\_ip\_cov\_ip\_staging\] table. Subsequently, the `ci_match_status` attribute in the Allocated IP Address \[cmdb\_ci\_allocated\_ip\_address\] table is updated for all new records.

## SubnetUsageCount

This daily scheduled job tracks subnet usage. Based on the value of the `ci_match_status` attribute in the Allocated IP Address \[cmdb\_ci\_allocated\_ip\_address\] table, the **SubnetUsageCount** scheduled job counts the number of free IP addresses, allocated IP addresses, and reserved IP addresses for each subnet.​

## Find missing IPAM ips in discovery

IPAM-managed networks, subnets, and allocated IP addresses are managed separately from the configured discovery ranges and schedules of organizations. This often leads to stale and missing data \(such as IP address ranges that are never scanned\) in the CMDB.

The **Find missing IPAM ips in discovery** scheduled job compares the IPAM data \(networks, subnets, and allocated IP addresses\) and the configured discovery ranges and schedules \(IPv4 and IPv6 addresses\) to identify gaps in IP address coverage, such as missing IPv4 address ranges and the number of IPAM IP addresses that don't have a discovery schedule. The data about gaps in IP address coverage is added to the Discovery schedule gap \[sn\_cmdb\_ip\_cov\_discovery\_schedule\_gap\]​ table, and is then available for operational review.

**Parent Topic:**[CMDB Coverage reference](../concept/cmdb-coverage-reference.md)

