---
title: Run Discovery on GitHub Actions config provider
description: Discover all repositories and workflows in your organization by adding a GitHub Actions config provider and running Discovery on it using the Cloud Services Catalog application.
locale: en-US
release: zurich
product: Cloud Services Catalog
classification: cloud-services-catalog
topic_type: task
last_updated: "2025-11-24"
reading_time_minutes: 1
breadcrumb: [Integrating GitHub Actions with Cloud-Services-Catalog, Configure, Cloud Services Catalog, ITOM Cloud Accelerate, IT Operations Management]
---

# Run Discovery on GitHub Actions config provider

Discover all repositories and workflows in your organization by adding a GitHub Actions config provider and running Discovery on it using the Cloud Services Catalog application.

## Before you begin

Role required: sn\_cmp.cloud\_admin

## Procedure

1.  In the Cloud Admin Portal, navigate to **Manage** &gt; **Credentials**.

2.  Select **New**.

3.  Select **API Key Credentials**.

4.  On the form, fill in the fields.

<table id="table_dvm_wp3_khc"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A unique and descriptive name for this credential.

</td></tr><tr><td>

Active

</td><td>

Option to enable these credentials for use.

</td></tr><tr><td>

API Key

</td><td>

The API key you copied while creating personal access token in GitHub.

</td></tr><tr><td>

Credential alias

</td><td>

Option to allow flow and workflow creators to assign individual credentials to any activity in a flow or workflow or assign different credentials to each occurrence of the same activity type in a flow or workflow.

</td></tr><tr><td>

Applies to

</td><td>

Determines whether to apply these credentials to  all MID Servers  in your network, or to one or more specified MID Servers.

</td></tr><tr><td>

MID servers

</td><td>

This field appears only when **Some MID servers** is selected from the **Applies to** field. It provides fields through which you can select the target MID Servers.

</td></tr><tr><td>

Order

</td><td>

Order in which  Discovery  tries this credential when it attempts to log on to devices. The smaller the number, the higher in the list this credential appears. Providing a credential order is helpful when using large numbers of credentials or when security locks out users after three failed login attempts.

 If all the credentials have the same order number \(or none\), the instance tries the credentials in a random order.

</td></tr></tbody>
</table>    **Important:** Infrastructure as Code \(IaC\) Discovery is supported. You can discover GitHub Actions workflows, inventory, and related resource groups.

5.  Select **Submit**.

6.  Add a config provider.

7.  Navigate to **Manage** &gt; **Config Management**.

8.  Initiate discovery of config installables and create an order in the sn\_cmp\_order table to start the discovery process by selecting **Discover Now**.

    The name of the config installable displays when creating a new template version.


## Result

Discovered config installables are saved in the sn\_cmp\_cfg\_installable table using the format ProviderName.WorkflowName.

**Parent Topic:**[Integrating GitHub Actions with Cloud-Services-Catalog](../concept/integrating-github-actions-with-cloud-service-catalog.md)

