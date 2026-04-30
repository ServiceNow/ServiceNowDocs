---
title: Activate a plugin on a personal developer instance
description: You can test a plugin on your personal developer instance \(PDI\) before launching it in a production instance.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Activate a plugin, ServiceNow plugins, Basic system configuration, Get started, Administer the ServiceNow AI Platform]
---

# Activate a plugin on a personal developer instance

You can test a plugin on your personal developer instance \(PDI\) before launching it in a production instance.

## Before you begin

Request a PDI on the [ServiceNow® Developer Site](https://developer.servicenow.com/).

## About this task

If a plugin isn't active by default on a PDI, you can activate the plugin without requesting or purchasing it.

To activate a plugin on a PDI, use the All Applications page on your instance. If the plugin isn't available on the All Applications page, activate it from the [ServiceNow® Developer Site](https://developer.servicenow.com/).

**Note:** Some plugins aren't available for activation on PDIs.

## Procedure

1.  Activate the plugin from the All Applications page or the Developer Site.

<table id="table_tbm_1pl_tkb"><thead><tr><th>

Activation method

</th><th>

Procedure

</th></tr></thead><tbody><tr><td>

All Applications page

</td><td>

In your PDI, navigate to **System Applications** &gt; **All Available Applications** &gt; **All**. Find the plugin and then activate it.

 For more information on using the All Applications page, see [Activate a plugin](t_ActivateAPlugin.md).

</td></tr><tr><td>

Developer Site

</td><td>

1.  Sign in to the [ServiceNow® Developer Site](https://developer.servicenow.com/).
2.  On the home page, go to the Instance Management widget and select **Manage** &gt; **Activate plugin**.

The Instance Management widget is titled **Your Instance**. It contains information such as the status, URL, and release version of your PDI.

![Selecting to activate a plugin in the Instance Management widget](../image/activate-plugin-pdi.png)

3.  On the window, locate the plugin to activate.
4.  Next to the plugin listing, select **Activate**.

If available, you can further select to activate the plugin only or include demo data.

![Activating a plugin from the window titled "Your instance actions"](../image/activate-plugin-dev-portal.png)

</td></tr></tbody>
</table>
