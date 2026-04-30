---
title: Cloud Configuration Governance Service Account Assume Role Config form
description: The Cloud Configuration Governance Service Account Assume Role Config form displays detailed information about the assume role configuration used to access the trusting account.
locale: en-US
release: zurich
product: ITOM Cloud Accelerate
classification: itom-cloud-accelerate
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Cloud Configuration Governance reference, Cloud Configuration Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Cloud Configuration Governance Service Account Assume Role Config form

The Cloud Configuration Governance Service Account Assume Role Config form displays detailed information about the assume role configuration used to access the trusting account.

<table id="table_qvb_hzm_h5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Access Role Name

</td><td>

Name of the Identity and Access Management \(IAM\) role created for the trusting account that allows the trusted account \(accessor\) to access the trusting account.To scan the member accounts by using the management account, enter OrganizationAccountAccessRole in this field. If you don't want to use the OrganizationAccountAccessRole to access the member account, enter the name of the IAM role created for the member account.

 To scan the trusting account by using the trusted account, enter the name of the IAM role created for the trusting account.

</td></tr><tr><td>

Service Account

</td><td>

Name of the service account where assume role exists.

</td></tr><tr><td>

Role Session Name

</td><td>

An identifier for the assumed role session.Do not change the default value.

</td></tr><tr><td>

Credential Alias

</td><td>

Optional: Credential alias for the AWS credential.

</td></tr></tbody>
</table>**Parent Topic:**[Cloud Configuration Governance reference](ccg-reference.md)

