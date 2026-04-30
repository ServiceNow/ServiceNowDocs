---
title: Set up the SmartRecruiters spoke
description: Integrate the ServiceNow instance and SmartRecruiters by using API credentials to authenticate ServiceNow requests.Generate an API key for authenticating SmartRecruiters API requests.Create a connection between your SmartRecruiters applications and your ServiceNow instance so that your instance can retrieve user data from your applications.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [SmartRecruiters Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up the SmartRecruiters spoke

Integrate the ServiceNow instance and SmartRecruiters by using API credentials to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate SmartRecruiters spoke.
-   SmartRecruiters role required: admin
-   Role required: admin

## Generate a SmartRecruiters API key

Generate an API key for authenticating SmartRecruiters API requests.

### Before you begin

Role required: SmartRecruiters admin

### Procedure

1.  From a web browser, open [SmartRecruiters](https://www.smartrecruiters.com/).

2.  Sign in using your admin credentials.

    The Administrator's view of the SmartRecruiters portal opens.

3.  On the page header of the SmartRecruiters portal, click your profile icon and then select **Settings/Admin**.

    Your SmartRecruiter settings open.

4.  Under Company Settings, locate the Administration section and then select **Apps &amp; Integrations**.

    The Apps &amp; Integrations page opens.

5.  Select the **CREDENTIALS** tab and then click **NEW CREDENTIAL**.

6.  When prompted to select the type of credential that you want to generate for your applications, select **API key**.

7.  Click **Next**.

8.  Enter a name for your API key in the **Credentials name** field.

9.  Enter a description for your API key in the **Description** field.

10. Click **Generate**.

    SmartRecruiters automatically generates and displays your API key.

11. Copy your API key and save it in a secure location for later use.


## Create a SmartRecruiters connection

Create a connection between your SmartRecruiters applications and your ServiceNow instance so that your instance can retrieve user data from your applications.

### Before you begin

Role required: admin

### Procedure

1.  From your ServiceNow instance, navigate to **Process Automation** &gt; **Flow Designer**.

    The Flow Designer launches in a new tab.

2.  Select the **Connections** tab.

3.  Locate your SmartRecruiters connection and then click **Add Connection**.

    The Create Connection dialog box opens.

4.  On the dialog box, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Information|
    |Connection Name|Name of the SmartRecruiters connection. This field populates automatically.|
    |Connection URL|URL for the connection. This field is automatically set to **https://api.smartrecruiters.com**.|
    |Credential Information|
    |API Key|API key for your SmartRecruiters applications. Enter the same API key that you generated in [Generate a SmartRecruiters API key](setup-smartrecruiters.md#).|

5.  Click **Create Connection**.


