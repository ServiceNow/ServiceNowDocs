---
title: Intelligent approval system properties
description: Configure how the system processes intelligent approvals.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-07-01"
reading_time_minutes: 1
---

# Intelligent approval system properties

Configure how the system processes intelligent approvals.

These properties are available for intelligent approvals.

To set intelligent approvals system properties, navigate to the System Properties \[sys\_properties\] table.

<table id="table_v5g_nzp_jdb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_iap.enable\_allowlist

</td><td>

Option to restrict intelligent approval access to approval tables and catalog items to only users with a specific role. When true, the system restricts access to approval tables based on an allowlist configuration record. When false, the system allows access to all approval tables and catalog items.-   Type: true \| false
-   Default value: false
-   Location: Add to the System Properties \[sys\_properties\] table
-   More information: [Create an allowlist configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/create-allowlist-configuration.md)

</td></tr></tbody>
</table>