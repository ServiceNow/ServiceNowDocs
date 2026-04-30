---
title: Create a scan account configuration
description: Configure the Cloud Account Management app before scanning a service account to confirm it’s ready for effective account management.
locale: en-US
release: yokohama
product: Cloud Account Management
classification: cloud-account-management
topic_type: task
last_updated: "2024-10-15"
reading_time_minutes: 1
breadcrumb: [Creating configurations, Configuring Cloud Account Management, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Create a scan account configuration

Configure the Cloud Account Management app before scanning a service account to confirm it’s ready for effective account management.

## Before you begin

Role required: sn\_itom\_cam.cw\_admin

## Procedure

1.  Navigate to **All** &gt; **Cloud Workspace** &gt; **Configuration**.

2.  Select **New**.

3.  In the **New Configuration** form, provide the following information.

<table id="table_rjf_fpl_zdc"><thead><tr><th>

Field Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cloud provider

</td><td>

Name of the cloud provider platform such as AWS, Azure, or GCP.

</td></tr><tr><td>

Name

</td><td>

Name for the configuration.

</td></tr><tr><td>

Service accounts

</td><td>

The service account and its member accounts.**Note:** Selecting a management account automatically scans all current and future member accounts. However, if you select individual member accounts, each must be chosen manually for scanning.

</td></tr><tr><td>

CCG scan configuration

</td><td>

Cloud Configuration Governance \(CCG\) scan configuration used for getting the violations for all accounts in the selected cloud organization.

</td></tr><tr><td>

Description

</td><td>

Information that can be recorded in work notes.

</td></tr></tbody>
</table>4.  Select **Submit**.


## What to do next

[Review default Cloud Account Management certification policy](policy-setup.md)

