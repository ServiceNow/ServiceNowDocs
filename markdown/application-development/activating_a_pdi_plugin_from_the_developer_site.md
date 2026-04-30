---
title: Activating a PDI plugin from the developer site
description: Activate your PDI plugin from the Developer Site to start working on an instance.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Personal developer instance guide, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Activating a PDI plugin from the developer site

Activate your PDI plugin from the Developer Site to start working on an instance.

## Before you begin

Role required: none

## About this task

Some plugins require activation by ServiceNow® personnel on company and partner instances. You cannot activate these plugins from the plugins list. You may be able to activate these plugins from the **My Instance** section of the **Account** menu.

**Note:** Many ServiceNow® Store applications cannot be installed to PDIs.

## Procedure

1.  Open the **Account** menu to access the **My Instance** section.

2.  Click the **Activate plugin** instance action.

3.  In the **Your instance actions** dialog, find the plugin and click the **Activate** button.

4.  If your plugin has demo data:

    1.  Select the **Activate plugin** menu item to activate the plugin without demo data.

    2.  Select the **Activate plugin with demo data** menu item to activate the plugin with demo data.

        ![Select to activate with demo data](../image/activate-plugin-pdi3.png)

    You cannot perform other instance actions while the plugin is activating. The **Instance Status** is **Fulfilling Request** while the plugin is activated.

    ![In-process fulfilling a request](../image/fulfilling-request-pdi.png)


## Result

You will receive an email from the Developer Site when the plugin activation is complete. Plugins that require activation by ServiceNow® personnel do not appear in the plugins list in your PDI. The **Available Plugins** dialog does not show plugin activation status.

To use the plugin, reload the browser window where you logged in to your PDI.

**Parent Topic:**[Personal developer instance guide](../concept/personal_developer_instance_guide.md)

