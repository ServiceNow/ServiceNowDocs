---
title: Create a custom translation management system
description: Configure Localization Framework with a third-party translation management system of your choice to localize an artifact.
locale: en-US
release: zurich
product: Localization Framework
classification: localization-framework
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Translation Management System configurations, Localization Framework settings, Configure the Localization Framework, Localization Framework, Translation and localization, Configure core features, Administer]
---

# Create a custom translation management system

Configure Localization Framework with a third-party translation management system of your choice to localize an artifact.

## Before you begin

Roles required: localization\_admin and flow\_designer

Ensure that the Localization Framework Installer plugin \(com.glide.localization\_framework.installer\) is activated.

## Procedure

1.  Navigate to **All** &gt; **Localization Framework** &gt; **TMS Configuration**.

    **Note:** By default, RWS, and XTM translation management system configurations are available.

2.  Click **New**.

3.  In the TMS Configuration form, fill in the fields.

<table id="table_shk_rfz_snb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Identifier of the TMS configuration.

</td></tr><tr><td>

Request translation subflow

</td><td>

IntegrationHub subflow that interacts with the third-party translation management system to request translations.

</td></tr><tr><td>

Retrieve translation subflow

</td><td>

IntegrationHub subflow that interacts with the third-party translation management system to retrieve translated content.

</td></tr><tr><td>

Application

</td><td>

The scope of the application. The default value is Global.

</td></tr><tr><td>

Version

</td><td>

Version of the contract used in subflows. The default value is **v1.**

</td></tr><tr><td>

Enable auto retrieval

</td><td>

Option to retrieve the translated content automatically.When selected, the translations are retrieved as per the scheduled jobs which run daily.

</td></tr></tbody>
</table>4.  Click **Submit**.


**Parent Topic:**[Translation Management System configurations](../concept/tms-configuration.md)

