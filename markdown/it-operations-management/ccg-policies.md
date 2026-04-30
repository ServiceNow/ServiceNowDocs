---
title: Cloud Configuration Governance policies
description: Cloud Configuration Governance policy defines the non-compliant configurations for a given cloud resource type.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using Cloud Configuration Governance, Cloud Configuration Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Cloud Configuration Governance policies

Cloud Configuration Governance policy defines the non-compliant configurations for a given cloud resource type.

Each Cloud Configuration Governance policy contains the following information:

-   The cloud on which the resource is provisioned.
-   The cloud resource type.
-   Definition of the non-compliant configuration. For example, unencrypted Amazon Web Services \(AWS\) S3 buckets or insecure Identity and Access Management \(IAM\) accounts.
-   Definition of the audit violation \(policy violation\) report.

**Note:** Starting with Cloud Configuration Governance version 1.3.7, the base system contents are moved to the CCG Content Pack. Install the CCG Content Pack to access the base system Cloud Configuration Governance contents.

Cloud Configuration Governance provides several base system policies. You can either use these policies or create custom policies as per the needs of your organization. Depending on the need and your familiarity with the ServiceNow AI Platform, you can use any one of the following methods to create the policy:

-   [Create a policy with the condition builder](../task/ccg-create-policy-condition-builder.md)
-   [Create a policy with Integration Hub flow](../task/ccg-create-policy-ih-subflow.md)
-   [Create a policy through script](../task/ccg-create-policy-through-script.md)

To use the policy, add the policy to a policy set. Each policy set can contain one or more policies. For more information on creating policy sets, see [Create policy set](../task/create-ccg-policy-set.md).

<table id="table_gdl_j2v_3sb"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AWS IAM User Activity policy

</td><td>

Condition builder

</td><td>

Policy to check if the password is enabled for the AWS IAM user.To use this policy, ensure that the AWS IAM user account has the following permissions:

-   Iam:GetCredentialReport
-   Iam:GenerateCredentialReport

</td></tr><tr><td>

AWS S3 Enforce Bucket encryption

</td><td>

Condition builder

</td><td>

Policy to check if the AWS S3 buckets are encrypted.

</td></tr><tr><td>

AWS Sample flow policy

</td><td>

Integration Hub flow

</td><td>

Policy to illustrate an Integration Hub flow-based policy.

</td></tr><tr><td>

AWS VM HardwareType

</td><td>

Condition builder

</td><td>

Policy to check if the deployed EC2 VMs are using only the approved hardware types.

</td></tr><tr><td>

AWS VM IPAddress

</td><td>

Script

</td><td>

Policy to check if the IP address of the EC2 VM is matching with the Configuration Management Database \(CMDB\) record.

</td></tr><tr><td>

AWS VM Monitoring State

</td><td>

Condition builder

</td><td>

Policy to check if detailed monitoring is enabled for the EC2 VM.

</td></tr><tr><td>

Azure VM HardwareType

</td><td>

Condition builder

</td><td>

Policy to check if the deployed Azure VMs are using only the approved hardware types.

</td></tr><tr><td>

Azure VM IP Address

</td><td>

Script

</td><td>

Policy to check if the IP address of the Azure VM is matching with the CMDB record.

</td></tr><tr><td>

Azure VM Monitoring State

</td><td>

Condition builder

</td><td>

Policy to check if detailed monitoring is enabled for the Azure VM.

</td></tr></tbody>
</table>