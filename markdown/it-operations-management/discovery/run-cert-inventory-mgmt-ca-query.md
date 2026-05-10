---
title: Run Certificate discovery via Certificate Authority query
description: Running Certificate discovery via Certificate Authority query allows for systematic identification and import of TLS certificates from specific Certificate Authorities, ensuring comprehensive tracking, management, and security of the certificate inventory. Discover TLS certificates from Certificate Authorities \(CA\) with Certificate Inventory and Management, using Patterns for diverse certificate authority vendors.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Visibility to TLS certificates, Configuring Certificate Inventory and Management, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Run Certificate discovery via Certificate Authority query

Running Certificate discovery via Certificate Authority query allows for systematic identification and import of TLS certificates from specific Certificate Authorities, ensuring comprehensive tracking, management, and security of the certificate inventory. Discover TLS certificates from Certificate Authorities \(CA\) with Certificate Inventory and Management, using Patterns for diverse certificate authority vendors.

## Before you begin

Role required: pki\_admin or discovery\_admin

## About this task

In Certificate discovery, the Certificate Authorities \(CA\) pattern uses specific API elements. The user added to the instance credentials needs permissions for these queries. For more information on the Certificate Authorities \(CA\) pattern and the associated API elements, see [Certificate authorities pattern API elements and permissions](../reference/ca-api-permission.md).

## Procedure

1.  Generate a credential alias if needed.

    For more information, see [Credential aliases for Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/discovery-credential-alias.md). Create a new credential alias for new credentials. In case multiple credentials share the same alias, Discovery prioritizes the Credential and initiates the process.

2.  Create a new credential type specific to the Certificate Authority \(CA\).

    1.  Navigate to **Discovery** &gt; **Credentials** then select **New**.

    2.  Select **Certificate Management Credentials**.

    3.  To unlock the **Credential alias list**, select the lock icon.

        The alias is mapped to the credential.

    4.  Select **Specify Type**: **Credential**.

    5.  Select **CA Type**.

        The available CA types are: GoDaddy, Digicert, Entrust, or Sectigo.

    6.  Fill in the fields that are specific to the CA type you selected.

        Each Certificate Authority \(CA\) requires specific form field entries. For more information, see [API Key credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/API-key-credential-form.md).

3.  Create a Discovery schedule with the following fields.

    For more information on setting up your Discovery schedules, see [Schedule a horizontal discovery](t_CreateADiscoverySchedule.md#).

    1.  Select **Discovery**: **Certificates**.

    2.  Select **Certificate Discovery Type**: **CA Trust Discovery**.

    3.  Select **MID Server selection method**: **Auto Select** or **Specific MID Server**.

    4.  Fill out any other necessary fields.

    5.  Select **Save**.

4.  To add CA pattern you need, from the **Serverless Execution pattern** tab, select **New**.

    If you enable the **Include cert status** option, you can specify multiple certificate statuses by separating them with commas.

5.  Select **Submit**.


## Result

When your Discovery schedule runs, it automatically scans your files.

