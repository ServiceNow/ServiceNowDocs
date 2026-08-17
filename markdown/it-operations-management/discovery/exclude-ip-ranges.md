---
title: Exclude IP ranges from a Discovery range set
description: You can specify a range of IP addresses that you want to exclude from your Discovery query.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/exclude-ip-ranges.html
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Discovery IP address configuration, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Exclude IP ranges from a Discovery range set

You can specify a range of IP addresses that you want to exclude from your Discovery query.

## Before you begin

Before a Discovery schedule is run, the number of excluded IP addresses is totaled. If there are more than 500,000 excluded IP addresses, the Discovery is cancelled and an error is logged through DiscoveryLogger regarding its status.

**Note:** Exclude IPs is not supported for IPv6 ranges or subnets.

Role required: discovery\_admin or agent\_admin

## Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Discovery Range Sets**.

2.  Select one of the range sets.

3.  Select one of the types from the **Discovery IP ranges** related list.

4.  Click **New** from the **Discovery Range Item Excludes** related list.

5.  Choose one of the following options from the **Type** drop-down list.

<table id="choicetable_vp2_g1m_dgc"><thead><tr><th align="left" id="d70183e112">

Option

</th><th align="left" id="d70183e115">

Description

</th></tr></thead><tbody><tr><td id="d70183e121">

**IP Address List**

</td><td>

Enables you to exclude non-consecutive IP addresses by listing individual IP addresses in the **Discovery Range Item IPs** related list.**Note:** After you select **IP Address List** as the **Type**, you must right-click the header and select **Save** before you can begin adding IPs to the related list.

</td></tr><tr><td id="d70183e144">

**IP Address Range**

</td><td>

Enables you to exclude a range of IPs by providing the starting and ending IP addresses.

</td></tr><tr><td id="d70183e153">

**IP Network**

</td><td>

Enables you to exclude an IP network by providing the Network IP and Network mask.

</td></tr></tbody>
</table>6.  Click **Submit**.


