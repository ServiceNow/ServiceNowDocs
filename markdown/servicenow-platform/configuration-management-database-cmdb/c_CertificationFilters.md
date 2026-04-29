---
title: Certification filters
description: A certification filter creates a subset of ServiceNow records to audit, typically from configuration items \(CI\) of a certain type, such as all UNIX servers in a specific datacenter.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CMDB Compliance, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Certification filters

A certification filter creates a subset of ServiceNow records to audit, typically from configuration items \(CI\) of a certain type, such as all UNIX servers in a specific datacenter.

However, you can define a filter for any ServiceNow table by using any set of system-supported conditions. Audited records identified by a filter for expected attributes or relationships, depending on the audit type.

You can create multiple versions of a filter, reactivate inactive versions, and select the version you want to use in a template or a certification schedule. Only the active versions of a filter are available for selection in template records. You can use a single filter for multiple certification templates or schedules.

|Filter|Description|
|------|-----------|
|Data Certification|Validates CMDB data.|
|Architecture Compliance|Manages reviews of CMDB data in architecture compliance audits to determine which configuration items \(CIs\) match expected attributes.|
|Desired State|Manages reviews of CMDB data to determine which CIs match a desired state for both attributes and relationships.|
|Compliance|Manages reviews of records from any ServiceNow table to determine which records match an expected set of attributes and related record conditions.|
|IT Governance Risk and Compliance|Generates audits and tests to ensure that controls are being followed and creates tasks to track corrective actions.|

## Roles

In the base ServiceNow system, users with the certification\_admin role have limited system rights and do not have access to the tables required for creating a filter.

When assigning compliance resources, make sure certification\_admin users have any additional roles they need. For example, a user requires roles that grant access to the Company `[core_company]` table.

