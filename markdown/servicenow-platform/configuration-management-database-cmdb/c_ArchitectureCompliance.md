---
title: Architecture Compliance
description: Architecture Compliance manages scheduled or on-demand audits of CMDB data to determine which configuration items \(CI\) match expected attributes. The compliance audits check servers to ensure that their physical resources, such as CPU speed or memory, comply with certain standards.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CMDB Compliance, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Architecture Compliance

Architecture Compliance manages scheduled or on-demand audits of CMDB data to determine which configuration items \(CI\) match expected attributes. The compliance audits check servers to ensure that their physical resources, such as CPU speed or memory, comply with certain standards.

The compliance process checks servers to ensure that their resources, such as CPU speed or memory, comply with standards set by your organization. Audit reports show any discrepancies in the attributes of the target CIs, and ServiceNow automatically assigns follow-on tasks to qualified users who can remediate those discrepancies.

The administrator responsible for compliance checking creates template definitions of expected attributes and then schedules an audit to check CIs for compliance. The audit results identify CIs that pass certification and itemize the discrepancies in those CIs that fail. ServiceNow automatically generates and assigns follow-on tasks to track the process of getting the CIs back into compliance. Users with the admin role activate Architecture Compliance.

## Architecture Compliance roles

To access or configure certification elements, a user must have the certification\_admin role. These users can create, update, and delete filters if they have the proper access to necessary tables.

In the base system, certification\_admin users have limited system rights and do not have access to all the necessary tables. When assigning compliance resources, make sure to grant additional roles to the certification\_admin user as needed. For example, the certification administrator needs roles that grant access to these tables:

-   Company `[core_company]`
-   Cost Center `[cmn_cost_center]`
-   Schedule `[cmn_schedule]`

## Architecture Compliance Process

Perform these tasks in this order to certify configuration items with Architecture Compliance.

1.  Create a filter.

    Create a filter that defines a subset of configuration items to certify. You can create multiple versions of a filter, and then activate the version you want to use for compliance checking. Architecture compliance only supports filters on the Configuration Item \[cmdb\_ci\] table and all tables that extend it.

2.  Create a template.

    Create template conditions using values from reference fields in a related list or conditions that define the expected physical attributes of each CI in an audit. The template uses a filter to determine which configuration items the system examines based on these conditions.

3.  Create and run an audit.

    Create and schedule an audit or run an audit on demand. The audit generates a set of results based on the conditions in the template you specify.

4.  View audit results.

    View the audit results which display any discrepancies between the expected state, as expressed by the template conditions, and the actual state of the target configuration items.

5.  Correct discrepancies.

    Correct the discrepancies the audit found by completing the follow-on tasks created by the system.


