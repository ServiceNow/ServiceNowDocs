---
title: Activate La Jolla theme branding
description: Activate the Service Portal La Jolla Brand to apply ServiceNow branding, which includes WCAG-AA compliance for contrast. This plugin is active by default on new instances, but admins must activate the plugin on instances upgraded from earlier versions.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Defining portal styles, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Activate La Jolla theme branding

Activate the Service Portal La Jolla Brand to apply ServiceNow branding, which includes WCAG-AA compliance for contrast. This plugin is active by default on new instances, but admins must activate the plugin on instances upgraded from earlier versions.

## Before you begin

Role required: admin

## About this task

The **Service Portal La Jolla Brand Update** activates these related plugins if they are not already active.

<table id="table_lrj_rty_vfb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service Portal La Jolla Brand\[com.glide.service-portal.themes.la-jolla\]

</td><td>

This plugin updates your /sp and /sp\_config portals with the ServiceNow La Jolla branding. If the portal record has not been modified, the logo, favicon, login page background image, hero banner, theme, and widget instance options are updated.

</td></tr></tbody>
</table>**Note:** If you have modified the **/sp** or **sp\_config** portal pages before installing the plugin, you may not see all elements of the La Jolla branding. All branding images are located in the **db\_image** table for manual updates to your custom portals.

To purchase a subscription, contact your ServiceNow account manager. After purchasing the subscription, activate the plugin within the production instance.

You can evaluate the feature on a sub-production instance without charge by requesting it from the HI Customer Service System.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[Defining portal styles](../concept/portal-css.md)

**Related topics**  


[bundle-platadm.list-of-plugins]

