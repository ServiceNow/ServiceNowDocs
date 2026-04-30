---
title: Set up the Microsoft Exchange Server spoke
description: Connect your ServiceNow instance with the Microsoft Exchange Server by setting up the connection and credential records for both the Microsoft Exchange Server that are provided when you install Integration Hub on your instance.Configure a connection for the Exchange alias to establish a connection between the ServiceNow instance and the Microsoft Exchange Server host.Configure a connection for the Exchange\_https alias to establish a connection between the ServiceNow instance and the Microsoft Exchange Server host.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Microsoft Exchange Server Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up the Microsoft Exchange Server spoke

Connect your ServiceNow instance with the Microsoft Exchange Server by setting up the connection and credential records for both the Microsoft Exchange Server that are provided when you install Integration Hub on your instance.

## Before you begin

-   Request the Integration Hub subscription.
-   Activate the latest Microsoft Exchange Server spoke plugin on your ServiceNow instance.
-   Role required: admin

## About this task

The Microsoft Exchange Server spoke provides two aliases: Exchange and Exchange\_https and their respective configuration templates as out of the box components when you install the Microsoft Exchange Server . These out of the box components enable you to easily set up the connection and credential records for both the aliases by just providing the connection and credential information. The out of the box components are already configured for you. To learn how to create the connections and credential records, see:

-   [Configure a connection for the Exchange alias](setup-msexchange.md#)
-   [Configure a connection for the Exchange\_https alias](setup-msexchange.md#)

You can perform all spoke actions except the Create Calendar Event For User and Lookup Room Availability actions. The Create Calendar Event For User and Lookup Room Availability actions are supported only on Exchange Server 2013.

**Note:** The user details that are provided in the credential record must have the application impersonation role.

To use the Create Calendar Event For User and Lookup Room Availability actions, perform the same steps again for the Exchange\_https connection and credential alias. MID Server isn’t necessary to perform this action.

## Configure a connection for the Exchange alias

Configure a connection for the Exchange alias to establish a connection between the ServiceNow® instance and the Microsoft Exchange Server host.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, toggle and enable the **Outbound** connections.

4.  Locate the **Exchange** alias.

    **Tip:** To find the alias, in the Search all connections field, enter `Exchange`.

    ![Search the Exchange alias on the Connections tab.](../image/search-alias-connections-tab.png "Search the Exchange alias on the Connections tab")

    The Exchange alias tile appears under the **Connections** tab.

5.  Click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Microsoft Exchange Server spoke, click **View Details**

        ![Configure the default connection.](../image/exchange-server-conn1.png "Default connection record")

    -   To manage more than one Microsoft Exchange Server spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](../../integrationhub/concept/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

    ![Configure button for Exchange alias.](../image/configure-button-exchange-alias.png "Configure button for Exchange alias")

6.  On the form, fill in the fields.

<table id="table_akz_3sh_vhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name that uniquely identifies the connection and credential record. For example, Microsoft Exchange.**Note:** The connection name of the first record is read-only. You can provide custom names for the subsequent records.

</td></tr><tr><td>

Host

</td><td>

Fully qualified domain name of the target host where the Microsoft Exchange Server is installed. For example, `<host>.<domain>.com`.

</td></tr><tr><td>

User Name

</td><td>

User name with access to the target Windows host.

</td></tr><tr><td>

Password

</td><td>

Password for the account.

</td></tr></tbody>
</table>    ![Provide the required details in the form.](../image/exchange-server-conn2.png "Configure Connection form")

7.  Select **Configure Connection**.

    The connection and credential record for the Exchange alias is created.


## Configure a connection for the Exchange\_https alias

Configure a connection for the Exchange\_https alias to establish a connection between the ServiceNow® instance and the Microsoft Exchange Server host.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, toggle and enable the **Outbound** connections.

4.  Locate the **Exchange\_https** alias.

    **Tip:** To find the alias, in the Search all connections field, enter `Exchange_https`.

    ![Search the Exchange alias on the Connections tab.](../image/search-alias-connections-tab.png "Search the Exchange_https alias on the Connections tab")

    The Exchange\_https alias tile appears under the **Connections** tab.

5.  Click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Microsoft Exchange Server spoke, click **View Details**

        ![Configure the default connection record.](../image/exchange-server-https-conn1.png "Default connection record")

    -   To manage more than one Microsoft Exchange Server spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](../../integrationhub/concept/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

    ![Configure button for Exchange_https connection record alias.](../image/set-exchange-https-alias-conn-record.png "Configure button for Exchange_https connection record alias")

6.  On the form, fill in the fields.

<table id="table_akz_3sh_vhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name that uniquely identifies the connection and credential record. For example, Exchange\_https.**Note:** The connection name of the first record is read-only. You can provide custom names for the subsequent records.

</td></tr><tr><td>

Host

</td><td>

Fully qualified domain name of the target host where the Microsoft Exchange Server is installed.

 For example, `https://mail.example.com/EWS/Exchange.asmx` can be the format of the host URL where

-   `mail.example.com` is the placeholder for your Exchange server's domain
-   `/EWS/Exchange.asmx` is the path to the Exchange Web Services \(EWS\) endpoint


</td></tr><tr><td>

User Name

</td><td>

User name with access to the target Windows host.

</td></tr><tr><td>

Password

</td><td>

Password for the account.

</td></tr></tbody>
</table>    ![Provide the required details in the form.](../image/exchange-server-https-conn2.png "Configure Connection form")

7.  Select **Configure Connection**.

    The connection and credential record for the Exchange\_https alias is created.


