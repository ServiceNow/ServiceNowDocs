---
title: Verify the Microsoft Intune spoke records
description: Verify that the spoke is integrated with CSD 2.0 after setting up and configuring the Microsoft Intune spoke and create server instance record to use Microsoft Intune spoke with CSD 2.0.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [CSD 2.0 for Microsoft Intune, Client Software Distribution 2.0 application, Integration Hub available solutions, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Verify the Microsoft Intune spoke records

Verify that the spoke is integrated with CSD 2.0 after setting up and configuring the Microsoft Intune spoke and create server instance record to use Microsoft Intune spoke with CSD 2.0.

## Before you begin

-   Activate the Microsoft Azure Active Directory spoke spoke and set up the spoke. For more information about the spoke setup, see [Set up Microsoft Entra ID spoke](set-up-azure.md#).
-   Activate the Microsoft Intune spoke and set up the spoke. For more information about the spoke setup, see [Set up the Microsoft Intune spoke](setup-ms-intune.md#).
-   Activate the CSD 2.0 application.
-   Role required: admin

## Procedure

1.  Verify that these modules are available.

    -   Applications
    -   Configurations
    -   Server Instances
    -   Deployments
    -   Groups
2.  Navigate to **System Definition** &gt; **Tables** and verify that these table are available.

    -   Configuration \[sn\_ms\_intune\_spoke\_sf\_config\]
    -   Deployment \[sn\_ms\_intune\_spoke\_deployment\]
    -   Server Instance \[sn\_ms\_intune\_spoke\_server\]
    -   Application \[sn\_ms\_intune\_spoke\_application\]
    -   Group \[sn\_ms\_intune\_spoke\_group\]
3.  Verify that the flows are configured correctly in the provider record.

    1.  Navigate to **Client Software Distribution 2.0** &gt; **Providers**.

    2.  Open the record **Microsoft Intune**.

    3.  Verify that the flows are configured correctly in the record.

        ![Verify that the flows are configured correctly.](../image/csd2-intune-flows.png)

        **Note:** You can configure the default flows as per your requirement.


**Parent Topic:**[CSD 2.0 for Microsoft Intune](../concept/csd2-ms-intune.md)

