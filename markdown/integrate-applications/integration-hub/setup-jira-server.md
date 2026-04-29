---
title: Set up the Jira spoke for Jira Server
description: Integrate the ServiceNow instance and Jira Server using user name and password to authenticate ServiceNow requests.Create a credential record for the Jira account. The Jira spoke connection and credential alias uses this credential to authorize actions.Create a connection record for the Jira account. The connection and credential alias uses this connection to perform actions in Jira.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Jira Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
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

## Create credential record for the Jira spoke

Create a credential record for the Jira account. The Jira spoke connection and credential alias uses this credential to authorize actions.

### Before you begin

Role required: admin

### Procedure

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


## Create a connection record for the Jira spoke

Create a connection record for the Jira account. The connection and credential alias uses this connection to perform actions in Jira.

### Before you begin

Role required: admin

### Procedure

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


