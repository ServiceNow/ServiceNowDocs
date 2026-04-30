---
title: Read-only roles for Financial Management - Legacy
description: You can restrict the level of access of your users with a read-only role that enables them to view the Financial Management \(FM\) dashboards. Users with the read-only role can view FM reports and the underlying tables that provide data.
locale: en-US
release: yokohama
product: Financial Management
classification: financial-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Financial Management - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Read-only roles for Financial Management - Legacy

You can restrict the level of access of your users with a read-only role that enables them to view the Financial Management \(FM\) dashboards. Users with the read-only role can view FM reports and the underlying tables that provide data.

## Plugin information

If you are a new customer, the Read only roles for PPM Standard \(com.snc.pmo\_read\_roles\) plugin is activated on zBoot. However, you also require Financial Management For APM \(com.snc.financial\_management\_for\_apm\) plugin, which activates Performance Analytics – Content Pack – Financial Management for Application Portfolio Management \(com.snc.pa.fm.apm\) plugin. With this plugin you can access the FM APM dashboards.

## Why read-only roles for FM

Read only roles for Financial Management \(sn\_itfm\_read\) is available when Read only roles for PPM Standard plugin \(com.snc.pmo\_read\_roles\) is activated. Users with this role can access dashboards and view reports in Financial Management for Application Portfolio Management. To assign user roles, including read-only roles, see [assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

## Dashboards accessible to users with FM read role

Following are the dashboards available for users with the read-only role:

-   Financial Management Application TCO dashboard
-   Costing for Business Applications dashboard
-   CIO dashboard

## Tables accessible to users with FM read role

Following are the Financial Management tables that the users with the FM read role can access:

|Label|Table name|
|-----|----------|
|Cost Allocation Aggregate|itfm\_allocation\_aggregate|
|Cost Allocation|itfm\_allocation|
|Financial Model|itfm\_cost\_model|
|Bucket|itfm\_bucket|
|Segment Definition|itfm\_ca\_segment\_map|
|IT Shared Service|itfm\_shared\_service|
|Cost Allocation Breakdown Aggregate|itfm\_allocation\_breakdown|

**Parent Topic:**[Financial Management - Legacy](../concept/c_ITFinance.md)

