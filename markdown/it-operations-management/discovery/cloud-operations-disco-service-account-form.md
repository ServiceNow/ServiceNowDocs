---
title: Cloud Discovery service account form reference
description: The Cloud Discovery service account form displays detailed information about the selected cloud provider. The Cloud Discovery service account form is available in the Cloud Discovery Workspace.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Cloud Discovery reference, Discovery reference, Discovery, ITOM Visibility, IT Operations Management]
---

# Cloud Discovery service account form reference

The Cloud Discovery service account form displays detailed information about the selected cloud provider. The Cloud Discovery service account form is available in the Cloud Discovery Workspace.

<table id="table_nw1_xt5_fwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service Account

</td><td>

Name of the service account whose resources you want to discover. This field appears only when the Existing service account option is selected.

</td></tr><tr><td>

Name

</td><td>

Name of the service account whose resources you want to discover.

</td></tr><tr><td>

Account ID

</td><td>

12-digit Identity and Access Management \(IAM\) account number.

</td></tr><tr><td>

Credentials

</td><td>

Name of the credentials that you have created for AWS discovery. Leave the field empty if the account is a member account of an AWS organization and you've configured the associated management account with a credential.

 To add a credential in the ServiceNow AI Platform, select the Add new credentials icon \(![Add new credentials icon.](../../../reuse/itom/image/workspace-icon-add.png)\) and fill in the fields. If required, you can select an existing credential and then edit it by selecting the Edit credentials icon \(![Edit credentials icon.](../../../reuse/itom/image/workspace-icon-edit.png)\).

</td></tr><tr><td>

URL

</td><td>

URL of the datacenter.Enter this field only for the AWS GovCloud \(US\) and AWS China region accounts.

</td></tr><tr><td>

Access role name

</td><td>

Name of the IAM role created for the trusting account.

</td></tr><tr><td>

Select account for access

</td><td>

Name of the trusted account. Configure this field only for accounts that don't use permanent AWS credentials, and rely on IAM roles for access.

</td></tr></tbody>
</table><table id="table_ocw_g55_fwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service Account

</td><td>

Name of the service account whose resources you want to discover. This field appears only when the Existing service account option is selected.

</td></tr><tr><td>

Name

</td><td>

Microsoft Azure subscription name.

</td></tr><tr><td>

Subscription ID/Management group ID

</td><td>

Microsoft Azure subscription ID.

</td></tr><tr><td>

Credentials

</td><td>

Name of the credentials that you have created for Microsoft Azure discovery. To add a credential in the ServiceNow AI Platform, select the Add new credentials icon \(![Add new credentials icon.](../../../reuse/itom/image/workspace-icon-add.png)\) and fill in the fields. If required, you can select an existing credential and then edit it by selecting the Edit credentials icon \(![Edit credentials icon.](../../../reuse/itom/image/workspace-icon-edit.png)\).

</td></tr><tr><td>

URL

</td><td>

URL of the datacenter.

 Configuring this field is required for Azure GovCloud \(US\) accounts. Add the required URL.

</td></tr><tr><td>

Pull Events

</td><td>

Option to enable the ServiceNow AI Platform to collect resource change information from the Microsoft Azure cloud. The ServiceNow AI Platform uses the resource change information to update the Configuration Management Database \(CMDB\). For more information on the supported Azure resource types, see [Azure change processing](../../it-operations-management/concept/azure-change-processing.md). If you select the Pull Events check-box for a management group, the ServiceNow AI Platform enables Azure change processing for all the subscriptions in the management group.

</td></tr></tbody>
</table><table id="table_sfg_t55_fwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service Account

</td><td>

Project ID of the Google Cloud Platform \(GCP\) project whose resources you want to discover.This field appears only when the Existing service account option is selected.

</td></tr><tr><td>

Name

</td><td>

Project ID of the Google Cloud Platform \(GCP\) project.

</td></tr><tr><td>

Project ID/Folder ID

</td><td>

Project ID of the Google project.

</td></tr><tr><td>

Credentials

</td><td>

Name of the credentials that you have created for GCP discovery. To add a credential in the ServiceNow AI Platform, select the Add new credentials icon \(![Add new credentials icon.](../../../reuse/itom/image/workspace-icon-add.png)\) and fill in the fields. If required, you can select an existing credential and then edit it by selecting the Edit credentials icon \(![Edit credentials icon.](../../../reuse/itom/image/workspace-icon-edit.png)\).

</td></tr><tr><td>

Pull Events

</td><td>

Option to enable the ServiceNow® event-driven discovery to collect events for the resource types hosted in the Google Project LDCs.

</td></tr></tbody>
</table><table id="table_yqg_x55_fwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service Account

</td><td>

Name of the service account whose resources you want to discover. This field appears only when the Existing service account option is selected.

</td></tr><tr><td>

Name

