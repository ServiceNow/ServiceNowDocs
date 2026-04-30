---
title: Activate Case and Knowledge Management
description: You can activate Human Resources Scoped App: Core \[com.sn\_hr\_core\] if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Activate Case and Knowledge Management

You can activate Human Resources Scoped App: Core \[com.sn\_hr\_core\] if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.

## Before you begin

Role required: admin

## About this task

Human Resources Scoped App: Core allows you to standardize the documentation, interaction, and fulfillment of employee inquiries and requests.

It activates these related plugins if they are not already active.

<table id="table_b1h_mld_dbb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Human Resources Scoped App: Security\[com.snc.hr.scoped\_security\]

</td><td>

Provides HR security.

</td></tr><tr><td>

Human Resources Scoped App: Integrations\[com.sn\_hr\_integrations\]

</td><td>

Provides HR Integrations.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated Admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/zurich-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[Configuring Case and Knowledge Management](../concept/configuring-ckm.md)

**Related topics**  


[Components installed with Case and Knowledge Management](../reference/components-installed-with-case-and-knowledge-management.md)

