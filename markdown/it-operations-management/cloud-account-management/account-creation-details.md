---
title: New cloud account request fields
description: New cloud account request form and related list field descriptions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/cloud-account-management/account-creation-details.html
release: zurich
product: Cloud Account Management
classification: cloud-account-management
topic_type: reference
last_updated: "2026-06-09"
reading_time_minutes: 2
breadcrumb: [Reference, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
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

Auto-generated name derived from the cost center, business unit, business application, and suffix values. Special characters are automatically removed.

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
</table>**Note:** For AWS and AWS GovCloud accounts, the values entered in the **Cost center**, **Business Unit**, **Department**, **Project/Application service**, **Business application**, and **Environment** fields are synced to AWS as tags. AWS restricts tag values to letters, numbers, spaces, and the following special characters: `+ - = . _ : / @`. Any other characters are automatically replaced with spaces. If all characters in a field value are unsupported, the tag is skipped. A tooltip on the form indicates this behavior. These actions are recorded in the execution log.

To return to the procedure, see [Request a cloud account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/cloud-account-management/request-account.md).

**Parent Topic:**[Cloud Account Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/cloud-account-management/cam-reference.md)

