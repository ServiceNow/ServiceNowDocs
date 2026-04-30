---
title: Set up the Pluralsight spoke
description: Integrate the ServiceNow instance and your Pluralsight Skills account using an API key to have the ServiceNow instance requests authenticated by the Pluralsight host.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Pluralsight Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Pluralsight spoke

Integrate the ServiceNow instance and your Pluralsight Skills account using an API key to have the ServiceNow instance requests authenticated by the Pluralsight host.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Pluralsight spoke.
-   Admin access to the Pluralsight Skills account.
-   Role required: admin.

## About this task

This task enables you to integrate your ServiceNow instance with the Pluralsight host. See the flow, as given in the image below.![Flow to set connection and credential record for Pluralsight spoke.](../image/conn-cred-record-pluralsight.png)

## Procedure

1.  Create an API key in your Pluralsight Skills account.

    1.  Log in to your [Pluralsight Skill account](https://app.pluralsight.com/id/) as an admin.

    2.  Navigate to **Account** and click the **Integrations** tab.

    3.  Click the [Pluralsight Developer Portal](https://developer.pluralsight.com/) link.

        ![Link to the Pluralsight Developer Portal](../image/pluralsight-dev-portal.png)

    4.  In the [Pluralsight Developer Portal](https://developer.pluralsight.com/), click the **Manage Keys** tab.

    5.  Click **Add Api Key**.

        ![Add API Key](../image/pluralsight-add-api.png)

    6.  On the form, fill the fields and provide write permissions to the API Key.

        ![Add API Key](../image/pluralsight-api-key.png)

    7.  Copy the API Key for later use.

        ![Copy the API key](../image/pluralsight-copy-api-key.png)

2.  Log in to your ServiceNow instance.

3.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

4.  Click the **Integrations** tab.

5.  Under **Connections**, toggle and enable the **Outbound** connections.

6.  Locate the alias for **Pluralsight** and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Pluralsight spoke, click **View Details**.

        ![Pluralsight connection.](../image/pluralsight-connection.png)

    -   To manage more than one Pluralsight spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](../../integrationhub/concept/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

    ![Configure button for configuring Pluralsight spoke connection and credentials.](../image/configure-button-pluralsight-conn-cred.png)

7.  On the Configure Connection form, fill the values,

    | | |
    |---|---|
    |Connection Name|Name of the connection between the ServiceNow instance and the Pluralsight host. The connection name is read-only.|
    |Connection URL|The URL to the Pluralsight skills account. Enter `https://paas-api.pluralsight.com/`|
    |API Key|API key generated earlier from the Pluralsight developers portal.|

    ![Configure the default connection.](../image/pluralsight-conf-template.png)

8.  Click **Configure Connection**.

    The connection and credentials connection record is created.


