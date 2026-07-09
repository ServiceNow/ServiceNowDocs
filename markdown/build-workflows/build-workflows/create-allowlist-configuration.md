---
title: Create an allowlist configuration
description: Manage access to specific tables by specifying the additional user roles necessary to create an intelligent approval on a specific table.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-07-01"
reading_time_minutes: 1
---

# Create an allowlist configuration

Manage access to specific tables by specifying the additional user roles necessary to create an intelligent approval on a specific table.

## Before you begin

Role required: sn\_iap.policy\_admin

## About this task

By default, the sn\_iap.policy\_manager role grants intelligent approvals access to all tables. If you want to prevent policy manager users from creating intelligent approvals on specific tables, you can create an allowlist configuration to require the sn\_iap.policy\_admin user role instead.

## Procedure

1.  Navigate to **All** &gt; **Intelligent Approvals** &gt; **Allowlist Configurations**.

2.  From the list controls, select **New**.

3.  Specify the configuration details.

    \[Omitted image "create-allowlist-config-01.png"\] Alt text: Sample allowlist configuration details

    |Field|Description|
    |-----|-----------|
    |Description|Summary of the table or roles needed to grant access to intelligent approvals.|
    |Role|User role needed to grant intelligent approvals access to the specified table. For example, select sn\_iap.policy\_admin to prevent users who only have the sn\_iap.policy\_manager role from creating intelligent approvals for a specific table.|
    |Active|Option to enable or disable the allowlist configuration.|
    |Table Name|Table that you want to control access to using the specified user role. For example, select change\_request to require the specified user role to access the Change Request table.|
    |Condition|Query string used to determine when to apply the allowlist configuration. By default this field is read-only.|

4.  Select **Submit**.

    \[Omitted image "create-allowlist-config-02.png"\] Alt text: Sample allowlist configuration to restrict access to the Change Request table to policy admin users


## Result

\[Omitted image "allowlist-not-configured.png"\] Alt text: Error message when creating intelligent approval

Only users with the specified user role \(usually sn\_iap.policy\_admin\) can create intelligent approvals on the specified table. Users without the required role see an error message when they attempt to create an intelligent approval on an access-restricted table.

