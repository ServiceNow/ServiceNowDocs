---
title: Configure a custom AWS member role
description: Customize the AWS roles that a MID Server can assume to receive temporary credentials for member accounts. You can configure additional parameters to improve security and customize the way that the member account’s role is assumed when discovering cloud resources.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Day 1 setup guide for Amazon Web Services on Cloud Provisioning and Governance, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Configure a custom AWS member role

Customize the AWS roles that a MID Server can assume to receive temporary credentials for member accounts. You can configure additional parameters to improve security and customize the way that the member account’s role is assumed when discovering cloud resources.

## Before you begin

Role required: admin

## About this task

Values that you enter in the Cloud Service Account &gt; AWS Org Assume Role Params \[cloud\_service\_account\_aws\_org\_assume\_role\_params\] table are passed as parameters to the AWS AssumeRole API for the named service account.

## Procedure

1.  Navigate to **All** &gt; **Cloud Provisioning and Governance** &gt; **Organization Access Parameters** &gt; **AWS Org Assume Role Parameters**.

    ![AWS Org Assume Role Parameters module](../image/AWSOrgAssumeRoleModule.png)

2.  Click **New** and then complete the form using these parameters:

<table id="table_cvy_5c3_phb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Access role name \[access\_role\_name\]

</td><td>

Name of the AWS role in the member account which is used by the management account to acquire temporary credentials.Default: OrganizationAccountAccessRole

</td></tr><tr><td>

Role session name \[role\_session\_name\]

</td><td>

Name for the session using the temporary security credentials that may help in distinguishing use of a role by a principal or purpose. This session name is visible in the AWS Cloud Trail logs. See [Cloud API Trail](../concept/cloud-api-trail.md#) and the [AWS documentation](https://aws.amazon.com/documentation/) on AWS Cloud Trail for details.Default: master\_account\_id\_\_&lt;management account ID number&gt; An example of this is: `master_account_id__321003876149`.

</td></tr><tr><td>

Credential TTL in seconds \[credential\_ttl\_seconds\]

</td><td>

Time in seconds for the temporary security credentials to live.Default: Calculated as follows:

1.  Retrieve the value in the **mid.aws.sts.assume\_role.credential\_ttl\_minutes** [MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).
2.  Constrain this value to be between 15 and 720 minutes. If the setting in the property is less than 15 minutes, the system enters 15 minutes. If the setting is greater than 720 minutes, the system enters 720 minutes.
3.  Convert the resulting value into seconds.


</td></tr><tr><td>

External ID \[external\_id\]

</td><td>

Unique identifier required by the trust policy of the role being assumed.Default: ServiceNow\_MID\_Server

</td></tr><tr><td>

Session policy \[session\_policy\]

</td><td>

IAM policy in JSON format that further restricts the permissions of the temporary security credentials beyond the role configured policy. \(JSON in AWS policy language.\)Default: Blank

</td></tr><tr><td>

MFA \[multifactor authentication\]

</td><td>

Serial number of the Multi-Factor Authentication \(MFA\) device \(hardware or virtual\) used to authenticate the management account.Default: Blank

</td></tr><tr><td>

MFA token code \[mfa\_token\_code\]

</td><td>

Token code supplied by the MFA device \(hardware or virtual\) used to authenticate the management account.Default: Blank

</td></tr><tr><td>

Cloud service account \[cloud\_service\_account\]

</td><td>

Required. Service account to associate with the access parameters that you pass to the AWS AssumeRole API. Enter an account ID, either a management account or a member account, from the Service Accounts \[cmdb\_ci\_cloud\_service\_account\] table.

</td></tr></tbody>
</table>    **Note:** For more details on how these parameters are used and what they mean, see the [AWS documentation](https://aws.amazon.com/documentation/) on the AWS Security Token Service API for the AssumeRole action.


