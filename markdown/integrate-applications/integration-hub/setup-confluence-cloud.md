---
title: Set up the Confluence Cloud spoke
description: Integrate the ServiceNow instance and Confluence Cloud by creating a custom OAuth 2.0 application in Confluence Cloud to authenticate ServiceNow requests.Add and configure a Confluence Cloud connection to authenticate ServiceNow requests in Confluence Cloud spoke.Specify the groups that have access to Confluence products so that you can manage the users within only these groups using the Confluence Cloud spoke.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Confluence Cloud Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Confluence Cloud spoke

Integrate the ServiceNow instance and Confluence Cloud by creating a custom OAuth 2.0 application in Confluence Cloud to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Confluence Cloud spoke.
-   Atlassian role required: site admin
-   Role required: admin.

## About this task

**Important:**

Starting with the Australia release, instructions for generating and using API tokens have been removed from our documentation to align with Atlassian's Acceptable Use Policy. See the Atlassian blog, [Building Secure and Scalable Integrations: Our Guidance for Third-Party Apps](https://www.atlassian.com/blog/developer/building-secure-and-scalable-integrations-our-guidance-for-third-party-apps) for more information.

## Configure a connection for Confluence Cloud spoke

Add and configure a Confluence Cloud connection to authenticate ServiceNow requests in Confluence Cloud spoke.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, the **Outbound** connections are displayed by default.

4.  Locate the **Confluence Cloud** connection alias and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Confluence Cloud spoke, click **View Details**.
    -   To manage more than one Confluence Cloud spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](../../integrationhub/concept/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

5.  On the **Connection** form, fill in the fields.

<table id="table_confluence_conn_fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name to uniquely identify the connection. For example, `Confluence Cloud Spoke Connection`.

</td></tr><tr><td>

Connection URL

</td><td>

URL of the Atlassian API endpoint: `https://api.atlassian.com/`.

</td></tr><tr><td>

Scopes

</td><td>

By default, these scopes are provided: `ace:confluence, read:page:confluence, search:confluence, read:confluence-groups, write:confluence-groups, read:confluence-user, read:me, read:account, offline_access`. You can modify the scopes as per your requirement. **Note:** After the scopes are modified and saved, whenever you edit the connection record, the scopes are reset to the default scopes.

</td></tr></tbody>
</table>    ![Create a connection for Confluence Cloud spoke using connection template](../image/confluence-cloud-spoke-conn-config.png)

6.  Click **Save and Get OAuth Token**.


## Add Confluence groups

Specify the groups that have access to Confluence products so that you can manage the users within only these groups using the Confluence Cloud spoke.

### Before you begin

ServiceNow role required: admin

Role required: Atlassian site admin

### Procedure

1.  From a web browser, open the [Atlassian Administration portal](https://admin.atlassian.com/).

2.  Log in to your site admin account.

3.  Navigate to **SITE SETTINGS** &gt; **Product access**.

4.  In the Confluence section, view the list of groups that have access to Confluence products.

    Take note of this information for later use.

5.  Return to your ServiceNow instance and navigate to **Confluence Cloud** &gt; **Confluence Groups**.

6.  On the Confluence Groups form, click the **Add Groups** related link.

    The Add Confluence Groups dialog box opens.

7.  In the Available list, select the groups that have access to Confluence products.

    **Tip:** The Available list includes all groups that are associated with your Atlassian account. Select only the groups that have access to Confluence products.

8.  Click the right arrow button to move the groups from the Available list to the Selected list.

9.  Click **OK**.


