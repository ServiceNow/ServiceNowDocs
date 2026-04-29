---
title: Policy sets
description: The Cloud Configuration Governance policy sets and its policies are listed for your reference.
locale: en-US
release: australia
product: ITOM Cloud Accelerate
classification: itom-cloud-accelerate
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Cloud Configuration Governance reference, Cloud Configuration Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Policy sets

The Cloud Configuration Governance policy sets and its policies are listed for your reference.

<table id="table_lfb_w5s_52c"><thead><tr><th>

Policy Set Name

</th><th>

Policies

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AWS 1.4.0

</td><td>

Ensure IAM Users Receive Permissions Only Through Groups \(Automated\)

 Ensure no Network ACLs allow ingress from 0.0.0.0/0 to remote server administration ports \(Automated\)

 Ensure IAM password policy requires minimum length of 14 or greater \(Automated\)

 Ensure a support role has been created to manage incidents with AWS Support \(Automated\)

 Eliminate use of the 'root' user for administrative and daily tasks \(Automated\)

 Ensure hardware MFA is enabled for the 'root' user account \(Automated\)

 Ensure that Object-level logging for write events is enabled for S3 bucket \(Automated\)

 Ensure access keys are rotated every 90 days or less \(automated\)

 Ensure there is only one active access key available for any single IAM user \(automated\)

 Ensure IAM policies that allow full "\*:\*" administrative privileges are not attached \(Automated\)

 Ensure that all the expired SSL/TLS certificates stored in AWS IAM are removed \(Automated\)

 Ensure IAM password policy prevents password reuse \(Automated\)

 Ensure that IAM Access analyzer is enabled for all regions \(Automated\)

 Ensure multi-factor authentication \(MFA\) is enabled for all IAM users that have a console password \(Automated\)

 Ensure credentials unused for 45 days or greater are disabled \(Automated\)

 Ensure that S3 Buckets are configured with 'Block public access \(bucket settings\)'

 Ensure no security groups allow ingress from 0.0.0.0/0 to remote server administration ports \(Automated\)

 Ensure no 'root' user account access key exists \(Automated\)

 Ensure MFA is enabled for the 'root' user account \(Automated\)

 Ensure that Object-level logging for read events is enabled for S3 bucket \(Automated\)

</td><td>

Amazon Web Services Foundations Benchmark \(Automated\) v1.4.0 - 05-28-2021

</td></tr><tr><td>

Azure 1.4.0

</td><td>

Ensure that logging for Azure KeyVault is 'Enabled' \(Automated\)

 Ensure Web App is using the latest version of TLS encryption \(Automated\)

 Ensure that Vulnerability Assessment \(VA\) is enabled on a SQL server by setting a Storage Account \(Automated\)

 Ensure Storage logging is Enabled for Blob Service for 'Read', 'Write', and 'Delete' requests \(Automated\)

 Ensure Diagnostic Setting captures appropriate categories \(Automated\)

 Ensure that VA setting 'Send scan reports to' is configured for a SQL server \(Automated\)

 Ensure That 'Notify about alerts with the following severity' is Set to 'High' \(Automated\)

 Ensure 'Additional email addresses' is Configured with a Security Contact Email \(Automated\)

 Ensure Web App Redirects All HTTP traffic to HTTPS in Azure App Service \(Automated\)

 Ensure That 'All users with the following roles' is set to 'Owner' \(Automated\)

 Ensure Storage Logging is Enabled for Table Service for 'Read', 'Write', and 'Delete' Requests \(Automated\)

 Ensure Storage Logging is Enabled for Queue Service for 'Read', 'Write', and 'Delete' requests \(Automated\)

 Ensure that 'Unattached disks' are encrypted with CMK \(Automated\)

 Ensure that VA setting 'Periodic recurring scans' to 'on' for each SQL server \(Automated\)

 Ensure SQL server's TDE protector is encrypted with Customermanaged key \(Automated\)

 Ensure the key vault is recoverable \(Automated\)

</td><td>

Microsoft Azure Foundations Benchmark v1.4.0 - 11-26-2021

</td></tr></tbody>
</table>**Parent Topic:**[Cloud Configuration Governance reference](ccg-reference.md)

