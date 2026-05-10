---
title: Onboard Jira to DevOps Change Velocity — Service Catalog
description: Create, connect, discover, and configure your Jira Server or Jira Cloud instance using the ServiceNow Service Catalog.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Jira, Integrate, DevOps Change Velocity, IT Service Management]
---

# Onboard Jira to DevOps Change Velocity — Service Catalog

Create, connect, discover, and configure your Jira Server or Jira Cloud instance using the ServiceNow Service Catalog.

## Before you begin

Role required: sn\_devops.admin or sn\_devops.tool\_owner

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Maintain Items** and search for DevOps.

    **Note:** You can also access the service catalog from the Employee Center or Service portal.

2.  From the DevOps catalog items, select and activate **DevOps App Onboarding** and **DevOps Tool Onboarding**.

3.  After activating, select **DevOps Tool Onboarding** and select **Try it**.

4.  In the DevOps Tool Onboarding form, enter the tool details:

<table id="table_bsr_hkv_kbc"><tbody><tr><td>

Jira Server

</td><td>

1.  In the **Tool name** field, enter a name for the tool.
2.  In the **Tool integration** field, search for and select Jira.
3.  Enter your Jira server instance URL.
4.  From the **Credential type** list, select the authentication type you want to use to connect with your Jira server.
    -   **Basic Auth**

        1.  Enter your Jira server username.

**Note:** The Jira user that you use here must have the Jira Administrators permissions.

        2.  Enter the password or access token to access this instance.
    -   **API Key**

Enter the API token to access the instance.

5.  If you want to configure webhooks for all the projects discovered in your Jira instance, then select the option **Do you wish to configure webhook for the tool?**
6.  Select  **Use MidServer** for an on-premises tool that is attached to a  MID Server. Application is automatically set to  DevOps and capability is set to REST.


</td></tr><tr><td>

Jira Cloud

</td><td>

1.  In the **Tool name** field, enter a name for the tool.
2.  In the **Tool integration** field, search for and select Jira Cloud.
3.  in the **Tool URL** field, enter your Jira Cloud instance URL.
4.  In the **Credential type** field, select **Basic Auth** or **OAuth 2.0**.

**Basic Auth**

    1.  Enter your Jira Cloud username.

**Note:** The Jira user that you use here must have the Jira Administrators permissions.

    2.  Enter the password or access token to access this instance.
**OAuth 2.0**

Pre-requisites:

    -   
    -   [Obtain the value of Cloud ID](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/setup-jira-serv-mgmt.md)
    -   
    -   Create credential record for Jira Cloud
In the **Tool credential** field, select an existing OAuth 2.0 tool credential record.

**Note:** Only records that are not in use and configured for Jira Cloud can be selected as an existing credential record.

5.  If you want to configure webhooks for all the projects discovered in your Jira instance, then select the option **Do you wish to configure webhook for the tool?**

**Note:** If you have connected your Jira tool using OAuth 2.0 based authentication, the webhooks are created for the OAuth 2.0 integration app in Jira when you configure automatically, whereas if you have connected using basic authentication, the webhooks are created for all your projects in Jira.

6.  Select  **Use MidServer** for an on-premises tool that is attached to a  MID Server. Application is automatically set to  DevOps and capability is set to REST.


</td></tr></tbody>
</table>    For a list of all the permissions required on the credentials for connecting to Jira, see Jira permissions in [Permissions required for DevOps tools](../reference/tool-req-permission.md).

5.  Select **Order Now**.

    A request is created. When the request is approved, the tool is created, connected, configured, and discovered.

6.  From the DevOps catalog items, select **DevOps App Onboarding** and select **Try it**.

7.  In the DevOps App Onboarding form, enter the details:

<table id="table_vb5_s3p_gwb"><tbody><tr><td>

Are you creating a new app or adding to an existing one?

</td><td>

Select from the options whether to create a new app or use an existing app.

</td></tr><tr><td>

App

</td><td>

Enter the name for the app that you're creating or using.

</td></tr><tr><td>

Onboarding pipelines

</td><td>

Leave empty.

</td></tr><tr><td>

Onboarding repositories

</td><td>

Leave empty.

</td></tr><tr><td>

Onboarding plans

</td><td>

Enter the connected Jira tool name.

</td></tr><tr><td>

Plans

</td><td>

Select the plans for which you want to import historical data.

</td></tr><tr><td>

Import from and Import to

</td><td>

Select the dates for which you want to import the data. By default, the last 30 days are selected. You can choose to import data for a maximum of 90 days.

</td></tr></tbody>
</table>8.  Select **Order Now**.

    A request is created. When the request is approved, the plan objects are associated to the app record, which enables real-time tracking. Historical data is also imported for the selected plans. The **Track** field is automatically enabled for imported plans.


**Parent Topic:**[Jira integration with DevOps Change Velocity](../concept/jira-integration-dev-ops.md)

