---
title: Verify the Microsoft Endpoint Configuration Manager spoke records
description: Verify that the spoke is integrated with CSD 2.0 after setting up and configuring the Microsoft Endpoint Configuration Manager spoke and create server instance record to use Microsoft Endpoint Configuration Manager spoke with CSD 2.0.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CSD 2.0 for Microsoft Endpoint Configuration Manager, Client Software Distribution 2.0 application, Integration Hub solutions, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Verify the Microsoft Endpoint Configuration Manager spoke records

Verify that the spoke is integrated with CSD 2.0 after setting up and configuring the Microsoft Endpoint Configuration Manager spoke and create server instance record to use Microsoft Endpoint Configuration Manager spoke with CSD 2.0.

## Before you begin

-   Activate the Microsoft Endpoint Configuration Manager spoke and set up the spoke. For more information about the spoke setup, see [Set up the Microsoft Endpoint Configuration Manager spoke](../concept/csd2-conf-sccm.md#).
-   Activate the CSD 2.0 application.
-   Role required: admin

## Procedure

1.  Verify that these modules are available.

    -   Applications
    -   Configurations
    -   Server Instances
    -   Deployments
    -   Collections
2.  Navigate to **System Definition** &gt; **Tables** and verify that these table are available.

    -   Deployment \[sn\_ms\_epcfgmgr\_spk\_deployment\]
    -   Configuration \[sn\_ms\_epcfgmgr\_spk\_sf\_config\]
    -   Collection \[sn\_ms\_epcfgmgr\_spk\_collection\]
    -   Server Instance \[sn\_ms\_epcfgmgr\_spk\_server\]
    -   Application \[sn\_ms\_epcfgmgr\_spk\_application\]
3.  Verify that the flows are configured correctly in the provider record.

    1.  Navigate to **Client Software Distribution 2.0** &gt; **Providers**.

    2.  Open the record **Microsoft Endpoint Configuration Manager**.

    3.  Verify that the flows are configured correctly in the record.

        ![Verify that the flows are configured.](../image/csd2-prvdr-rec.png)

        **Note:** You can configure the default flows as per your requirement.


**Parent Topic:**[CSD 2.0 for Microsoft Endpoint Configuration Manager](../concept/csd2.md)

