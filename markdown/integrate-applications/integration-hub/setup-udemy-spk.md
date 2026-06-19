---
title: Set up the Udemy spoke
description: Create an Udemy API key and configure a Udemy spoke connection to enable your ServiceNow instance to authenticate with Udemy and access data.Create a Udemy API key to authenticate ServiceNow requestsCreate a Udemy spoke connection to connect to the Udemy instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/setup-udemy-spk.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Udemy Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Udemy spoke

Create an Udemy API key and configure a Udemy spoke connection to enable your ServiceNow instance to authenticate with Udemy and access data.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Udemy spoke plugin.
-   Ensure that you have the admin access to the Udemy instance.
-   Role required: admin.

## Create a Udemy API key

Create a Udemy API key to authenticate ServiceNow® requests

### Before you begin

Role required: admin

### Procedure

1.  Log in to your Udemy instance.

2.  Navigate to **Manage** &gt; **Settings**.\[Omitted image "udemy-spoke-config-log-in.png"\] Alt text: Navigation to API key.

3.  Under Settings, select LMX/LXP integrations.\[Omitted image "udemy-spoke-lms.png"\] Alt text: LMS/LXP integration link.

4.  Select **Copy** to copy the client ID.

5.  Select **Copy** to copy the client secret.\[Omitted image "udemy-spoke-client-id-secret.png"\] Alt text: Client ID and Client secret.

6.  Go to [GET /api-2.0/organizations/\{organization\_id\}/courses/list/](https://servicenow-integration.udemy.com/developers/organization/courses/methods/organizationcourseslist-list/get/).

7.  In the Your Client Id field, paste the client ID you had copied.

8.  In the Your Client Secret field, paste the client secret you had copied.\[Omitted image "udemy-api-key.png"\] Alt text: Generate the API key.


### Result

The API key is generated and displayed in the **Authorization** field. Copy this value to use when configuring the Udemy spoke connection.

## Create a connection for the Udemy spoke

Create a Udemy spoke connection to connect to the Udemy instance.

### Before you begin

-   Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Select the **Integrations** tab.

3.  Under **Connections**, toggle and enable the **Outbound** connections.

4.  Locate the alias for **Udemy** and select **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Udemy spoke, select **View Details**.

        \[Omitted image "udemy-spoke-tile.png"\] Alt text: Connection for the Udemy spoke

    -   To manage more than one Udemy spoke connection records, you should create child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/support-multiple-connections.md).
    If you're configuring the spoke for the first time, select **Configure**. Otherwise, select **Edit**.

    \[Omitted image "udemy-spoke-configure.png"\] Alt text: Initial connection configuration

5.  On the form, fill in these fields:

<table id="table_whp_kcp_x3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name of the connection record.**Note:** The default and the read-only name of the connection is Udemy for the first record that you create. However, you can provide custom connection names for all connection records you create after the first record.

</td></tr><tr><td>

Connection URL

</td><td>

The URL used to connect to the Udemy server or instance. The format is `https://<provider-domain-name>.com`.

</td></tr><tr><td>

Domain Name

</td><td>

The domain name of your Udemy instance.

</td></tr><tr><td>

Domain ID

</td><td>

The domain ID of your Udemy instance.**Note:** To get the domain ID, do the following steps:

1.  Log in to the Udemy instance.
2.  Go to **Manage&gt;Settings**.
3.  On the left panel, under Settings, select API.
4.  Under the API heading, select the API documentation link for the Courses API section.

The API Client and Account Id are available under the Your API Client and Your Account Id section.

</td></tr><tr><td>

API Version

</td><td>

The version of the API that you use to connect to the Udemy instance or server. The default version is api-2.0.

</td></tr><tr><td>

API Key

</td><td>

The API key that you had generated.

</td></tr><tr><td>

Credential Name

</td><td>

Custom name of the connection and credential record.

</td></tr></tbody>
</table>    \[Omitted image "udemy-spoke-connection-config.png"\] Alt text: Configure a connection for the Udemy spoke.

6.  Select **Save**.


### Result

The Udemy spoke is set up and your Udemy is integrated with the ServiceNow instance.

