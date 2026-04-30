---
title: Activate Predictive Intelligence for Universal Request
description: You can activate the Predictive Intelligence for Universal Request plugin \(com.snc.universal\_request.ml\) to use machine-learning solutions in the Universal Request application, if you have the admin role.
locale: en-US
release: yokohama
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Universal Request plugins, Setting up and configuring Universal Request, Universal Request, Employee Service Management]
---

# Activate Predictive Intelligence for Universal Request

You can activate the Predictive Intelligence for Universal Request plugin \(com.snc.universal\_request.ml\) to use machine-learning solutions in the Universal Request application, if you have the admin role.

## Before you begin

Role required: admin

**Note:** The Predictive Intelligence for Universal Request plugin \(com.snc.universal\_request.ml\) plugin requires a separate subscription and must be activated by a ServiceNow personnel.

The application includes demo data and installs related applications and plugins if they are not already installed.

-   Predictive Intelligence for Universal Request requires the following plugins. Ensure that these plugins are activated before you install this plugin.
    -   **Required ServiceNow plugins**
        -   **Predictive Intelligence**

            Install this plugin to enable the creation of machine learning solutions using data in your instance. The plugin provides various capabilities and solution types for training the system to predict, recommend, and drive data outcomes. A trained solution can be invoked by any application through the use of a prediction API..

    -   **Universal Request**

        Install this plugin to use the Universal Request application.


Role required: admin.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Predictive Intelligence for Universal Request plugin \(com.snc.universal\_request.ml\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[Universal Request plugins](../concept/ur-plugins.md)

