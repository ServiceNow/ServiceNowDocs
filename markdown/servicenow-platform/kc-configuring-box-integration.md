---
title: Integrate Box in Knowledge Center
description: Configure a Box application and connect it to your ServiceNow instance so that knowledge authors can use Box as an external content source for knowledge article creation using Now Assist.Create an application on the Box Platform.Connect your ServiceNow instance to Box by configuring an OAuth entity and linking it to the REST message record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/kc-configuring-box-integration.html
release: australia
topic_type: concept
last_updated: "2026-05-28"
reading_time_minutes: 3
breadcrumb: [Configuring Knowledge Center, Knowledge Center, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Integrate Box in Knowledge Center

Configure a Box application and connect it to your ServiceNow instance so that knowledge authors can use Box as an external content source for knowledge article creation using Now Assist.

To integrate your Box account with Knowledge Center, you must have an admin access to the Box Dev Console for your organization. To use Box, each author must have a Box user account.

Complete this two-part configuration to enable the Box integration for knowledge article creation from Now Assist, in the Knowledge Center. First, create and authorize a Box application. Then, connect your ServiceNow instance to Box by configuring an OAuth entity and linking it to the REST message record. After you complete these steps, knowledge authors can select Box as a content source when they create articles with Now Assist.

## Configure Box application

Create an application on the Box Platform.

### Before you begin

Role required: admin

### Procedure

1.  In the Box Dev Console, navigate to **My Platform Apps** &gt; **New App**.

2.  Create a **Client Credentials Grant** app.

    Give the app a descriptive name, for example, "ServiceNow KC Open Prompt Integration".

3.  Navigate to **General Settings** &gt; **App Info** and note the **Enterprise ID** value.

    You need this value later when you set the system property in ServiceNow.

4.  Set the **App Access Level** to **App + Enterprise Access**.

5.  Under **Application Scopes**, enable the following content actions.

    |Scope|Purpose|
    |-----|-------|
    |Read all files and folders stored in Box|Allows the integration to search and retrieve file content for article creation.|
    |Write all files and folders stored in Box|Allows the integration to store files when required by the workflow.|
    |Manage AI|Allows the integration to use Box AI capabilities.|

6.  Under **Administrative Actions**, enable **Manage users**.

7.  Under **Additional Configuration**, enable the following options:

    -   **Make API calls using the as-user header**
    -   **Generate user access tokens**
8.  Request the Box Admin to authorize the app.

    Box creates a service account when the admin authorizes the app. This service account handles API calls on behalf of the integration.

9.  Open the app's **Configuration** tab and copy the **Client ID** and **Client Secret** values.

    You need these values to configure the OAuth entity in your ServiceNow instance.


## Configure Application Registry for Box integration

Connect your ServiceNow instance to Box by configuring an OAuth entity and linking it to the REST message record.

### Before you begin

Role required: admin

### Procedure

1.  In your ServiceNow instance, navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Select **New** and then select **Connect to a third party OAuth Provider**.

3.  Complete the following fields on the OAuth entity form.

    |Field|Value|
    |-----|-----|
    |Name|`KC Open Prompt - Box Integration`.|
    |Client ID|Enter the Client ID value from the Box app's Configuration tab.|
    |Client Secret|Enter the Client Secret value from the Box app's Configuration tab.|
    |OAuth API Script|Search and select **OAuthUtilBox**.|
    |Default Grant type|Select **Client Credentials**.|
    |Token URL|Enter `https://api.box.com/oauth2/token`.|
    |Send Credentials|Select **In Request Body \(Form URL-Encoded\)**.|

4.  **Save** the record.

5.  Create a default OAuth Entity Profile with the grant type set to **Client Credentials**.

6.  Set the system property `sn_km_center.box_integration_enterprise_id` to the Enterprise ID you noted in step 3.

    Navigate to **All** &gt; **sys\_properties.list** and search for the property name to locate and update it.

7.  Open the REST Message record **Open Prompt - Box Integration**.

    Navigate directly to the record at `sys_rest_message.do?sys_id=e2e7869f938c83905579f2d89803d6b7`.

8.  Under **Authentication**, connect the OAuth profile you created.

9.  Select **Get OAuth Token** to verify the connection.

    The system retrieves an OAuth token from Box. A successful response confirms that the integration is connected and authorized.


### Result

The Box integration is active. The **Box** option appears under the Integration section of the **Source** drop-down on the article creation page in the Knowledge Center. Knowledge authors with a matching Box user account can now select Box as a content source when they create articles with Now Assist.

**Related topics**  


[Create knowledge articles using Now Assist and Box](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/kc-create-article-with-Box.md)

