---
title: Set up the Ansible spoke
description: Integrate your ServiceNow instance and Ansible Tower to automate Ansible spoke actions. For example, you can create a flow that retrieves a list of credentials from the Ansible Tower environment.Create an OAuth application on the Ansible Tower to have the connection requests from your ServiceNow instance authenticated by the OAuth application.Create the connection record that contains the information that enables your ServiceNow instance to send an authentication request to the Ansible Tower instance and get an OAuth token.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Ansible Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up the Ansible spoke

Integrate your ServiceNow instance and Ansible Tower to automate Ansible spoke actions. For example, you can create a flow that retrieves a list of credentials from the Ansible Tower environment.

## Before you begin

-   Request an Integration Hub subscription
-   Activate the Ansible spoke
-   Role required: admin

## Create an OAuth application in the Ansible Tower

Create an OAuth application on the Ansible Tower to have the connection requests from your ServiceNow instance authenticated by the OAuth application.

### Before you begin

Role required: admin

Ensure that you have the administrator's access to the Ansible Tower instance.

### Procedure

1.  Log in to the Ansible Tower application instance.

2.  On the left panel, under Administration, select Applications.

    ![Applications link on Ansible Automation Platform.](../image/ansible-spoke-application-link.png)

3.  On the Applications page, select **Add**.

    ![Add button for adding an application.](../image/ansible-spoke-add-application-button.png)

4.  Fill the form.

    |Field|Description|
    |-----|-----------|
    |Name|Unique name of the OAuth application.|
    |Description|Description of the application. This field is optional.|
    |Organization|Organization the OAuth application is associated with.|
    |Authorization grant type|The basis of the OAuth application granting access to the client. The basis could be an authorization code given to the client or a resource-owner password.|
    |Redirect URIs|Redirect the URI to the client after access is granted. Enter the redirect URI in the format `https://<instance name>.service.now.com/api/sn_ansible_spoke/ansible_oauth_redirect`.|
    |Client type|Type of client that requests authentication from the OAuth application.|

5.  Select **Save**.

6.  Copy the Client ID and Client Secret and store them at a secure place.

    ![](../image/ansible-spoke-client-id-secret.png)

    You've created the OAuth application.

    ![OAuth application created.](../image/ansible-spoke-oauth-app-created.png)


## Set up the Ansible spoke connection record

Create the connection record that contains the information that enables your ServiceNow instance to send an authentication request to the Ansible Tower instance and get an OAuth token.

### Before you begin

Role required: admin

Ensure you have set up an OAuth application on the Ansible Tower instance.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select Connections.

3.  Turn on the Outbound tab.

4.  In the Search all connections field, enter `AnsibleTowerAlias`.

5.  On the AnsibleTowerAlias card, select **View Details**.

6.  Select **Configure**.

7.  Fill the form.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name of the connection established with the Ansible Tower instance. The first connection's default name is automatically assigned to match the name specified in the Connections and Credentials form on the Connection &amp; Credential Aliases page. To provide your custom name, create a connection record by selecting **Add Connection**.|
    |Connection URL|The URL your ServiceNow instance uses to connect to the Ansible Tower instance.|
    |Credential Name|Name of the credential record that you created for Ansible on your ServiceNow instance.|
    |Application Registry Name|Name of the application registry record that you created for Ansible on your ServiceNow instance.|
    |OAuth Client ID|The client ID that you had generated while you set up the OAuth application.|
    |OAuth Client Secret|The client secret that you had generated while you set up the OAuth application.|
    |Oauth Entity Profile Name|Name of the OAuth application that you created on the Ansible Tower instance.|
    |Authorization URL|The URL that the client uses to request access to the Ansible Tower instance. The URL format is `https://<ansible-tower-instancename>.com/api/o/authorize`.|
    |Token URL|The URL that the client uses to request a token to access the Ansible Tower instance. The URL format is `https://<ansible-tower-instance-name>.com/api/o/token`.|
    |OAuth Redirect URL|The redirect URL that the OAuth application uses to redirect to your ServiceNow instance. The URL must be in the format `https://<your instance name>.service-now.com/api/sn_ansible_spoke/ansible_oauth_redirect`.|

8.  Select **Configure and Get OAuth Token**.

    The OAuth application authenticates the connection request and provides a temporary token to access the Ansible Tower instance.


