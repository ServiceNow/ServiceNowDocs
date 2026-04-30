---
title: Business process roles
description: Various roles are available for business process users and managers.
locale: en-US
release: yokohama
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Reference, Risk Management, Governance, Risk, and Compliance]
---

# Business process roles

Various roles are available for business process users and managers.

The following table lists the roles that you must use for managing your business processes.

<table id="table_stw_1mk_ctb"><thead><tr><th>

Role title

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Business process administrator business\_process\_admin

</td><td>

This role provides create, read, update, and delete \(CRUD\) access to all records and their relationships in the business process. This role is assigned to users who are administrators and have thorough information and training on business processes. In the context of GRC, users with the sn\_grc.admin role who manage GRC applications and their setup automatically gain access to this role. This access enables the GRC administrators to administer business process and its records similar to other GRC tables.

</td></tr><tr><td>

Business process manager business\_process\_manager

</td><td>

This role is assigned to business process managers who are usually specialists and manage multiple business processes in the organisation. They can create, read and update any business process and manage the relationship of business process with other records. Such users generally work with other employees and are experts around business processes. In the context of GRC, users with the sn\_grc.manager role automatically inherit this role that enables them to manage the business processes for the entire organization.

</td></tr><tr><td>

Business process userbusiness\_process\_user

</td><td>

This role must be assigned to the respective process owners who manage the business process that they own. With this role, they can update the business processes that they own and can also read any business process. This role can also be provided to users who are required to view the business processes in the organization and understand them better. In the context of GRC, users with the sn\_risk.user role are automatically assigned this role as this role enables them to manage the business processes they own as well as read all business processes.

</td></tr></tbody>
</table>**Parent Topic:**[Risk Management reference](../reference/risk-management-reference.md)

