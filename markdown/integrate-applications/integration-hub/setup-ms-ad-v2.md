---
title: Set up the Microsoft Active Directory v2 spoke
description: Integrate the ServiceNow instance and the Microsoft Active Directory v2 spoke by using the Windows credentials to authenticate ServiceNow requests.Configure a connection record to connect to the Microsoft Active Directory v2 spoke host and enable the Microsoft Active Directory v2 spoke connections and credentials alias to authorize actions.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Microsoft Active Directory v2 Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Microsoft Active Directory v2 spoke

Integrate the ServiceNow instance and the Microsoft Active Directory v2 spoke by using the Windows credentials to authenticate ServiceNow requests.

Demonstrates setting up the Microsoft Active Directory v2 spoke. 

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Microsoft Active Directory v2 spoke.
-   Role required: admin

## Configure a connection record for the Microsoft Active Directory v2 spoke

Configure a connection record to connect to the Microsoft Active Directory v2 spoke host and enable the Microsoft Active Directory v2 spoke connections and credentials alias to authorize actions.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Click **Connections**.

4.  Toggle and enable the **Outbound** connections.

5.  Locate the **AD\_v2** connection alias and click **View Details**.

    ![Configure connection and credentials for Microsoft Active Directory v2.](../image/click-add-connection-ad-v2.png)

    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**

    ![Configure the default alias.](../image/configure-def-alias-adv2.jpg)

6.  Enter the following details in the form.

    |Field|Information|
    |-----|-----------|
    |Connection name|Name to uniquely identify the record.|
    |Host|Fully qualified domain name or IP address of the target host where the Microsoft AD is installed. For example, `<host>.<domain>.com`.|
    |User name|User name with access to the target Windows host.|
    |Password|Password for the account.|

    ![Configure connection form.](../image/create-connection-form.png "Create connection form")

7.  Click **Configure Connection**.


### What to do next

To use the spoke actions, your instance must have a MID Server set up and configured to use PowerShell. For more information about running actions on the MID Server, see [Integration steps](../../integrationhub/concept/integration-steps.md). For more information about the MID Server, see MID Server.

To set up the MID Server for this spoke, see [Set up MID Server for a spoke](config-adv-mid-settings-for-oauth-on-mid.md).

**Note:** You must install the MID Server and Microsoft Active Directory on different servers.

