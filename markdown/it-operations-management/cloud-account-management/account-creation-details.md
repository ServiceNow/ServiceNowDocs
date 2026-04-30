---
title: New cloud account request fields
description: New cloud account request form and related list field descriptions.
locale: en-US
release: yokohama
product: Cloud Account Management
classification: cloud-account-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Cloud Account Management reference, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# New cloud account request fields

New cloud account request form and related list field descriptions.

<table id="simpletable_rbp_cr5_vzb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Environment

</td><td>

Name of the environment.

</td></tr><tr><td>

This is a GovCloud account \(applicable only for AWS\)

</td><td>

Check-box to request an AWS GovCloud account.

</td></tr><tr><td>

Desired cloud provider

</td><td>

Name of the cloud provider platform such as AWS or Azure.

</td></tr><tr><td>

Cloud account name suffix

</td><td>

Suffix a name for easier tracking.

</td></tr><tr><td>

Cloud account name

</td><td>

Auto-populated cloud account name.

</td></tr><tr><td>

Monthly Budget Limit

</td><td>

Monthly budget for this account. **Note:**

If the budget threshold is reached, an email alert is sent to the root user of the AWS organization account and owner of the newly created account.

Even if the threshold is exceeded, there are no restrictions in accessing the account but you can’t create resources for the suspended account.

</td></tr><tr><td>

Project/ application service

</td><td>

The project or application to associate with this account.

</td></tr><tr><td>

Cost center

</td><td>

Cost center to associate with this account.

</td></tr><tr><td>

Business Unit

</td><td>

Business unit to associate with this account.

</td></tr><tr><td>

Department

</td><td>

Department to associate with this account.

</td></tr><tr><td>

Business application

</td><td>

Business application to associate with this account.

</td></tr><tr><td>

Tags

</td><td>

Key-value information to categories the account. For example, by region, country, organization, or a branch.

</td></tr><tr><td>

Account owner

</td><td>

Owner of this account.

</td></tr><tr><td>

Propagate ownership to cloud assets.

</td><td>

The account owner information is propagated to all assets for this account.

</td></tr><tr><td>

Primary teams

</td><td>

The teams that will manage the account and assets, acting as the responsible party when the owner is absent.

</td></tr><tr><td>

Secondary teams

</td><td>

The secondary team that will support the account.

</td></tr></tbody>
</table>To return to the procedure, see [Request a cloud account](../task/request-account.md).

**Parent Topic:**[Cloud Account Management reference](cam-reference.md)

