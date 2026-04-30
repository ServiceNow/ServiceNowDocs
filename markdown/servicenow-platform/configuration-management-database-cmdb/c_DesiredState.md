---
title: Desired State
description: Desired State performs scheduled or on-demand audits of CMDB data to determine which records match the expected attributes, CI relationships, and relationships to other records in the system.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [CMDB Compliance, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Desired State

Desired State performs scheduled or on-demand audits of CMDB data to determine which records match the expected attributes, CI relationships, and relationships to other records in the system.

For example, desired state can determine if a computer has a license for a particular software program. The compliance process checks configuration items \(CI\) to ensure that their attributes and relationships comply with standards set by your organization. Audit results show any discrepancies in the desired state of a record, and ServiceNow automatically assigns follow-on tasks to qualified users who can remediate those discrepancies.

## Desired State roles

To access or configure certification elements, a user must have the certification\_admin role. These users can create, update, and delete filters if they have the proper access to necessary tables.

In the base system, certification\_admin users have limited system rights and do not have access to all the necessary tables. When assigning compliance resources, make sure to grant additional roles to the certification\_admin user as needed. For example, the certification administrator requires roles that grant access to these tables:

-   Company \[`core_company`\]
-   Cost Center \[`cmn_cost_center`\]
-   Schedule \[`cmn_schedule`\]

## Desired State process

The desired state certification process can mean checking servers to ensure that their physical resources, such as CPU speed or memory, comply with certain standards. This process also ensures that all critical business services have a manager, support group, and approval group assigned.

The administrator responsible for certification creates definitions of desired states and then schedules an audit to check CIs for compliance. The audit results identify CIs that pass certification and itemize the discrepancies in those CIs that fail. The ServiceNow system automatically generates follow-on tasks to track the process of adjusting the CIs to the desired state.

Desired state differs substantially from data certification. Data certification is a manual process to ensure that your data matches reality. Desired state examines the same data and determines when the configuration of each item is in the desired and approved state.

1.  Create a certification filter: Create a filter that defines a subset of configuration items to certify. You can create multiple versions of a filter, and then activate the version you want to use for certification. You can create filters on the Configuration Item \[`cmdb_ci`\] table and all tables that extend it.
2.  Create a template: Create a template with conditions that define the desired state of the physical attributes, related records, and relationships for a CI. The certification filter you select for the template determines which configuration items the system examines.
3.  Create and run an audit: Create an audit using the template. Set the audit to run on a schedule or on demand. The audit generates a set of results based on the conditions from the template you specify. Determine usage of follow-on tasks:
    -   Determine if the audit creates follow-on tasks and assignment.
    -   Determine if the same follow-on task is used for the same audit failure across multiple runs. The system property **glide.allow.new.cert\_follow\_on\_task** is set to true by default, allowing for new follow on tasks to be created for the same failure, at each audit run \(this system property applies only to audits that aren't scripted\).
4.  View audit results: View the audit results which display any discrepancies between the desired state, as specified by the template, and the actual state of the target configuration items.
5.  Correct discrepancies: Correct the discrepancies the audit found by completing the follow-on tasks created by the system.

