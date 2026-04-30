---
title: Set up the Jira spoke for Jira Server
description: Integrate the ServiceNow instance and Jira Server using user name and password to authenticate ServiceNow requests.Integrate the ServiceNow instance and Jira Server using user name and password to authenticate ServiceNow requests.Create a credential record for the Jira account. The Jira spoke connection and credential alias uses this credential to authorize actions.Create a connection record for the Jira account. The connection and credential alias uses this connection to perform actions in Jira.Integrate the ServiceNow instance and Jira Server using API Token to authenticate ServiceNow requests.Generate a personal access token from the Jira Server instance.Create an API key credential record to authenticate the requests from ServiceNow.Create a connection record for the Jira account. The connection and credential alias uses this connection to perform actions in Jira.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Jira Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up the Jira spoke for Jira Server

Integrate the ServiceNow instance and Jira Server using user name and password to authenticate ServiceNow requests.

## Before you begin

**Important:**

-   Starting with the Australia release, instructions for generating and using API tokens have been removed from our documentation to align with Atlassian's Acceptable Use Policy.
-   As of February 15, 2024 PT, your Jira Server products reached the end of support. Starting from Jira Software 9.13 and Jira Service Management 5.13, new Jira releases support only Data Center licenses.
-   End of life for impacted Data Center products will take place on March 28, 2029 at 23:59 PST. Data Center subscriptions and any associated Marketplace apps will expire on this date, making Data Center products and apps read-only. For more information, see [Data Center EOL General Questions](http://atlassian.com/licensing/data-center-end-of-life#data-center-eol-general-questions).
-   Apps that collect API tokens to create individual 3LO apps don't comply with Atlassian security requirements for cloud apps and Atlassian acceptable use policy.

-   Request an Integration Hub subscription.
-   Activate the Jira spoke.
-   Role required: admin.

## Option 1: Using user name and password

Integrate the ServiceNow instance and Jira Server using user name and password to authenticate ServiceNow requests.

### Before you begin

Role required: admin

### Create credential record for the Jira spoke

Create a credential record for the Jira account. The Jira spoke connection and credential alias uses this credential to authorize actions.

#### Before you begin

Role required: admin

#### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays the message `What type of Credentials would you like to create?`

3.  Select **Basic Auth Credentials**.

4.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the credential record for the Jira spoke. For example, `Jira Data Center Basic Cred`.|
    |Username|Username to log in to the Jira Data Center or Jira Server.|
    |Password|Password to log in to the Jira Data Center or Jira Server.|

5.  Right-click the form header and click **Save**.


### Create a connection record for the Jira spoke

Create a connection record for the Jira account. The connection and credential alias uses this connection to perform actions in Jira.

#### Before you begin

Role required: admin

#### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open the alias record for **Jira** that shipped with the spoke.

3.  On the **Connections** tab, click **New**.

    The system displays a blank HTTP\(s\) Connection form.

4.  Enter these values and click **Submit**.

    |Field|Value required|
    |-----|--------------|
    |Name|Enter any name to uniquely identify the connection record. For example, enter `Jira cloud OAuth Connection`.|
    |Credential|Select the Credential record created for Jira. For example, select **Jira Data Center Basic Cred**.|
    |Connection URL|Base URL of the Jira server.|

5.  Click **Submit**.

    The Jira spoke is configured to use Basic Auth credentials.


## Option 2: Using API Token

Integrate the ServiceNow instance and Jira Server using API Token to authenticate ServiceNow requests.

### Before you begin

**Important:** Apps that collect API tokens to create individual 3LO apps don't comply with Atlassian security requirements for cloud apps and Atlassian acceptable use policy.

Role required: admin

### Generate a personal access token

Generate a personal access token from the Jira Server instance.

#### Before you begin

-   Access to Jira Server instance.
-   Role required: admin

#### Procedure

1.  Log in to the Jira Server instance as an admin.

2.  Click the user profile icon and click **Profile**.

3.  Under **Personal Access Tokens**, click **Create token**.![Create a personal access token.](../image/jira-spoke-server-api-token.png)

4.  On the Create a personal access token form, fill in the required values.![Fill in the values to create a personal access token.](../image/jira-spoke-server-api-token1.png)

    The value of personal access token is generated and displayed. Copy this value for later use.![Copy the value of the generated token.](../image/jira-spoke-server-api-token2.png)


### Create a credential record for the Jira spoke

Create an API key credential record to authenticate the requests from ServiceNow.

#### Before you begin

Role required: admin

#### Procedure

1.  Navigate to **All** &gt; **Integration Hub** &gt; **Connection &amp; Credential Aliases** &gt; **Credentials**.

2.  Click **New**.

    The system displays the message, `What type of Credentials would you like to create?`

3.  Select **API Key Credentials**.

4.  On the form, fill these values.

<table id="table_h4b_lr3_bzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to identify the credential record. For example, `Jira Server API Token Cred`.

</td></tr><tr><td>

API Key

</td><td>

Enter value in this format: `Bearer <Personal Access Token>`.`<Personal Access Token>` is the value of personal access token you had created in the Jira system dashboard.

</td></tr></tbody>
</table>5.  Click **Submit**.


### Create a connection record for the Jira spoke

Create a connection record for the Jira account. The connection and credential alias uses this connection to perform actions in Jira.

#### Before you begin

Role required: admin

#### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open the alias record for **Jira** that shipped with the spoke.

3.  On the **Connections** tab, click **New**.

    The system displays a blank HTTP\(s\) Connection form.

4.  Enter these values and click **Submit**.

    |Field|Value required|
    |-----|--------------|
    |Name|Enter any name to uniquely identify the connection record. For example, enter `Jira Server API Token Connection`.|
    |Credential|Select the Credential record created for Jira. For example, select **Jira Server API Token Cred**.|
    |Connection URL|Enter the URL of your Jira Server instance.|

5.  In the Attributes related list, provide these values.

    1.  Enter the value `2` for **api\_version**.

    2.  Enter the value `server` for **server\_type**.

    ![Set the value of server_type to server.](../image/jira-spoke-attribute-server.png)

6.  Click **Submit**.


