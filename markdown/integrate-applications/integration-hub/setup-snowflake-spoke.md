---
title: Set up the Snowflake spoke
description: Integrate the ServiceNow instance and Snowflake spoke by using the OAuth credentials to authenticate ServiceNow requests.Add and configure a Snowflake connection to authenticate ServiceNow requests.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Snowflake Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Set up the Snowflake spoke

Integrate the ServiceNow instance and Snowflake spoke by using the OAuth credentials to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Snowflake spoke.
-   Role required: admin.

## Configure a connection for Snowflake spoke

Add and configure a Snowflake connection to authenticate ServiceNow requests.

### Before you begin

-   Get the OAuth client ID and client secret for your Snowflake account. For more information, see [Snowflake OAuth](https://docs.snowflake.com/en/sql-reference/sql/create-security-integration-oauth-snowflake).
-   Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, toggle and enable the **Outbound** connections.

4.  Locate the alias for **Snowflake** and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Snowflake spoke, click **View Details**.![Snowflake connection template](../image/snowflake-conn-template.png)
    -   To manage more than one Snowflake connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see[Supporting multiple connections](../../integrationhub/concept/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

    ![Configure Snowflake connection template](../image/snowflake-conn-config.png)

5.  On the **Configure Connection** form, fill in the fields:

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name to uniquely identify the connection.|
    |Connection URL|URL to connect to Snowflake. Enter the URL in this format: `https://<your_domain>.snowflakecomputing.com`.|
    |Application Registry Name|Name of the application registry.|
    |Credentials Name|Name to uniquely identify the credentials. For example, `Snowflake credential`.|
    |OAuth Client ID|OAuth client ID of your Snowflake account.|
    |OAuth Client Secret|OAuth client secret of your Snowflake account.|
    |Authorization URL|Snowflake authorization URL. Enter the URL in this format: `https://<your_domain>.snowflakecomputing.com/oauth/authorize`|
    |Token URL|URL from which the ServiceNow instance obtains the access token. Enter the URL in this format: `https://<your_domain>.snowflakecomputing.com/oauth/token-request`|
    |Oauth Entity Profile Name|OAuth Entity Profile Name for your Snowflake account.|
    |OAuth Redirect URL|OAuth callback endpoint in this format: `https://<instance>.service-now.com/oauth_redirect.do` is auto-populated.|

6.  Click **Configure Configure and Get OAuth Token**.


### Result

The spoke connection is configured and ready to be used.

