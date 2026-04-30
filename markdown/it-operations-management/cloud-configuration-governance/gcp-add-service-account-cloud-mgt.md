---
title: \(Optional\) Add a Google Cloud Platform service account to the cloud account
description: During Cloud Provisioning and Governance Day 1 setup, you added one service account to the cloud account. To compartmentalize your infrastructure or to include different datacenters, you can add another service account. A particular datacenter, however, cannot be selected in more than one service account in a cloud account.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Day 1 setup guide for Cloud Provisioning and Governance: Google Cloud Connector, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# \(Optional\) Add a Google Cloud Platform service account to the cloud account

During Cloud Provisioning and Governance Day 1 setup, you added one service account to the cloud account. To compartmentalize your infrastructure or to include different datacenters, you can add another service account. A particular datacenter, however, cannot be selected in more than one service account in a cloud account.

## Before you begin

Role required: sn\_cmp.cloud\_admin

## About this task

A service account is a secure record on your instance that stores the credential and access information for your provider account. Discovery uses the information to access your provider account to get data on each resource in each specified datacenter.

In this example, you added the service account named **ProviderB-ServiceAccount-1** and selected three datacenters to include in the cloud account:

![A second service account with three selected datacenters](../image/cloud-acct-makeup.png "A service account with three selected datacenters")

**Important:** In a cloud account, you cannot select a particular datacenter in two different service accounts.

## Procedure

1.  Navigate to **Cloud Admin Portal** &gt; **Service Accounts**.

2.  Click **New**, enter a unique and meaningful **Name**, and then fill in the form.

3.  Fill in the remaining fields:

<table id="table_c1m_cxy_jkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Account ID

</td><td>

From the JSON key file that is associated with the service account, copy/paste the **project\_id** value into the **Account ID** field.![Copy the project_id value into the Account ID field](../image/gcp-add-service-acct.png "Google Cloud Platform (GCP) project ID")

</td></tr><tr><td>

Discovery credentials

</td><td>

Select the appropriate credentials for the service account For information on generating or obtaining the credentials, see [Specify the credentials that Cloud Provisioning and Governance: Google Cloud Connector uses to access Google Cloud Platform data](gcp-create-creds-cloud-mgt-1.md).

</td></tr><tr><td>

Datacenter URL

</td><td>

Leave the **Datacenter URL** field blank.

</td></tr><tr><td>

Datacenter type

</td><td>

Select **Google Cloud Platform Datacenter**.

</td></tr><tr><td>

Datacenter discovery status

</td><td>

Auto-generated value: Status and timestamp of the last execution of Discovery on the datacenter.

</td></tr></tbody>
</table>4.  Click **Update** or **Submit**.

    The system creates the service account and displays the list of all discovered datacenters.

5.  Repeat the process to add as many service accounts as needed.


