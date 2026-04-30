---
title: Create a connection record for Microsoft Dynamics 365
description: Create a connection for your Microsoft Dynamics 365 application. The Microsoft Dynamics 365 spoke connection and credential aliases use these connections to perform actions in Microsoft Dynamics 365.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Microsoft Dynamics 365 Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Create a connection record for Microsoft Dynamics 365

Create a connection for your Microsoft Dynamics 365 application. The Microsoft Dynamics 365 spoke connection and credential aliases use these connections to perform actions in Microsoft Dynamics 365.

## Before you begin

Role required: Global administrator and Dynamics 365 administrator in Microsoft admin center

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

2.  Select the alias record for **Microsoft 365 Dynamics**.

3.  On the Connection &amp; Credential Aliases page, select **Create New connection and credential**.

4.  In the Create Connection and Credential window, perform the following:

    1.  In the **Connection URL** field, enter the connection URL.

        To fetch the connection URL, log in to the Microsoft Admin portal and navigate to **Admin Centers** &gt; **All admin centers** &gt; **Select Dynamics 365 apps** &gt; **Environments**. Select the environment that you want to integrate with. The environment URL is the connection URL.

    2.  Under the **Please Enter the Credential Information** section, select the permission type to ensure your application accesses data correctly and securely.

        The permission type can be **Application Permissions** or **Delegated Permissions** depending on the application's data access requirements.

    3.  In the **OAuth Client ID** field, enter the OAuth Client ID that you received from [Set up Microsoft Azure Active Directory](setup-ms-azure-ad.md).

    4.  In the **OAuth Client Secret** field, enter the OAuth Client Secret key that you received from [Set up Microsoft Azure Active Directory](setup-ms-azure-ad.md).

5.  Select **Create and Get OAuth Token**.


