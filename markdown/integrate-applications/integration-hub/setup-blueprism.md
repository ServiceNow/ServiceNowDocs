---
title: Set up the Blue Prism spoke
description: Integrate your ServiceNow instance with the Blue Prism server to have the requests from your ServiceNow instance authenticated.Configure the Dispatch Framework and Process info utilities in your Blue Prism environment to enable integration with ServiceNow.Create a connection and credential record to enable your ServiceNow instance to connect to the Blue Prism ProcessInfo utility. The record is a single form that contains all the information needed to connect to the Blue Prism ProcessInfo utility every time.Create a connection and credential record to enable your instance to connect to the Blue Prism Process Dispatcher utility. The record is a single form that contains all the information needed to connect to the Blue Prism ProcessInfo utility every time.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Blue Prism Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Blue Prism spoke

Integrate your ServiceNow instance with the Blue Prism server to have the requests from your ServiceNow instance authenticated.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Blue Prism spoke.
-   Role required: admin.

## Configure Blue Prism application

Configure the Dispatch Framework and Process info utilities in your Blue Prism environment to enable integration with ServiceNow.

### Before you begin

Blue Prism Digital Exchange account.

Role required: admin.

### Procedure

1.  Log in to [Blue Prism Digital Exchange](https://digitalexchange.blueprism.com/saml/login).

2.  Click **Link to Asset** of [Dispatch Framework](https://digitalexchange.blueprism.com/dx/entry/9648/solution/process-dispatch-framework) utility.

    You’re redirected to the Dispatch Framework repository on GitHub.

3.  Complete the steps mentioned in the Blue Prism Process Dispatch Framework User Guide.

4.  Click **Link to Asset** of [Process Info](https://digitalexchange.blueprism.com/dx/entry/9648/solution/process-information-utility-2) utility.

    You’re redirected to the Process Info repository on GitHub.

5.  Complete the steps mentioned in the Blue Prism Process Info VBO User Guide.

    Your Blue Prism environment is ready for integration with your ServiceNow instance.


## Create Connection and Credential record for Blue Prism ProcessInfo

Create a connection and credential record to enable your ServiceNow instance to connect to the Blue Prism ProcessInfo utility. The record is a single form that contains all the information needed to connect to the Blue Prism ProcessInfo utility every time.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection and Credential Aliases**.

2.  Open the record for **BluePrismProcessInfo**.

3.  From the **Related Links** section, Click **Create New Connection &amp; Credential**.

4.  On the form, fill these fields:

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name of the connection. Default value is `Blue Prism Process Info Connection`.|
    |Connection URL|URL used to connect to the connection to the Blue Prism environment.|
    |Database Credential Name|Credential name of the database. Default value is `DB Read User`.|
    |Database Server Address|Database server address in the Blue Prism environment.|
    |Database Name|Name of the database. Default value is `BluePrism`.|
    |Credential Name|Blue Prism Process Info Credentials.|
    |User Name|User name that the Blue Prism Process Info server authenticates.|
    |Password|Password that the Blue Prism Process Info server authenticates.|

5.  Click **Create**.

    A new connection and credential record is created in the Connections tab. This is the default record unless you create another record and set that as default.

    ![Default connection and credential record created for Blue Prism spoke.](../image/blue-prism-procinfo-connection-credential-saved.png "Default connection and credential record created")

6.  Click to open the record.

7.  Enable the **Use MID server** option.

    ![Mid server option in Blue Prism connection and credential record.](../image/select-mid-server-option-blue-prism.png "Mid server option")

    To set up the MID Server for this spoke, see [Set up MID Server for a spoke](config-adv-mid-settings-for-oauth-on-mid.md).


## Create Connection and Credential record for Blue Prism Process Dispatcher

Create a connection and credential record to enable your instance to connect to the Blue Prism Process Dispatcher utility. The record is a single form that contains all the information needed to connect to the Blue Prism ProcessInfo utility every time.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection and Credential Aliases**.

2.  Open the record for **BluePrismProcessDispatcher**.

3.  From the **Related Links** section, click **Create New Connection &amp; Credential**.

4.  On the form, fill these fields:

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name of the connection. Default value is `Blue Prism Process Dispatcher Connection`.|
    |Connection URL|URL used to connect to the Blue Prism environment.|
    |Runtime Credential Name|Credential with runtime access configured in the Blue Prism environment.|
    |Credential Name|Name of the credential. Default value is `Blue Prism Process Dispatcher Credentials`.|
    |User Name|User name that the Blue Prism Process Dispatcher server authenticates.|
    |Password|Password that the Blue Prism Process Dispatcher server authenticates.|

5.  Click **Create**.

    A new connection and credential record is created in the Connections tab. This is the default record unless you create another record and set that as default.

    ![Blue Prism Process Dispatcher connection and credential record.](../image/blueprism-pd-conn-cred-created.png "Blue Prism Process Dispatcher connection and credential record")

6.  Click to open the record.

7.  Enable the **Use MID server** option.

    To set up the MID Server for this spoke, see [Set up MID Server for a spoke](config-adv-mid-settings-for-oauth-on-mid.md).


