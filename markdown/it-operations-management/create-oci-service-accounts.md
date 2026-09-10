---
title: Create OCI service accounts
description: Create Oracle Cloud Infrastructure \(OCI\) service accounts on the ServiceNow AI Platform to access your Oracle account during Oracle discovery.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/create-oci-service-accounts.html
release: zurich
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Oracle OCI, Oracle service account]
breadcrumb: [Set up Oracle Cloud infrastructure \(OCI\) service accounts, Set up a cloud service account, Access to cloud environments for ITOM products, IT Operations Management]
---

# Create OCI service accounts

Create Oracle Cloud Infrastructure \(OCI\) service accounts on the ServiceNow AI Platform to access your Oracle account during Oracle discovery.

## Before you begin

Verify that Oracle API credentials have been created. For more information, see [Create Oracle API credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/create-oracle-api-credentials.md).

Retrieve the Compartment ID from **Identity &amp; Security** &gt; **Compartments** in the Oracle Cloud Console.

For GovCloud accounts, confirm that Discovery and Service Mapping Patterns is using at least version 1.29.0.

For UK Sovereign Cloud accounts, confirm that Discovery and Service Mapping Patterns is using at least version 1.35.0.

Role required: discovery\_admin

## Procedure

1.  In the navigation filter, enter `cmdb_ci_cloud_service_account.list`.

2.  Select **New**.

3.  In the **Discovery Credentials** field, begin to enter the credential name and select it from the list.

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

The compartment ID, which is the Oracle Cloud Identifier \(OCID\) of the compartment associated with this service account.

</td></tr><tr><td>

Datacenter URL

</td><td>

The URL of the datacenter.Example URLs:

-   For commercial cloud: `https://{service}.ap-mumbai-1.oraclecloud.com`
-   For GovCloud: `https://{service}.us-gov-ashburn-1.oraclegovcloud.com`
-   For UK Sovereign Cloud: `https://{service}.uk-gov-london-1.oci.oraclegovcloud.uk`


</td></tr><tr><td>

Datacenter Type

</td><td>

The type of datacenter where the account is hosted, which should be `OCI Datacenter [cmdb_ci_oci_datacenter]`.

</td></tr></tbody>
</table>5.  Select **Submit**.


## What to do next

Schedule an OCI cloud discovery. For more information, see [Create an OCI Discovery schedule in Discovery Admin Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/create-oci-schedule-DAW.md).

**Parent Topic:**[Set up Oracle Cloud infrastructure \(OCI\) service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/set-up-oracle-cloud-infrastructure-oci-service-accounts.md)

