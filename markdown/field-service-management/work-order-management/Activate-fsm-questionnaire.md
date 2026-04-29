---
title: Activate Field Service Questionnaire
description: You can activate the Field Service - Questionnaire plugin \(com.snc.wm\_questionnaire\) for Field Service if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application includes demo data and installs related applications and plugins if they are not already installed.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Survey-based questionnaires, Questionnaires, Work order tasks, Set up work orders and tasks, Configure, Field Service Management]
---

# Activate Field Service Questionnaire

You can activate the Field Service - Questionnaire plugin \(com.snc.wm\_questionnaire\) for Field Service if you have the admin role. The application includes demo data and installs related applications and plugins if they are not already installed.

## Before you begin

Role required: Admin

-   Ensure that the following plugins are activated before you install Field Service com.snc.wm\_questionnaire.
    -   **Required ServiceNow plugins**
        -   **Customer Service \(com.sn\_customerservice\)**
        -   **Customer Service Management Demo Data \(com.snc.customerservice.demo\)**
        -   **Field Service Management**

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Field Service Questionnaire plugin \(com.snc.wm\_questionnaire\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


## Result

The Field Service Questionnaire plugin when activated successfully adds the Questionnaire module to the Field Service menu \(**Field Service** &gt; **Administration** &gt; **Questionnaire**\).

## What to do next

Configure the form layout and add the **Assigned to** field to ensure that a questionnaire does not get created without an assigned agent.

**Related topics**  


[Create a questionnaire for a work order or task](create-questionnaire-for-work-order.md)

