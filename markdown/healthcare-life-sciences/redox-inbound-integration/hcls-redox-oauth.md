---
title: Link your ServiceNow instance with your Redox account
description: Create an OAuth application endpoint for the external Redox healthcare system to access your ServiceNow instance.
locale: en-US
release: xanadu
product: Redox Inbound Integration
classification: redox-inbound-integration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Redox Inbound Integration, Redox Inbound Integration, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Link your ServiceNow instance with your Redox account

Create an OAuth application endpoint for the external Redox healthcare system to access your ServiceNow instance.

## Before you begin

Ensure that the application scope is set to Redox Inbound Integration by using the application picker. For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

Role required: sn\_hcls.admin or admin

## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  In the Application Registries list, click **New**.

3.  On the OAuth application page, select **Create an OAuth API endpoint for external clients**.

4.  On the Application Registries form, fill in the Redox healthcare system details including the name, client ID, accessible from, client secret, accessible from, refresh token lifespan, and access token lifespan.

    **Note:** You can ignore the **Redirect URL** and **Logo URL** fields, which are not used for this configuration.

    For more information, see [Create an endpoint for clients to access the instance](https://www.servicenow.com/docs/access?context=t_CreateEndpointforExternalClients&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

5.  Click **Submit**.


