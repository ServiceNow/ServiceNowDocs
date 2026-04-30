---
title: Set up Azure Service Principal credential
description: Provide the Azure credentials obtained from your Azure administrator. These credentials are used to create a suspension profile and enables you to suspend temporarily or terminate Azure accounts as needed.
locale: en-US
release: yokohama
product: Cloud Account Management
classification: cloud-account-management
topic_type: task
last_updated: "2025-03-05"
reading_time_minutes: 1
breadcrumb: [Setting up Azure cloud, Configuring cloud providers, Configuring Cloud Account Management, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Set up Azure Service Principal credential

Provide the Azure credentials obtained from your Azure administrator. These credentials are used to create a suspension profile and enables you to suspend temporarily or terminate Azure accounts as needed.

## Before you begin

Review the [Permissions required for Azure Service Principal](../reference/permissions-required-for-azure-service-principal.md) topic before creating a Azure Service Principal credential.

Role required: ServiceNow AI Platform admin

## Procedure

1.  Log in to the ServiceNow instance.

2.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

3.  From the list, select **Azure Service Principal**.

4.  In the **Connections &amp; Credentials** form, provide the following information.

    |Field|Value|
    |-----|-----|
    |Name|Name of the service principal to register with the instance. For example, `Azure service principal credentials`.|
    |Tenant ID|Azure Directory ID value from the text file.|
    |Client ID|Azure Application ID value from the text file.|
    |Secret key|Azure Application key value from the text file.|
    |Credential Alias|The credential alias that you want to tie to the OAuth 2.0 credential. By default, use the predefined alias name as: sn\_itom\_cam.CAM\_Azure\_Connection|

5.  In the **API Key** field, enter the key obtained from the admin.

6.  To complete the process, select **Submit**.


