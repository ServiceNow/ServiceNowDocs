---
title: Set up the Microsoft Azure Cosmos DB spoke
description: Integrate the ServiceNow instance and the Microsoft Azure Cosmos DB by installing and configuring the Microsoft Azure Resource Management Spoke connection alias and configuring the Microsoft Azure Cosmos DB SAS connection alias.Create a connection alias record for the Microsoft Azure Cosmos DB SAS to execute the actions under the Core SQL Database Management category of the Microsoft Azure Cosmos DB spoke. Specify whether record is for a host, instance, server, custom application, or account:
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Microsoft Azure Cosmos DB Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Microsoft Azure Cosmos DB spoke

Integrate the ServiceNow instance and the Microsoft Azure Cosmos DB by installing and configuring the Microsoft Azure Resource Management Spoke connection alias and configuring the Microsoft Azure Cosmos DB SAS connection alias.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Microsoft Azure Cosmos DB spoke.
-   Role required: admin

## Create a connection alias record for Microsoft Azure Cosmos DB SAS

Create a connection alias record for the Microsoft Azure Cosmos DB SAS to execute the actions under the Core SQL Database Management category of the Microsoft Azure Cosmos DB spoke.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select **Connections**.

3.  In the Search all connections field, enter `Microsoft Azure Cosmos DB SAS`.

    The **Outbound** tab is active by default. If the tab isn’t active, toggle it to activate.

4.  On the Microsoft Azure Cosmos DB SAS tile, select **View Details**.

5.  Select **Configure**.

6.  Fill the form.

    |Field|Description|
    |-----|-----------|
    |Connection name|Name of the connection record.|
    |Credential name|Name of the credential that is used to access the Cosmos DB SAS.|
    |Shared Access Key Name|Name of the shared access key to the Cosmos DB SAS.|
    |Shared Access Key|Shared access key to the Cosmos DB SAS. Generate the key from the Microsoft Azure portal.|

7.  Select **Create Connection**.


