---
title: Set up the Roadmunk spoke
description: Integrate the ServiceNow instance and Roadmunk by using an API access token to authenticate ServiceNow requests.Generate an API access token that authorizes access to the Roadmunk GraphQL API.Create a connection between your Roadmunk applications and your ServiceNow instance so that your instance can retrieve user data from your applications.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Roadmunk Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Set up the Roadmunk spoke

Integrate the ServiceNow instance and Roadmunk by using an API access token to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Roadmunk spoke.
-   Roadmunk role required: Account Admin.
-   Role required: admin.

## Generate a Roadmunk API access token

Generate an API access token that authorizes access to the Roadmunk GraphQL API.

### Before you begin

Role required: Roadmunk Account Admin

### Procedure

1.  From a web browser, open [Roadmunk](https://roadmunk.com/).

2.  Log in using your account admin credentials.

    The Roadmunk dashboard opens.

3.  On the left navigation menu of the Roadmunk dashboard, click your profile icon and then select **Account Settings**.

    Your account settings open.

4.  On the page header of your account settings, select the **Integrations** tab.

5.  Under Existing Integrations, click **Add an integration**.

6.  When prompted to select an integration to configure, select **API Tokens**.

    The Roadmunk API Tokens form opens.

7.  Enter a name for your API access token in the **Application Name** field.

8.  Click **Create API Token**.

    The API access token generates and then the API Token Created dialog box opens.

9.  On the dialog box, copy your API access token by clicking **Copy To Clipboard**.

    Save it in a secure location for later use.


## Create a Roadmunk connection

Create a connection between your Roadmunk applications and your ServiceNow instance so that your instance can retrieve user data from your applications.

### Before you begin

Role required: admin

### Procedure

1.  From your ServiceNow instance, navigate to **Process Automation** &gt; **Flow Designer**.

    The Flow Designer launches in a new tab.

2.  Select the **Connections** tab.

3.  Locate your Roadmunk connection and then click **Add Connection**.

    The Create Connection dialog box opens.

4.  On the dialog box, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Information|
    |Connection Name|Name of the Roadmunk connection. This field populates automatically.|
    |Connection URL|URL for the connection. This field is automatically set to **https://app-gateway.roadmunk.com**, where **app** is the default geographic region \(North America\) in which the connection is being created. If you are creating the connection outside of the default **app** \(North America\) region, you can change the value of the region to either **eu** \(Europe\) or **apac** \(Asia-Pacific Region\).|
    |Credential Information|
    |API Token|API access token that authorizes access to the Roadmunk GraphQL API. Enter the same API access token that you generated in [Generate a Roadmunk API access token](setup-roadmunk.md#).|

5.  Click **Create Connection**.


