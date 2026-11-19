---
title: Onboard Rally to DevOps Change Velocity — Service Catalog
description: Create, connect, discover, and configure your Rally instance using the ServiceNow Service Catalog.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/devops-change-velocity/sc-rally.html
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Rally, Integrate, DevOps Change Velocity, IT Service Management]
---

# Onboard Rally to DevOps Change Velocity — Service Catalog

Create, connect, discover, and configure your Rally instance using the ServiceNow Service Catalog.

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

Name for your Rally integration.

</td></tr><tr><td>

Tool integration

</td><td>

Select Rally.

</td></tr><tr><td>

Tool URL

</td><td>

URL of your Rally instance to integrate.

</td></tr><tr><td>

Credential type

</td><td>

Select Basic Auth or OAuth 2.0, depending on the credentials you're using.-   For Basic Auth, enter the password or access token.
-   For OAuth 2.0, enter the credentials. For information on setting up your OAuth 2.0 credentials for Rally, see [Setting up Rally OAuth 2.0 credentials for DevOps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/devops-change-velocity/setting-up-rally-oauth-2-0-credentials-for-devops.md).


</td></tr><tr><td>

Use MidServer

</td><td>

Optional. Select MID Server for an on-premises tool that is attached to a MID Server. Application is automatically set to  DevOps  and capability is set to REST.

</td></tr></tbody>
</table>5.  Select **Order Now**.

    A request is created. When the request is approved, the tool is created, connected, discovered, and configured.

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

Enter the connected Rally tool name.

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


**Parent Topic:**[Rally integration with DevOps Change Velocity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/devops-change-velocity/rally-devops-integration.md)

