---
title: Set up the Ansible spoke
description: Integrate your ServiceNow instance and Ansible Tower to automate Ansible spoke actions. For example, you can create a flow that retrieves a list of credentials from the Ansible Tower environment.Create an OAuth application on the Ansible Tower to have the connection requests from your ServiceNow instance authenticated by the OAuth application.Create the connection record that contains the information that enables your ServiceNow instance to send an authentication request to the Ansible Tower instance and get an OAuth token.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/setup-ansible.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-08-03"
reading_time_minutes: 3
breadcrumb: [Ansible Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Ansible spoke

Integrate your ServiceNow instance and Ansible Tower to automate Ansible spoke actions. For example, you can create a flow that retrieves a list of credentials from the Ansible Tower environment.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Ansible spoke.
-   Role required: admin.

**Note:** Ansible spoke supports MID Server from v2.4.0 onwards. If you are using a previous version of the spoke and want to use MID Server, upgrade to the latest version of Ansible spoke and delete the existing connection and credential record.

To delete the existing connection and credential record:

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.
2.  Search and open the default connection and credential record for the Ansible spoke. For example, **AnsibleTowerAlias**.
3.  Under the **Connections** tab, open the default HTTP\(s\) Connection record. For example, **Ansible Spoke Connection**.
4.  Click **Delete**. System prompts you confirm delete action.
5.  Click **Delete**.
6.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.
7.  Search and open the default credential record for the Ansible spoke. For example, **Ansible credential**.
8.  Click **Delete**. System prompts you confirm delete action.
9.  Click **Delete**.

## Create an OAuth application in the Ansible Tower

Create an OAuth application on the Ansible Tower to have the connection requests from your ServiceNow instance authenticated by the OAuth application.

### Before you begin

Role required: admin

Ensure that you have the administrator's access to the Ansible Tower instance.

### Procedure

1.  Log in to the Ansible Tower application instance.

2.  On the left panel, under Administration, select Applications.

    \[Omitted image "ansible-spoke-application-link.png"\] Alt text: Applications link on Ansible Automation Platform.

3.  On the Applications page, select **Add**.

    \[Omitted image "ansible-spoke-add-application-button.png"\] Alt text: Add button for adding an application.

4.  Fill the form.

    |Field|Description|
    |-----|-----------|
    |Name|Unique name of the OAuth application.|
    |Description|Description of the application. This field is optional.|
    |Organization|Organization the OAuth application is associated with.|
    |Authorization grant type|The basis of the OAuth application granting access to the client. The basis could be an authorization code given to the client or a resource-owner password.|
    |Redirect URIs|Redirect the URI to the client after access is granted. Enter the redirect URI in the format `https://<ServiceNow-Instance-Name>.service-now.com/oauth_redirect.do`.|
    |Client type|Type of client that requests authentication from the OAuth application.|

5.  Select **Save**.

6.  Copy the Client ID and Client Secret and store them at a secure place.

    \[Omitted image "ansible-spoke-client-id-secret.png"\]

    You've created the OAuth application.

    \[Omitted image "ansible-spoke-oauth-app-created.png"\] Alt text: OAuth application created.


## Set up the Ansible spoke connection record

Create the connection record that contains the information that enables your ServiceNow instance to send an authentication request to the Ansible Tower instance and get an OAuth token.

### Before you begin

Role required: admin

Ensure you have set up an OAuth application on the Ansible Tower instance.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, toggle and enable the **Outbound** connections.

4.  Locate the alias for **AnsibleTowerAlias** and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Ansible spoke, click **View Details**.

        \[Omitted image "ansible-conf-temp.png"\] Alt text:

    -   To manage more than one Ansible spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

    \[Omitted image "ansible-configure.png"\] Alt text:

5.  On the form, fill in these fields:

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name of the connection established with the Ansible Tower instance.|
    |Connection URL|The URL your ServiceNow instance uses to connect to the Ansible Tower instance.|
    |Credential Name|Name to identify the credential record.|
    |Application Registry Name|Name to identify the application registry record.|
    |OAuth Client ID|The client ID that you had generated while you set up the OAuth application.|
    |OAuth Client Secret|The client secret that you had generated while you set up the OAuth application.|
    |Oauth Entity Profile Name|Name to identify the OAuth application.|
    |Authorization URL|The URL that the client uses to request access to the Ansible Tower instance. The URL format is `https://<ansible-tower-instancename>.com/api/o/authorize`.|
    |Token URL|The URL that the client uses to request a token to access the Ansible Tower instance. The URL format is `https://<ansible-tower-instance-name>.com/api/o/token`.|
    |OAuth Redirect URL|The redirect URL that the OAuth application uses to redirect to your ServiceNow instance. The URL must be in the format `https://<ServiceNow-Instance-Name>.service-now.com/oauth_redirect.do`.|

    \[Omitted image "ansible-conf-temp-form.png"\] Alt text:

6.  Click **Save and Get OAuth Token**.

    The OAuth application authenticates the connection request and provides a temporary token to access the Ansible Tower instance.


