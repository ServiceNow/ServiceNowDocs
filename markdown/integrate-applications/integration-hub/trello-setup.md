---
title: Set up the Trello spoke
description: Integrate the ServiceNow instance and Trello by creating an API key in Trello to authenticate ServiceNow requests.Generate a Trello API key and token to get access to the Trello portal.Set up your ServiceNow instance to add the Trello API key and API token.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Trello Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Trello spoke

Integrate the ServiceNow instance and Trello by creating an API key in Trello to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Trello spoke.
-   Role required: admin.

## Generate Trello API key and token

Generate a Trello API key and token to get access to the Trello portal.

### Before you begin

Trello Role required: admin

Verify that you have a managed user account and Atlassian admin access.

### Procedure

1.  Go to [Trello](https://trello.com/).

2.  Log in as an enterprise admin.

3.  Go to [Developer API Keys](https://trello.com/app-key).

4.  Copy the API key from Personal Key on the Developer API keys page.

5.  In the following link, replace \{YourAPIKey\} with the API key that you copied in the last step and open the link.

    `https://trello.com/1/authorize?expiration=never&scope=read,write,account&response_type=token&name=ServerToken&key={YourAPIKey}`

    For example, if your API key is 123xyz, then open the following link- `https://trello.com/1/authorize?expiration=never&scope=read,write,account&response_type=token&name=ServerToken&key=123xyz`

    The MyPersonalToken page appears and asks if you want to give access to your account.

6.  Select **Allow**.

    An API token is generated. Copy this API token and store it securely.


## Create a Trello connection

Set up your ServiceNow instance to add the Trello API key and API token.

### Before you begin

ServiceNow Role required: admin

### Procedure

1.  Log in to your ServiceNow instance.

2.  Navigate to **Process Automation** &gt; **Flow Designer**.

3.  Select the **Connections** tab.

4.  Locate the Trello Alias connection alias and select **View Details**.

5.  Configure the Trello spoke.

    -   If you’re configuring the spoke for the first time, select **Configure**.
    -   If you aren't configuring the spoke for the first time, select **Edit**.
6.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name to identify the connection record.|
    |Connection URL|Enter the URL as `https://api.trello.com/`.|
    |API Key|The API key that you copied from the Trello portal.|
    |API Token|The API token that you copied from the Trello portal.|

7.  Select **Configure Connection**.


