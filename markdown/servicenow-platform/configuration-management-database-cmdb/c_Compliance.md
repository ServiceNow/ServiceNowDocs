---
title: CMDB Compliance
description: CMDB Compliance is a tool set that enables administrators to certify CMDB data for correctness and fix any discrepancies found in the data.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB Compliance

CMDB Compliance is a tool set that enables administrators to certify CMDB data for correctness and fix any discrepancies found in the data.

**Note:** For compliance in the context of internal business goals and objectives, and external legislation and regulations, see [Exploring Policy and Compliance Management](https://www.servicenow.com/docs/access?context=policy-compliance&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US).

## Certification options

CMDB Compliance offers these certification options to suit the size and requirements of your organization:

|Option|Description|
|------|-----------|
|Desired State|Automatically compares the actual attributes and relationships of specific ServiceNow records against the desired states for those records. For example, an audit can detect a Linux database server with insufficient RAM or whose Depends on relationships with another CI is incorrect. The system then publishes any discrepancies found and automatically assigns follow-on tasks to qualified users to bring that server into compliance.|
|Architecture Compliance|Automatically compares the actual attributes of specific CIs, such as CPU count, RAM, or disk size against the expected attributes for those CIs. The system publishes any discrepancies found and automatically assigns remediation tasks to qualified users.|

## Compliance Templates and Audits

The Templates and Audits modules on the top level of the Compliance menu enable a certification\_admin user to create, edit, and delete all template and audit types.

You can use Compliance Templates and Audits to evaluate records for any table in the ServiceNow system, not just those tables extending the Configuration Item `[cmdb_ci]` table. Compliance audits certify record attributes only. Compliance templates can be used in Control Test Definitions in Governance Risk and Compliance.

