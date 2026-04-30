---
title: Create OCI service accounts
description: Create Oracle Cloud Infrastructure \(OCI\) service accounts on the ServiceNow AI Platform to access your Oracle account during Oracle discovery.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-11-09"
reading_time_minutes: 1
keywords: [Oracle OCI, Oracle service account]
breadcrumb: [Set up Oracle Cloud infrastructure \(OCI\) service accounts, Setting up a cloud service account, Access to cloud environments for ITOM products, IT Operations Management]
---

# Create OCI service accounts

Create Oracle Cloud Infrastructure \(OCI\) service accounts on the ServiceNow AI Platform to access your Oracle account during Oracle discovery.

## Before you begin

Verify that Oracle API credentials have been created. For more information, see [Create Oracle API credentials](create-oracle-api-credentials.md).

Retrieve the Compartment ID, which can be found under **Identity &amp; Security** &gt; **Compartments** in the Oracle Cloud Console.

For GovCloud accounts, confirm that Discovery and Service Mapping Patterns is using at least version 1.29.0.

Role required: discovery\_admin

## Procedure

1.  In the navigation filter, enter `cmdb_ci_cloud_service_account.list`.

2.  Select **New**.

3.  In the **Discovery Credentials field**, begin to enter the credential name and select it from the list.

4.  On the form, fill in the remaining fields.

<table id="table_t3q_snf_gfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A unique name for the OCI service account.

</td></tr><tr><td>

Account ID

</td><td>

Compartment ID, which is the Oracle Cloud Identifier \(OCID\) of the compartment associated with this service account.

</td></tr><tr><td>

Datacenter URL

</td><td>

URL of the datacenter.Example URLs:

-   For commercial cloud: `https://{service}.ap-mumbai-1.oraclecloud.com`
-   For GovCloud: `https://{service}.us-gov-ashburn-1.oraclegovcloud.com`


</td></tr><tr><td>

Datacenter Type

</td><td>

Type of the datacenter where the account is hosted, which should be OCI Datacenter \[cmdb\_ci\_oci\_datacenter\].

</td></tr></tbody>
</table>5.  Select **Submit**.


## What to do next

Schedule an OCI cloud discovery. For more information, see [Create a discovery schedule in Cloud Discovery Workspace](../../discovery/task/cloud-operations-disco-create-schedule.md).

**Parent Topic:**[Set up Oracle Cloud infrastructure \(OCI\) service accounts](../concept/set-up-oracle-cloud-infrastructure-oci-service-accounts.md)

