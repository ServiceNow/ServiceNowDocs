---
title: Scripted audits
description: A scripted audit enables users with the certification\_admin role to conduct an audit from a script rather than using restrictive template conditions.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CMDB Compliance, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Scripted audits

A scripted audit enables users with the certification\_admin role to conduct an audit from a script rather than using restrictive template conditions.

A scripted audit uses a [certification filter](c_CertificationFilters.md) to select the records to audit, and then creates standard follow-on tasks for remediation of any discrepancies. Use this type of audit to query for any values or states that a script can define. A scripted audit is a specific audit type that is activated together with the [Desired State](c_DesiredState.md) plugin. ServiceNow provides a sample audit script with configuration instructions.

