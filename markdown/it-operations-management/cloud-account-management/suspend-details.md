---
title: Suspend account configuration fields
description: Suspend the account configuration form and related list field descriptions.
locale: en-US
release: yokohama
product: Cloud Account Management
classification: cloud-account-management
topic_type: reference
last_updated: "2024-09-04"
reading_time_minutes: 1
breadcrumb: [Cloud Account Management reference, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Suspend account configuration fields

Suspend the account configuration form and related list field descriptions.

<table id="table_cct_w5k_2bc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cloud provider

</td><td>

Name of the cloud provider platform. The entries are retrieved from the CMDB records.

</td></tr><tr><td>

Cloud organization

</td><td>

The cloud organization that creates the subscription account.

</td></tr><tr><td>

Name

</td><td>

A name to identify the configuration.

</td></tr><tr><td>

Cloud credential alias

</td><td>

The cloud credential alias that you had configured. The entries are populated from the CMDB records.

</td></tr><tr><td>

Suspension SCP policy ID \(applicable only for AWS\)

</td><td>

The AWS suspension policy ID. This policy ID is used to suspend the AWS account. Service control policies limit the resources, services, and API operations.

 To configure AWS suspend policy, see [Set up suspension of an AWS account using service control policy](../task/configure-suspension-policy.md).

</td></tr><tr><td>

Azure suspension policy ID \(applicable only for Azure\)

</td><td>

The Azure suspension policy ID. This policy ID is used to suspend the Azure account. Service control policies limit the resources, services, and API operations.

 To configure Azure suspend policy, see [Set up suspension of a subscription using Azure policy](../task/configuring-lock-unlock-policy-for-azure.md).

</td></tr><tr><td>

Description

</td><td>

Information that can be recorded in work notes.

</td></tr></tbody>
</table>To return to the procedure, see [Suspend a Cloud account](../concept/suspend-account.md).

**Parent Topic:**[Cloud Account Management reference](cam-reference.md)

