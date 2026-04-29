---
title: Set up Azure connection
description: Add and configure an Azure connection with your Azure portal. Using the connection credentials, the Cloud Account Management application creates Azure subscriptions. This is a one-time configuration step.
locale: en-US
release: australia
product: Cloud Account Management
classification: cloud-account-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Cloud Account Management, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Set up Azure connection

Add and configure an Azure connection with your Azure portal. Using the connection credentials, the Cloud Account Management application creates Azure subscriptions. This is a one-time configuration step.

## Before you begin

The below procedure is only required if you're creating Azure subscriptions.

Role required: sn\_itom\_cam.cw\_admin

## Procedure

1.  Navigate to **All** &gt; **Flow Designer**.

2.  Select **Integrations** &gt; **Connections** &gt; **Outbound**.

3.  Search and select **Azure Connection \(sn\_itom\_cam\)**.

4.  Select **View Details**.

5.  Select **Configure**.

6.  In the **Configure Connection** dialog box, provide the following information.

    |Field|Description|
    |-----|-----------|
    |Connection name|Unique name for the Azure OAuth connection.|
    |Connection URL|The default URL is automatically populated. If necessary, you can modify the URL.|
    |OAuth Client ID|The client ID of the application registered in the Azure OAuth server.|
    |OAuth Client Secret|The client secret of the application registered in the Azure OAuth server.|
    |OAuth Token URL|The URL that specifies the endpoint to get the access token from the OAuth server. The default URL is automatically populated. If necessary, you can modify the URL.|

7.  Select **Configure and Get OAuth Token**.

8.  To view the connection alias, select **View connection alias**.


