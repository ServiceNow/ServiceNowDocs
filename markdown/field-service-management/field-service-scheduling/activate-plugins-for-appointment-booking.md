---
title: Activate Appointment Booking
description: Activate the Appointment Booking feature by installing the required plugins.
locale: en-US
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Appointment Booking, Configuring Appointment Booking, Additional scheduling configuration options, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Activate Appointment Booking

Activate the Appointment Booking feature by installing the required plugins.

## Before you begin

Role required: admin

## About this task

The Appointment Booking plugin \(com.snc.appointment\_booking\) is activated automatically when you activate the Field Service Management plugin.

Ensure that the following plugins are activated:

-   **Field Service Management**: Enables core Field Service Management capabilities. Activating this plugin automatically activates the Appointment Booking plugin.
-   **Appointment Booking plugin**: Provides the capability to book and manage appointments for services.
-   **Customer Service with Field Service Management Plugin**: Integrates Field Service Management with Customer Service Management to streamline appointment-related workflows.
-   **Dynamic Scheduling** \(Optional but recommended\): Enables dynamic scheduling capabilities, bulk task recommendations, and interval-based auto-assignment. It also allows the use of the scripted availability method for advanced scheduling in Appointment Booking configurations.
-   **Appointment Booking Demo data**: Installs demo data to help you set up and explore the Appointment Booking feature.

For more information on the components installed with Appointment Booking see, [Appointment booking components](../reference/appointment-booking-components.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugins \(com.snc.appointment\_booking\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


