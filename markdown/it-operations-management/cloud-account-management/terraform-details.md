---
title: Terraform account configuration fields
description: Terraform account configuration form and related list field descriptions.
locale: en-US
release: yokohama
product: Cloud Account Management
classification: cloud-account-management
topic_type: reference
last_updated: "2024-03-07"
reading_time_minutes: 1
breadcrumb: [Cloud Account Management reference, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Terraform account configuration fields

Terraform account configuration form and related list field descriptions.

<table id="table_ul3_hgy_w1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Provision mode

</td><td>

Name of the provision mode. Here it should be Terraform.

</td></tr><tr><td>

Cloud provider

</td><td>

The name of the cloud provider platform. Currently, only AWS is supported.

</td></tr><tr><td>

Cloud organization

</td><td>

The cloud organization where the subscription account is created.

</td></tr><tr><td>

Name

</td><td>

A name to identify the configuration.

</td></tr><tr><td>

Root email

</td><td>

Cloud Account Management uses an email address to generate the root email ID for newly created account.

 For example, if your root email ID is myawsaccount@example.com, the Cloud Account Management application appends a request ID to generate myawsaccount-CWSAREQ0000001@example.com.

 **Note:** To create a root email, see [Set up and verify root email in AWS](../task/aws-setup.md).

</td></tr><tr><td>

Terraform URL

</td><td>

A default URL appears. You can customize the URL by selecting the ![Edit](../../service-mapping/image/EvalEditIcon.png) icon.

</td></tr><tr><td>

Terraform OAuth Token ID

</td><td>

The OAuth token ID provided when you configured the VCS provider in Terraform.

</td></tr><tr><td>

Terraform credentials

</td><td>

The Terraform credentials that you had configured. The entries are populated from the CMDB records.

</td></tr><tr><td>

Terraform organization

</td><td>

The Terraform organization name used as a workspace to create a subscription.

</td></tr><tr><td>

VCS identifier

</td><td>

GitHub \(or Version Control System \(VCS\)\) location of the Terraform template.

</td></tr><tr><td>

Description

</td><td>

Option to provide a description for the Terraform account.

</td></tr></tbody>
</table>To return to the procedure, see [Create a Terraform account configuration](../task/create-terraform-account-config.md).

**Parent Topic:**[Cloud Account Management reference](cam-reference.md)

