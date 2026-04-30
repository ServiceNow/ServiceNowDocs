---
title: Create API key credentials for the Terraform account and the supported VCS account
description: Create API key credential for Terraform account and supported Version Control System \(VCS\) accounts that contain the Terraform template repositories.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a Terraform Enterprise or Terraform Cloud config provider, Configuring Cloud Services Catalog Terraform Connector, Cloud Services Catalog Terraform Connector, Support for continuous delivery \(configuration management\), Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Create API key credentials for the Terraform account and the supported VCS account

Create API key credential for Terraform account and supported Version Control System \(VCS\) accounts that contain the Terraform template repositories.

## Before you begin

Role required: admin

## About this task

An API key credential is a secured record in the ServiceNow AI Platform that stores an API key such as Terraform Enterprise, Terraform Cloud, or VCS account API key. Cloud Services Catalog Terraform Connector uses the API key credential to connect with the account and discover its resources.

## Procedure

1.  Navigate to **All** &gt; **Cloud Provisioning and Governance** &gt; **Cloud Admin Portal**.

    The Cloud Admin Portal opens in a new browser tab.

2.  On the Cloud Admin Portal, navigate to **Manage** &gt; **Credentials**.

3.  Select **New**.

4.  Select **API Key Credentials**.

5.  On the form, fill in the fields.

    For description of the form fields, see [Cloud Services Catalog Terraform Connector API Key Credentials form reference](../reference/cpg-terraform-connector-api-key-credentials-form-reference.md).

6.  Select **Submit**.


