---
title: New cloud account request fields
description: New cloud account request form and related list field descriptions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/cloud-account-management/account-creation-details.html
release: australia
product: Cloud Account Management
classification: cloud-account-management
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Reference, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# New cloud account request fields

New cloud account request form and related list field descriptions.

|Fields|Description|
|------|-----------|
|Environment|Name of the environment.|
|This is a GovCloud account \(applicable only for AWS\)|Check-box to request an AWS GovCloud account.|
||Name of the cloud provider platform such as AWS or Azure.|
|Account name suffix|Suffix a name for easier tracking.|
|Account name|Auto-generated name derived from the cost center, business unit, business application, and suffix values. Special characters are automatically removed.|
||Monthly budget for this account.|
|Project/ application service|The project or application to associate with this account.|
|Cost center|Cost center to associate with this account.|
|Business Unit|Business unit to associate with this account.|
|Department|Department to associate with this account.|
|Business application|Business application to associate with this account.|
|Tags|Key-value information to categories the account. For example, by region, country, organization, or a branch.|
|Account owner|Owner of this account.|
|Propagate ownership to cloud assets.|The account owner information is propagated to all assets for this account.|

**Note:** For AWS and AWS GovCloud accounts, the values entered in the **Cost center**, **Business Unit**, **Department**, **Project/Application service**, **Business application**, and **Environment** fields are synced to AWS as tags. AWS restricts tag values to letters, numbers, spaces, and the following special characters: `+ - = . _ : / @`. Any other characters are automatically replaced with spaces. If all characters in a field value are unsupported, the tag is skipped. A tooltip on the form indicates this behavior. These actions are recorded in the execution log which you can view in the request details page.

To return to the procedure, see [Request a cloud account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/cloud-account-management/request-account.md).

**Parent Topic:**[Cloud Account Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/cloud-account-management/cam-reference.md)

