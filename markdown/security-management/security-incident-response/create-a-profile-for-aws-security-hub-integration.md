---
title: Create a profile for AWS Security Hub finding integration
description: Create an AWS Security Hub profile in your ServiceNow AI Platform instance which you are going to use to ingest data from AWS Security Hub and create a corresponding security incident in Security Incident Response Workspace.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-09-29"
reading_time_minutes: 1
breadcrumb: [Amazon Web Services \(AWS\) Security Hub integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create a profile for AWS Security Hub finding integration

Create an AWS Security Hub profile in your ServiceNow AI Platform instance which you are going to use to ingest data from AWS Security Hub and create a corresponding security incident in Security Incident Response Workspace.

## Before you begin

Role required: admin

## About this task

The integration enables you to create security incidents for different types of findings on the AWS Security Hub platform, such as unauthorized access attempts and malware. These incidents are created based on the profiles that you configure in the ServiceNow AI Platform instance. All incidents are initially created for a configured finding type in a profile. You can further filter the findings you have created to specify which findings create security incidents.

All findings that meet the selection criteria in your AWS Security Hub tenant, and are available over the AWS Security Hub API, are initially ingested into your ServiceNow AI Platform instance.

## Procedure

1.  Navigate to **All** &gt; **AWS Security Hub Findings Integration** &gt; **AWS Security Hub Findings Profile**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_kyc_qbg_p4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the profile.

 This name helps you to identify the profile type and is also the default name for the security tag that is associated with this profile.

</td></tr><tr><td>

Active

</td><td>

Select to activate the profile.

 When the profile is active, it implies that the ServiceNow AI Platform actively ingests AWS Security Hub findings data and corresponding security incidents are created in SIR when the filtering conditions are matched.

</td></tr><tr><td>

Source

</td><td>

The AWS Security Hub Integration tenant that you have configured to ingest findings. If you have multiple tenants configured, select the appropriate tenant for the finding types that you are planning to ingest for the profile.

</td></tr><tr><td>

Order

</td><td>

Enter a value for this field which indicates the order that flows are executed when two or more profiles share triggering conditions.

 The flow with the lowest number has the highest priority.

To set the order of operation, enter a value. For example, 100, 200, 300, 400.The default is 100.

</td></tr><tr><td>

Description

</td><td>

Extra text to help you distinguish this profile from other profiles.

</td></tr></tbody>
</table>