</td><td>

Name of the service account.

</td></tr><tr><td>

Credentials

</td><td>

Name of the credentials that you have created for IBM discovery. To add a credential in the ServiceNow AI Platform, select the Add new credentials icon \(![Add new credentials icon.](../../../reuse/itom/image/workspace-icon-add.png)\) and fill in the fields. If required, you can select an existing credential and then edit it by selecting the Edit credentials icon \(![Edit credentials icon.](../../../reuse/itom/image/workspace-icon-edit.png)\).

</td></tr><tr><td>

Account ID

</td><td>

IBM software user number that the instance should use to access the IBM Cloud Console.

</td></tr></tbody>
</table><table id="table_l4f_z55_fwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service Account

</td><td>

Name of the service account whose resources you want to discover. This field appears only when the Existing service account option is selected.

</td></tr><tr><td>

Name

</td><td>

Name of the service account.

</td></tr><tr><td>

Account ID

</td><td>

OCI Compartment id.

</td></tr><tr><td>

Credentials

</td><td>

Name of the credentials that you have created for Oracle Cloud Infrastructure \(OCI\) discovery. To add a credential in the ServiceNow AI Platform, select the Add new credentials icon \(![Add new credentials icon.](../../../reuse/itom/image/workspace-icon-add.png)\) and fill in the fields. If required, you can select an existing credential and then edit it by selecting the Edit credentials icon \(![Edit credentials icon.](../../../reuse/itom/image/workspace-icon-edit.png)\).

</td></tr><tr><td>

Datacenter URL

</td><td>

Datacenter value.For example, `https://$service.ap-mumbai-1.oraclecloud.com`

</td></tr></tbody>
</table><table id="table_mzj_bv5_fwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service Account

</td><td>

Name of the service account whose resources you want to discover. This field appears only when the Existing service account option is selected.

</td></tr><tr><td>

Name

</td><td>

Name of the service account.

</td></tr><tr><td>

OpenStack account ID

</td><td>

Project ID of the OpenStack Project to be discovered.

</td></tr><tr><td>

Account credentials

</td><td>

Name of the credentials that you have created for OpenStack discovery. To add a credential in the ServiceNow AI Platform, select the Add new credentials icon \(![Add new credentials icon.](../../../reuse/itom/image/workspace-icon-add.png)\) and fill in the fields. If required, you can select an existing credential and then edit it by selecting the Edit credentials icon \(![Edit credentials icon.](../../../reuse/itom/image/workspace-icon-edit.png)\).

</td></tr><tr><td>

Cloud URL

</td><td>

OpenStack identity service endpoint.For example: https://&lt;openstack dns&gt;:&lt;port&gt;.

</td></tr></tbody>
</table><table id="table_kd2_dv5_fwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service account

</td><td>

Name of the service account whose resources you want to discover. This field appears only when the Existing service account option is selected.

</td></tr><tr><td>

Name

</td><td>

Name of the service account.

</td></tr><tr><td>

Manager URL

</td><td>

The account ID to which this credential belongs. Specify the API url of the RHV-M instance, including the port. For example, https://my-manager-instance.com:443.

</td></tr><tr><td>

Manager credentials

</td><td>

Name of the credentials that you have created for RHV discovery. To add a credential in the ServiceNow AI Platform, select the Add new credentials icon \(![Add new credentials icon.](../../../reuse/itom/image/workspace-icon-add.png)\) and fill in the fields. If required, you can select an existing credential and then edit it by selecting the Edit credentials icon \(![Edit credentials icon.](../../../reuse/itom/image/workspace-icon-edit.png)\).

</td></tr></tbody>
</table><table id="table_kw1_fv5_fwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service Account

</td><td>

Name of the service account whose resources you want to discover. This field appears only when the Existing service account option is selected.

</td></tr><tr><td>

Name

</td><td>

Name of the service account.

</td></tr><tr><td>

UUID

</td><td>

Universal Unique Identifier \(UUID\) of the instance.To access the UUID, do the following:

1.  Open the Managed Object Browser \(MOB\) for the vCenter.
2.  Select **Content** &gt; **About**.
3.  Paste the value of the instance UUID property in this field.

</td></tr><tr><td>

Credentials

</td><td>

Name of the credentials that you have created for VMware discovery. To add a credential in the ServiceNow AI Platform, select the Add new credentials icon \(![Add new credentials icon.](../../../reuse/itom/image/workspace-icon-add.png)\) and fill in the fields. If required, you can select an existing credential and then edit it by selecting the Edit credentials icon \(![Edit credentials icon.](../../../reuse/itom/image/workspace-icon-edit.png)\).

</td></tr><tr><td>

URL

</td><td>

Full URL of the vCenter.

</td></tr></tbody>
</table>**Parent Topic:**[Cloud Discovery reference](cloud-discovery-reference.md)

