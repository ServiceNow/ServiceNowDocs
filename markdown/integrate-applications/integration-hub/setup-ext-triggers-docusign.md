---
title: Set up triggers for the Docusign eSignature spoke
description: Set up the trigger to generate the callback URL on your ServiceNow instance.Create or enable the glide.oauth.inbound.client.credential.grant\_type.enabled system property to use the OAuth client credentials grant type for inbound integrations from the Docusign OAuth client to ServiceNow instance.Create an application registry in the ServiceNow instance to authenticate the inbound calls.Activate the trigger definition to generate the callback URL on your ServiceNow instance.Add a custom configuration in the Docusign account to send real‐time data updates to the ServiceNow instance.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Docusign eSignature Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up triggers for the Docusign eSignature spoke

Set up the trigger to generate the callback URL on your ServiceNow instance.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate and set up the Docusign eSignature spoke.
-   Role required: admin.

## Enable system property for client credentials grant type

Create or enable the glide.oauth.inbound.client.credential.grant\_type.enabled system property to use the OAuth client credentials grant type for inbound integrations from the Docusign OAuth client to ServiceNow instance.

### Before you begin

Role required: admin

### About this task

For more information about client credentials grant type, see [Client Credentials](https://www.servicenow.com/docs/access?context=client-credentials&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

### Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  Search for the `glide.oauth.inbound.client.credential.grant_type.enabled` system property.

3.  Open the record.

4.  For **Value**, enter `true`.

5.  Right-click the form header and click **Save**.


## Create an application registry to authenticate the inbound calls

Create an application registry in the ServiceNow instance to authenticate the inbound calls.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Click **New**.

3.  Select **Create an OAuth API endpoint for external clients**.

4.  On the form, fill in the fields.

<table id="table_jyr_bfl_b2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to identify the application registry record. For example, `Docusign External Trigger`.

</td></tr><tr><td>

OAuth Application User

</td><td>

User role to which the OAuth token flow is mapped.**Important:** By default, this field is not displayed on the Application Registries form. Configure the form layout to see the field on the form. For information about configuring the form layout, see [Configuring the form layout](https://www.servicenow.com/docs/access?context=configure-form-layout&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

</td></tr></tbody>
</table>5.  Right-click the form header and click **Save**.

    Application registry record is created and value of **Client Secret** is generated.

    Copy and record the values of **Client ID** and **Client Secret** for later use.


## Activate the trigger definition on ServiceNow instance

Activate the trigger definition to generate the callback URL on your ServiceNow instance.

### Before you begin

Role required: flow\_designer and connection\_admin.

### About this task

Docusign uses the callback URL to securely send the payload to the ServiceNow instance.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Select the **Integrations** tab.

3.  Toggle and enable the **Inbound** tab.

4.  Locate the **Docusign eSignature Spoke** card and select **View Details**.

    ![Locate the Docusign eSignature Spoke card.](../image/inbound-docusign.png)

5.  Select **Configure**.

    ![Configure the endpoint.](../image/comf-ext-trigger-docusign.png)

6.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Required roles|Roles using which the flow will be triggered. For example, select **admin**.|
    |Application Registry|Select the application registry you had created to authenticate inbound calls. For example, select **Docusign External Trigger**.|

    ![Activate the endpoint.](../image/conf-endpt-docusign.png)

7.  Click **Activate**.

    The endpoint is activated and the value of **URL** is generated.

    Copy and record the value of **URL** for later use.

    ![Copy the URL for later use.](../image/copy-url-docusign.png)


## Add configuration in Docusign account

Add a custom configuration in the Docusign account to send real‐time data updates to the ServiceNow instance.

### Before you begin

Role required: admin

### Procedure

1.  Log in to the Docusign account as an admin.

2.  Click **Admin**.

3.  Navigate to **Integrations** &gt; **Connect**.

4.  Under **Configurations**, click **Add Configuration** and select **Custom**.

5.  On the form, fill in the values.

<table id="table_oy2_j4l_b2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to identify the custom configuration record.

</td></tr><tr><td>

URL to Publish

</td><td>

Enter the URL that is generated when you activated the trigger definition in this format: `https://<ServiceNow-instance-name>.service-now.com/api/sn_docusign_spoke/docusign_esignature_external_trigger`.For more information, [Activate the trigger definition on ServiceNow instance](setup-ext-triggers-docusign.md#).

</td></tr><tr><td>

Data Format

</td><td>

Ensure that you select **REST v2.1**.

</td></tr><tr><td>

Event Message Delivery Mode

</td><td>

Select **Send Individual Messages \(SIM\)**.

</td></tr><tr><td>

Trigger Events

</td><td>

Expand **Envelope and Recipients** and select these events:-   Envelope Sent
-   Envelope Delivered
-   Envelope Signed/Completed
-   Envelope Declined
-   Envelope Voided
-   Envelope Deleted
-   Recipient Sent
-   Recipient Auto Responded
-   Recipient Delivered
-   Recipient Signed/Completed
-   Recipient Declined
![Triggers events to be selected.](../image/trigger-events-docusign.png)

Under **Include Data**, select the **Recipients** option. Select other options as per your requirement.

![Select the Recipients option.](../image/include-data.png)

</td></tr></tbody>
</table>6.  Under **Integration and Security Settings**, select the **Include OAuth \(Recommended\)** check box.

7.  Click **Add Configuration**.

    The custom configuration record is created.

8.  Click **Actions** for the custom configuration record that you created and select **Edit**.

    ![Edit the custom configuration.](../image/edit-conf-docusign.png)

9.  Under **Integration and Security Settings**, click **Manage OAuth**.

    The **OAuth 2.0** tab is displayed.

10. Enter the values of Client ID and Client Secret.

    These values are created when you create application registry record in ServiceNow instance. For more information, see [Create an application registry to authenticate the inbound calls](setup-ext-triggers-docusign.md#).

11. Enter **Authorization Server URL** in this format: `https://<ServiceNow-instance-name>.service-now.com/oauth_token.do`.

12. Click **Save**.


### What to do next

Create flows in Workflow Studio using these triggers as per your requirement. For more information, see [Create a flow with an external trigger](https://www.servicenow.com/docs/access?context=create-a-flow-with-an-external-trigger-definition&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

