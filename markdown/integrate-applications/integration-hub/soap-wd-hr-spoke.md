---
title: Configurations to use Workday SOAP Basic Auth with WS-Security
description: Configure your ServiceNow instance to perform actions that use the Workday SOAP Basic Auth with WS-Security.Provide the base URL of your Workday HR instance in the Connection Details \[connection\_details\] table. Spoke actions based on the SOAP API, use these details for the action execution.Create a WS-Security Username Profile to provide your Workday credentials to authenticate requests from ServiceNow.Configure the SOAP security profile by adding the security user name profile you had created to authenticate requests from ServiceNow.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Workday HR Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Configurations to use Workday SOAP Basic Auth with WS-Security

Configure your ServiceNow instance to perform actions that use the Workday SOAP Basic Auth with WS-Security.

## Before you begin

Role required: admin.

## About this task

This is the most traditional Workday SOAP authentication setup.

**Note:** These configurations are needed to use the SOAP-based spoke actions. For information about the SOAP-based spoke actions, see the Spoke actions that use Workday SOAP APIs section in [Workday HR Spoke](../concept/workday-hr-spoke.md).

## Provide the Workday HR base URL

Provide the base URL of your Workday HR instance in the Connection Details \[connection\_details\] table. Spoke actions based on the SOAP API, use these details for the action execution.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Workday HR Spoke** &gt; **Connection Details**.

2.  Click the **Show List** related list.

3.  Click **New**.

4.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Base URL|Base URL of the Workday instance or tenant name. Enter the base URL in this format `https://<workday_host_url>/ccx/service/<workday_tenant_name>`|
    |Version|Version of the API. For example, enter `v33.2`.|
    |Webservice Type|Type of web service. Select `SOAP`.|

5.  Click **Save**.


## Create a WS-Security Username Profile for the Workday HR spoke

Create a WS-Security Username Profile to provide your Workday credentials to authenticate requests from ServiceNow.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **SOAP Integrations** &gt; **WS-Security Username Profiles**.

2.  Click **New**.

3.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify this credential. For example, enter `WorkdayHR User`.|
    |Application|Application in which the record is applicable. Select **Workday HR Spoke**.|
    |Username|Workday user who has integration rights using Workday Web Services.|
    |Password|Password of the Workday user.|

4.  Click **Save**.


## Configure the SOAP security policy for the Workday HR spoke

Configure the SOAP security profile by adding the security user name profile you had created to authenticate requests from ServiceNow.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **SOAP Integrations** &gt; **SOAP Security Policies**.

2.  Open the record for the Workday HR spoke, for example, **WorkdayHR**.

    **Note:** If you intend to use another SOAP security policy record and not the default record, you must ensure that you select that record in all the actions that use Workday SOAP web services.

    ![Select the required SOAP security policy if you are not using the default policy.](../image/ws-security-wd-hr-spoke.png)

    Except these listed actions, all other actions use Workday SOAP web services:

3.  For **WS-Security Username Profile**, select the security username profile you had created for the Workday HR spoke.

    See [Create a WS-Security Username Profile for the Workday HR spoke](soap-wd-hr-spoke.md#) for more information.

4.  Do not provide a value in **WS-Security X.509 Profile**.

5.  Right-click the form header and click **Save**.


