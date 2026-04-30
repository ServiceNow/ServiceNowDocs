---
title: Activate Lifecycle Events for Enterprise
description: You can activate the Human Resources Scoped App: Lifecycle Events for Enterprise plugin \[com.sn\_hr\_lifecycle\_ent\] if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
---

# Activate Lifecycle Events for Enterprise

You can activate the Human Resources Scoped App: Lifecycle Events for Enterprise plugin \[com.sn\_hr\_lifecycle\_ent\] if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.

## Before you begin

Role required: admin

## About this task

Human Resources Scoped App: Lifecycle Events for Enterprise enables you to automate onboarding and other employee lifecycle events that span across multiple departments such as IT, Facilities, Finance, and Legal.

It activates these related plugins if they are not already active.

<table id="table_otq_5ld_dbb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Human Resources Scoped App: Core\[com.sn\_hr\_core\]

</td><td>

Provides core HR features.

</td></tr><tr><td>

Employee Service Center\[com.sn\_hr\_service\_portal\]

</td><td>

Provides Employee Center.

</td></tr><tr><td>

Human Resources Scoped App: Lifecycle Events\[com.sn\_hr\_lifecycle\_events\]

</td><td>

Provides lifecycle events.

</td></tr><tr><td>

Document Templates\[com.snc.document\_templates\]

</td><td>

Provides Document templates.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/plugins/task/find-components.html).


