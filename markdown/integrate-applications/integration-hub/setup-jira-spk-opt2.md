---
title: Set up the Jira spoke for Jira Cloud
description: Integrate your ServiceNow instance with the Jira Cloud instance to authenticate the requests from ServiceNow.Integrate the ServiceNow instance with your Jira account using OAuth to authenticate ServiceNow requests.Obtain the value of Cloud ID of the Jira Cloud instance. This value is required during the configuration of the connection record in your ServiceNow instance.Add and configure a Jira connection to authenticate ServiceNow requests in Jira spoke.Integrate the ServiceNow instance with your Jira account using OAuth to authenticate ServiceNow requests.Create a credential record for the Jira account. The Jira spoke connection and credential alias uses this credential to authorize actions.Create a connection record for the Jira account. The connection and credential alias uses this connection to perform actions in Jira.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Jira Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Jira spoke for Jira Cloud

Integrate your ServiceNow instance with the Jira Cloud instance to authenticate the requests from ServiceNow.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Jira spoke.
-   Role required: admin.

## About this task

**Important:**

Starting with the Australia release, instructions for generating and using API tokens have been removed from our documentation to align with Atlassian's Acceptable Use Policy. See the Atlassian blog, [Building Secure and Scalable Integrations: Our Guidance for Third-Party Apps](https://www.atlassian.com/blog/developer/building-secure-and-scalable-integrations-our-guidance-for-third-party-apps) for more information.

## Option 1: Using OAuth authentication \(Authorization Code grant type\)

Integrate the ServiceNow instance with your Jira account using OAuth to authenticate ServiceNow requests.

### Before you begin

Role required: admin.

### Obtain the value of Cloud ID

Obtain the value of Cloud ID of the Jira Cloud instance. This value is required during the configuration of the connection record in your ServiceNow instance.

#### Before you begin

Role required: admin

#### Procedure

1.  Log in to [Atlassian Administration](https://admin.atlassian.com/) as an admin.

2.  Click **Select** against the required organization.

3.  From the **Jira Software** product, click **Manage product access**.

    A new window is opened and the URL is in this format: `https://admin.atlassian.com/s/<Cloud-ID>/apps`.

4.  Copy the value of the Cloud ID for later use.


### Configure a connection for Jira spoke

Add and configure a Jira connection to authenticate ServiceNow requests in Jira spoke.

#### Before you begin

Role required: admin

#### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, the **Outbound** connections are displayed by default.

4.  Locate the **Jira** connection alias and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Jira spoke, click **View Details**.
    -   To manage more than one Jira spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](../../integrationhub/concept/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

5.  On the **Connection** form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name to uniquely identify the connection. For example, `Jira Spoke OAuth basic conn`.|
    |Connection URL|URL of your Jira instance in this format: `https://api.atlassian.com/ex/jira/{cloud-id}/`. Replace `{cloud-id}` with value of the Cloud ID you had obtained previously.|
    |Scopes|By default, these scopes are provided `read:jira-work, read:jira-user, write:jira-work, manage:jira-project, manage:jira-configuration, manage:jira-webhook, manage:jira-data-provider, delete:sprint:jira-software, read:sprint:jira-software, write:sprint:jira-software, read:board-scope:jira-software, read:project:jira, read:jql:jira, read:issue-details:jira, read:me, read:account, offline_access`. You can modify the scopes as per your requirement.|

    ![](../image/jira-new-conf-temp.jpg)

6.  Click **Save and Get OAuth Token**.


## Option 2: Using OAuth authentication \(Client Credentials grant type\)

Integrate the ServiceNow instance with your Jira account using OAuth to authenticate ServiceNow requests.

### Before you begin

-   In your Jira cloud instance, [Create OAuth 2.0 credential for service accounts](https://support.atlassian.com/user-management/docs/create-oauth-2-0-credential-for-service-accounts/).

    Save the values of **Client ID**, **Client Secret**, and **Cloud ID**. You will need these for configurations in ServiceNow instance.

-   Role required: admin.

### Create an application registry record

#### Before you begin

Role required: admin

#### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Click **New**.

    The system displays the message `What kind of OAuth application?`.

3.  Select **Connect to a third party OAuth Provider**.

4.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the application registry record. For example, `Jira Client Credentials OAuth`.|
    |Client ID|Client ID generated when the OAuth 2.0 integration was created in Atlassian Developer console.|
    |Client Secret|Client secret generated when the OAuth 2.0 integration was created in Atlassian Developer console.|
    |Default Grant type|Grant type used to establish the token. Select **Client Credentials**.|
    |Token URL|OAuth server token endpoint. Enter: `https://auth.atlassian.com/oauth/token`.|
    |Token Revocation URL|OAuth server token revocation endpoint. Enter: `https://auth.atlassian.com/oauth/token`.|
    |Active|Select the check box.|

5.  In the **OAuth Entity Scopes** tab, create these entity scope records.

    |Name|OAuth scope|
    |----|-----------|
    |Classic scopes|`manage:jira-configuration manage:jira-project manage:jira-webhook read:jira-work read:jira-user write:jira-work`|
    |Granular Scopes|`delete:sprint:jira-software read:issue-details:jira read:jql:jira read:sprint:jira-software write:sprint:jira-software read:board-scope:jira-software read:project:jira`|

6.  Right-click the form header and click **Save**.

    The record is saved and a OAuth Entity Profile record under the **OAuth Entity Profiles** tab.

7.  Click the **OAuth Entity Profiles** tab and open the default profile record.

8.  Verify these values.

    -   **Grant type** is set to **Client Credentials**.
    -   Scope records previously created are listed under the **OAuth Entity Profile Scopes** related list.
9.  Click **Update**.


### Create credential record for the Jira spoke

Create a credential record for the Jira account. The Jira spoke connection and credential alias uses this credential to authorize actions.

#### Before you begin

Role required: admin

#### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays the message `What type of Credentials would you like to create?`

3.  Select **OAuth 2.0 Credentials**.

4.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the credential record for the Jira spoke. For example, `Jira client credential cred`.|
    |OAuth Entity Profile|Select the OAuth entity profile record that was created when the application registry record is configured. For more information, see [Create an application registry record](setup-jira-spk-opt2.md#).|

5.  Right-click the form header and click **Save**.

6.  Click the **Get OAuth Token** related link.


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

<table id="table_vsw_lkv_4fb"><thead><tr><th>

Field

</th><th>

Value required

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter any name to uniquely identify the connection record. For example, enter `Jira cloud OAuth Connection`.

</td></tr><tr><td>

Credential

</td><td>

Select the Credential record created for Jira. For example, select **Jira cloud OAuth credential**.

</td></tr><tr><td>

Connection URL

</td><td>

Enter the URL of your Jira instance in this format: `https://api.atlassian.com/ex/jira/<Cloud-ID>`.For information about obtaining the value of Cloud ID, see [Obtain the value of Cloud ID](setup-jira-spk-opt2.md#).

</td></tr></tbody>
</table>5.  Click **Submit**.

    The Jira spoke is configured to use OAuth 2.0 Client Credentials via the service account.


