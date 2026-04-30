---
title: Onboard Agile Development 2.0 to DevOps Change Velocity — Service Catalog
description: Create, connect, discover, and configure your Agile Development 2.0 instance using the ServiceNow Service Catalog.
locale: en-US
release: xanadu
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Agile Development 2.0, Integrate, DevOps Change Velocity, IT Service Management]
---

# Onboard Agile Development 2.0 to DevOps Change Velocity — Service Catalog

Create, connect, discover, and configure your Agile Development 2.0 instance using the ServiceNow Service Catalog.

## Before you begin

Role required: sn\_devops.admin or sn\_devops.tool\_owner

Jira cloud version is not supported.

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Maintain Items** and search for DevOps.

    **Note:** You can also access the service catalog from the Employee Center or Service portal.

2.  From the DevOps catalog items, select and activate **DevOps App Onboarding** and **DevOps Tool Onboarding**.

3.  After activating, select **DevOps Tool Onboarding** and select **Try it**.

4.  In the DevOps Tool Onboarding form, enter the tool details:

    |Field|Description|
    |-----|-----------|
    |Tool name|Name for your Agile Development 2.0 integration.|
    |Tool integration|Select Agile Development 2.0.|

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

Enter the connected Agile Development 2.0 tool name.

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


**Parent Topic:**[Agile Development 2.0 integration with DevOps Change Velocity](../concept/agile-integration-dev-ops.md)

