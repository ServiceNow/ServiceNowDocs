---
title: Set up the SAP Commerce Cloud spoke
description: Integrate your ServiceNow instance with the SAP Commerce Cloud to automate various actions on the SAP Commerce Cloud. For example, you can set up a flow that looks up a shopping cart at a specified time every day.Generate the credentials that you use to create the connection record for the SAP Commerce Cloud spoke. Your ServiceNow instance uses the connection record connect with the SAP Commerce Cloud.Create a connection record that enables your ServiceNow instance to connect with the SAP Commerce Cloud record. The connection record has the underlying connection information required to integrate with SAP Commerce Cloud.Integrate the ServiceNow instance and SAP Commerce Cloud spoke by creating a custom OAuth application in SAP Commerce Cloud to authenticate ServiceNow requests.Create a connection record for your SAP Commerce Cloud account. The SAP Commerce Cloud connection and credential aliases use these connections to perform actions in SAP Commerce Cloud.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [SAP Commerce Cloud Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up the SAP Commerce Cloud spoke

Integrate your ServiceNow instance with the SAP Commerce Cloud to automate various actions on the SAP Commerce Cloud. For example, you can set up a flow that looks up a shopping cart at a specified time every day.

## Before you begin

-   Request an Integration Hub subscription.
-   Install the SAP Commerce Cloud plugin.
-   Role required: admin
-   Access to the SAP Backoffice account.

## Create the SAP Commerce Cloud credentials

Generate the credentials that you use to create the connection record for the SAP Commerce Cloud spoke. Your ServiceNow instance uses the connection record connect with the SAP Commerce Cloud.

### Before you begin

Role required: admin

Access to the SAP Backoffice account.

### Procedure

1.  Log in to the SAP Backoffice account.

2.  On the left panel, go to **System** &gt; **OAuth** &gt; **OAuth Clients**.![OAuth Client navigation.](../image/sap-cloud-commerce-spoke-oauth-client-nav.png)

3.  To create a client ID, select the Add Client ID icon \(![Add Client ID icon.](../image/add-icon.png)\).

4.  In the OAuth client ID, enter a custom client ID.

5.  In the Client Secret field, enter a custom password and then verify the password.![Client ID and secret fields.](../image/sap-commerce-cloud-spoke-create-client-ID.png)

6.  Under BASIC, add the details.

    1.  Under Authorities, add ROLE\_CLIENT.

    2.  Under Client Grant Types, add the details.

        -   client\_credentials
        -   refresh\_token
        -   password
        -   authorization\_code
    3.  Under Scopes, add basic.

7.  On the Create New OAuth Client Details window, do the steps.![OAuth Client Details window.](../image/sap-commerce-cloud-spoke-oauth-screen.png)

    1.  Under ESSENTIAL, enter the custom OAuth client ID and client secret.

    2.  Under BASIC, add ROLE\_CLIENT and under Client Grant Types, add the values.

        -   client\_credentials
        -   refresh\_token
        -   password
        -   authorization\_code
    3.  Under SCOPES, add enter basic.

    4.  Under TOKEN VALIDITY, enter the time for which the token to access the SAP Commerce Cloud is valid.

    5.  Select **DONE**.![Create New OAuth Client Details window.](../image/sap-commerce-cloud-spoke-auth-done.png)

    The credentials to create a SAP Commerce Cloud connection record are created.


## Create connection record for SAP Commerce Cloud spoke

Create a connection record that enables your ServiceNow instance to connect with the SAP Commerce Cloud record. The connection record has the underlying connection information required to integrate with SAP Commerce Cloud.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select **Connections**.

3.  Turn on the Outbound tab.

4.  In the Search all connections field, enter `SAP Commerce Cloud`.

5.  On the SAPCommerceCloud card, select **View Details**.

6.  Select **Configure**.

7.  Fill the form.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name of the connection record. The default and read-only name of the first connection record is SAPCommerceCloud. To provide a custom name to a connection record, you must create a connection record by selecting **Add Connection**.|
    |Connection URL|URL that your ServiceNow instance uses to connect to the SAP Commerce Cloud.|
    |OAuth Client ID|Client ID that you generated on your SAP Backoffice account.|
    |OAuth Client Secret|Client secret that you had generated on your SAP Backoffice account.|
    |OAuth Redirect URL|URL of your ServiceNow instance in the format `https://<instance-name>.service-now.com/oauth_redirect.do`.|
    |OAuth Token URL|URL in the format `https://<instance-name>/authorizationserver/oauth/token`.|

8.  Select **Create and Get OAuth Token.**

    The OAuth token is generated and your ServiceNow is connected to the SAP Commerce Cloud.


## Create a credential record for the SAP Commerce Cloud

Integrate the ServiceNow instance and SAP Commerce Cloud spoke by creating a custom OAuth application in SAP Commerce Cloud to authenticate ServiceNow requests.

### Before you begin

-   Request an Integration Hub subscription.
-   Activate SAP Commerce Cloud.
-   Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays the message **What type of Credentials would you like to create?**.

3.  Select **OAuth 2.0 Credentials**.

4.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the record. For example, SAP Commerce Cloud cred Cred.|
    |Active|Option to actively use the credential record.|
    |OAuth Entity Profile|OAuth profile created during the registration of SAP Commerce Cloud as an OAuth provider. For example, SAP Commerce Cloud default\_profile OAuth Profile.|
    |Applies to|Option to specify if the credential applies to all MID Servers in your network, or to one or more **Specific MID servers**. Specify the MID Servers that should use this credential in the **MID servers** field.|
    |Order|Order to apply this credential. For example, `100`.|
    |Credential alias|Credential alias associated with the spoke.|


## Create a connection record for the SAP Commerce Cloud

Create a connection record for your SAP Commerce Cloud account. The SAP Commerce Cloud connection and credential aliases use these connections to perform actions in SAP Commerce Cloud.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

2.  Open the alias record for SAP Commerce Cloud.

3.  From the **Connections** tab, click **New**.

4.  On the form, fill these fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the record. For example, `SAP Commerce Cloud Connection`.|
    |Credential|Credential record created for SAP Commerce Cloud spoke. For example, `SAP Commerce Cloud Cred`.|
    |Connection alias|Alias record associated with this connection.|
    |Host|IP address of the target host where the SAP Commerce Cloud server is installed.|
    |||
    |Active|Option to actively use the connection record.|
    |Domain|Domain that the action runs in.|
    |Override default port|Target port used by the connection. If blank, the system uses the default port.|

5.  Click **Submit**.


