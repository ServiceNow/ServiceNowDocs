---
title: Request Coaching
description: The Coaching \(com.sn\_coaching\) plugin requires a separate subscription and must be activated by ServiceNow personnel.
locale: en-US
release: xanadu
product: Coaching
classification: coaching
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Coaching, IT Service Management]
---

# Request Coaching

The Coaching \(com.sn\_coaching\) plugin requires a separate subscription and must be activated by ServiceNow personnel.

## Before you begin

Role required: admin

## About this task

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

<table id="table_vgp_3dq_n4b"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Coaching

 \(com.sn\_coaching\)

</td><td>

Activates the Coaching application. This plugin includes demo data and activates related plugins if they are not already active. The Coaching application is available with the ITSM Professional subscription only. Please contact your account manager for more information.

</td></tr><tr><td>

Coaching with Learning \(sn\_coach\_lrn\)

**Note:** This is a ServiceNow Store plugin. You must install this plugin separately from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

</td><td>

Activates the Coaching with Learning application and enables you to integrate the Learning module with the Coaching application.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/xanadu-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[Coaching](../concept/coaching-landing.md)

