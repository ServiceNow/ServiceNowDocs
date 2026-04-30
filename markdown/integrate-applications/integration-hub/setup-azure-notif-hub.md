---
title: Set up the Microsoft Azure Notification Hub spoke
description: Set up your ServiceNow instance to integrate with the Microsoft Azure Notification Hub. Setting enables the Microsoft Azure Notification Hub to authenticate requests from your ServiceNow instance.Set up the Microsoft Azure Resource Management connection alias to do the actions under the Notification Hub Management and Namespace Management categories of the Microsoft Azure Notification Hub spoke.Establish a connection between the Microsoft Azure Notification Hub SAS connection alias and the Microsoft Azure portal.Generate a shared access key that you must provide to create a connection between the Microsoft Azure Notification Hub SAS connection alias and the Microsoft Azure portal.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Microsoft Azure Notification Hub Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Set up the Microsoft Azure Notification Hub spoke

Set up your ServiceNow instance to integrate with the Microsoft Azure Notification Hub. Setting enables the Microsoft Azure Notification Hub to authenticate requests from your ServiceNow instance.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Microsoft Azure Notification Hub spoke.
-   Role required: admin.

## Set up Microsoft Azure Resource Management connection alias

Set up the Microsoft Azure Resource Management connection alias to do the actions under the Notification Hub Management and Namespace Management categories of the Microsoft Azure Notification Hub spoke.

### Before you begin

Role required: admin

-   To view the procedure to set up the Microsoft Azure Resource Management connection alias, see [Set up the Microsoft Azure Resource Management spoke](setup-res-mngmt.md#).

## Set up Microsoft Azure Notification Hub SAS connection alias

Establish a connection between the Microsoft Azure Notification Hub SAS connection alias and the Microsoft Azure portal.

### Before you begin

Role required: admin

### About this task

The Microsoft Azure Notification Hub SAS connection alias enables you to do the actions in the Installation Management, Notification Management, and Registration Management categories of the Microsoft Azure Notification Hub

spoke.

### Procedure

1.  Log in to your ServiceNow instance.

2.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

3.  Select the **Integrations** tab.

4.  Select **Connections**.

5.  In the Search all connections field, search the Microsoft Azure Notification Hub SAS connection alias record.

    **Note:** The **Outbound** tab is enabled by default. Or else, toggle to enable it.

6.  On the Microsoft Azure Notification Hub SAS connection alias tile, select **View Details**.

7.  Select **Configure**.

8.  Fill the form.

    |Field|Description|
    |-----|-----------|
    |Connection name|Name of the connection record.|
    |Credential name|Name of the credential that is used to access the Microsoft Azure Notification Hub SAS.|
    |Shared Access Key Name|Name of the shared access key to the Microsoft Azure Notification Hub SAS.|
    |Shared Access Key|Shared access key to the Microsoft Azure Notification Hub SAS. Generate the key from the Microsoft Azure portal. To view the procedure, see [Generate shared access key for Microsoft Azure Notification Hub SAS](setup-azure-notif-hub.md#).|

9.  Select **Create**.


### Generate shared access key for Microsoft Azure Notification Hub SAS

Generate a shared access key that you must provide to create a connection between the Microsoft Azure Notification Hub SAS connection alias and the Microsoft Azure portal.

#### Before you begin

Role required: admin.

#### Procedure

1.  Log in to [https://portal.azure.com](https://portal.azure.com).

2.  Select **Notification Hubs**.

3.  Select the required notification hub and then select **Apply**.

4.  Select a notification hub to open it.

    The spoke performs the actions on the notification hub that you open.

5.  Under Manage, select **Access Policies**.

6.  Corresponding to the required policy, copy the string under the Connection String field.

    ![Copy the string.](../image/copy-string.png)

7.  From the string that you copied, copy the shared access key.

    Copy the value of the SharedAccessKey in the string.


**Related topics**  


[Set up Microsoft Azure Notification Hub SAS connection alias](setup-azure-notif-hub.md#)

