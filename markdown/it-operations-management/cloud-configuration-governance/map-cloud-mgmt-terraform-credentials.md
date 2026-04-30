---
title: Map credentials between Cloud Provisioning and Governance and Terraform
description: Map credential types and service account fields Check for accuracy after IaC provider settings is updated to Credential mappings between Cloud Provisioning and Governance and Terraform using Credential Mapping.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Using Cloud Services Catalog Terraform Connector, Cloud Services Catalog Terraform Connector, Support for continuous delivery \(configuration management\), Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Map credentials between Cloud Provisioning and Governance and Terraform

Map credential types and service account fields between Cloud Provisioning and Governance and Terraform using Credential Mapping.

## Before you begin

The latest Cloud Services Catalog Terraform Connector must be installed from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/9b04ffc20b1323002530a387b6673a1d/).

Role required: sn\_cmp.cloud\_admin, admin

## About this task

Use the Credential Mapping module to perform credential and service account mappings for datacenter credentials used by the Terraform provider to provision datacenter resources and Cloud Provisioning and Governance for discovery.

## Procedure

1.  Navigate to **All** &gt; **Design** &gt; **Credential Mapping**.

2.  Select **New**.

    ![Terraform Datacenter Mapping form](../../it-operations-management/image/new-credential-mapping-terraform.png "Terraform Datacenter Mapping form")

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Terraform Provider|Name of the Terraform provider.|
    |Datacenter Block|The resource block whose credentials you are mapping from the lookup table.|
    |Credential Type|The appropriate credential type from the lookup table. For example, Azure Service Principal \[azure\_service\_principal\].|
    |Credential Resolver|An appropriate MID Server script include from the lookup table. For example, Search and select the TerraformProviderCredentialResolver script.|

4.  Select **Submit**.

    The Terraform provider credentials record is created and displayed in the Terraform Datacenter Mappings list.

5.  On the record you created, navigate to the **Credentials Mappings** related list, and then select **New**.

    1.  Complete the **Credential Mapping** form.

        |Field|Description|
        |-----|-----------|
        |Provider Authentication Key|Authentication key \(variable\) field name as used by the provider. For example, the Terraform provider block for \(Amazon Web Services\) AWS uses the field `secret_key`.|
        |Discovery Credential Key|The corresponding field in the Discovery credentials from the lookup table. For example, `access_key` field in Terraform corresponds to `Secret key` field in the ServiceNow instance.|
        |Terraform Datacenter Mapping|Datacenter for which you are mapping the credentials.|

    2.  Select **Submit**.

6.  Select the **Service Account Mappings** tab, and then select **New**.

    1.  Complete the **Service Account Mapping** form.

        |Field|Description|
        |-----|-----------|
        |Provider Authentication Key|Authentication key \(variable\) field name as used by the provider. For example, the Terraform provider block for AWS uses the field `secret_key`.|
        |Service Account Field|Service Account \(variable\) field name from the lookup table, whose credentials you are mapping to the Provider Authentication Key.|
        |Terraform Datacenter Mapping|Datacenter for which you are mapping the credentials.|

    2.  Select **Submit**.

    You have mapped the field values that you added under the Credential Mapping and Service Account Mapping related lists to the Terraform provider.


**Parent Topic:**[Using Cloud Services Catalog Terraform Connector](../concept/using-ccg-terraform-connector.md)

