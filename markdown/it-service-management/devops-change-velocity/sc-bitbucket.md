---
title: Onboard Bitbucket to DevOps Change Velocity — Service Catalog
description: Create, connect, discover, and configure your Bitbucket instance using the ServiceNow Service Catalog.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Bitbucket, Integrate, DevOps Change Velocity, IT Service Management]
---

# Onboard Bitbucket to DevOps Change Velocity — Service Catalog

Create, connect, discover, and configure your Bitbucket instance using the ServiceNow Service Catalog.

## Before you begin

Role required: sn\_devops.admin or sn\_devops.tool\_owner

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Maintain Items** and search for DevOps.

    **Note:** You can also access the service catalog from Employee Center or Service portal.

2.  From the DevOps catalog items, select and activate **DevOps App Onboarding** and **DevOps Tool Onboarding**.

3.  After activating, select **DevOps Tool Onboarding** and select **Try it**.

4.  In the DevOps Tool Onboarding form, enter the tool details:

<table id="table_ubw_p1p_gwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Tool name

</td><td>

Name for your Bitbucket integration.

</td></tr><tr><td>

Tool integration

</td><td>

Select Bitbucket.

</td></tr><tr><td>

Tool URL

</td><td>

URL of your Bitbucket instance.

</td></tr><tr><td>

Credential type

</td><td>

Select the credential type as one of the following:-   Basic Auth
-   Access Token
-   OAuth 2.0 - Authorization Code
-   Oauth 2.0 - Client Credentials
 For more information, see [Bitbucket integration with DevOps Change Velocity](../concept/bitbucket-integration-dev-ops.md).

</td></tr><tr><td>

Use MidServer

</td><td>

Optional. Select  MID Server for an on-premises tool that is attached to a  MID Server. Application is automatically set to  DevOps and capability is set to REST.

</td></tr></tbody>
</table>    For a list of all the permissions required on the credentials for connecting to Bitbucket, see Bitbucket permissions in [Permissions required for DevOps tools](../reference/tool-req-permission.md).

5.  Select **Order Now**.

    A request is created. When the request is approved, the tool is created, connected, and discovered.

6.  From the DevOps catalog items, select **DevOps App Onboarding**.

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

Enter the connected Bitbucket tool name.

</td></tr><tr><td>

Repositories

</td><td>

Select the repositories for which you want to configure webhooks and import historical data.

</td></tr><tr><td>

Import from and Import to

</td><td>

Select the dates for which you want to import the data. By default, the last 30 days are selected. You can choose to import data for a maximum of 90 days.

</td></tr><tr><td>

Do you wish to configure webhook for the tool?

</td><td>

Select the check box if you want to configure webhooks for the selected repositories.

</td></tr><tr><td>

Onboarding plans

</td><td>

Leave empty.

</td></tr></tbody>
</table>8.  Select **Order Now**.

    A request is created. When the request is approved, the repository objects are associated to the app record and webhooks are configured for real-time tracking. Historical data is imported for the selected repositories. The **Track** field is automatically enabled for imported repositories.


**Parent Topic:**[Bitbucket integration with DevOps Change Velocity](../concept/bitbucket-integration-dev-ops.md)

