---
title: Set up the Udemy spoke
description: Enable your ServiceNow instance to connect to the Udemy instance by setting up a connection and credential record for the Udemy spoke. The Udemy instance uses the record to authenticate the requests from the ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Udemy Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Udemy spoke

Enable your ServiceNow instance to connect to the Udemy instance by setting up a connection and credential record for the Udemy spoke. The Udemy instance uses the record to authenticate the requests from the ServiceNow instance.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Udemy spoke plugin.
-   Ensure that you have the admin access to the Udemy instance.
-   Role required: admin.

## Procedure

1.  Generate an Application Programming Interface \(API\) key from your Udemy instance.

    1.  Log in to your Udemy instance.

    2.  Navigate to **Manage** &gt; **Settings**.![Navigation to API key.](../image/udemy-spoke-config-log-in.png)

    3.  Under Settings, select LMX/LXP integrations.![LMS/LXP integration link.](../image/udemy-spoke-lms.png)

    4.  Click **Copy** to copy the client ID.

    5.  Click **Copy** to copy the client secret.![Client ID and Client secret.](../image/udemy-spoke-client-id-secret.png)

    6.  Go to [GET /api-2.0/organizations/\{organization\_id\}/courses/list/](https://servicenow-integration.udemy.com/developers/organization/courses/methods/organizationcourseslist-list/get/).

    7.  In the Your Client Id field, paste the client ID you had copied.

    8.  In the Your Client Secret field, paste the client secret you had copied.![Generate the API key.](../image/udemy-api-key.png)

        The API key is generated and displayed in the **Authorization** field. Copy and record the value for later use.

2.  Create a connection and credential record to connect to the Udemy instance.

    1.  Log in to your ServiceNow instance.

    2.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

    3.  Select Connections.

    4.  In the Search all connections field, enter `Udemy`.![Enter Udemy in the search field.](../image/udemy-spokes-search-udemy-conn.png)

    5.  In the Udemy connection card, select **View Details**.

    6.  Click **Configure**.![Configure button for connection and credentials.](../image/udemy-spoke-click-configure.png)

    7.  Fill the form with the details.

<table id="table_ufq_kjv_ywb"><thead><tr><th>

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
</table>    8.  Click **Configure Connection**.

        The connection and credential record is created.


