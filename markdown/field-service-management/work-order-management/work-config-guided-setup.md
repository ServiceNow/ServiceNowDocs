---
title: Set up work configurations
description: Use the Field Service Management application to handle different types of field service work. A work configuration identifies the configurations and the data required for specific field service work.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Work Configurations, Set up work orders and tasks, Configure, Field Service Management]
---

# Set up work configurations

Use the Field Service Management application to handle different types of field service work. A work configuration identifies the configurations and the data required for specific field service work.

## Before you begin

Role required: admin

## About this task

You can create a table to extend the work order task table for each work configuration. You can then configure a number of items, such as business rules and client scripts, that drive work order tasks of the work configuration from creation to resolution. When creating a work order, initiators or qualifiers can select the work configuration that corresponds to the field work either directly or through a template.

## Procedure

1.  On the Getting Started page of the guided setup, click **Get Started**.

2.  In the Work order task types category, view the list of tasks to configure the feature.

<table id="table_pz1_qqv_llb"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create Work Order Task Types

</td><td>

You can optionally create a new Work Order Task Type table that extends the Work Order Task \(wm\_task\) table.**Note:** Make sure the Work Order Task table is extensible before proceeding. Enable the Audit flag for the new Work Order Task Type table created to capture audit history.

 You can create a table for the Work Order Task Type using the Platform table creation feature \(navigate to **System Definition** &gt; **Table**\).

**Note:** Ensure that Application access is set to ‘All applications scopes’ to allow all field service features to access the new table.

</td></tr><tr><td>

Set Up View Rules

</td><td>

View rules determine the form views that are available to users. Create view rules that determine the conditions for when the system displays the Work Order Task Type table in a specified view.

</td></tr><tr><td>

Set Up UI Policies

</td><td>

UI policies dynamically change the behavior of information on a form, such as setting a field to read-only or making a field mandatory. Configure the desired UI policies for the Work Order Task form.

</td></tr><tr><td>

Set Up Client Scripts

</td><td>

Client scripts allow the system to run JavaScript on the client when client-based events occur, such as when a form loads or when a field changes value. Configure the desired client scripts for the Work Order Task Type table.

</td></tr><tr><td>

Set Up Business Rules

</td><td>

A business rule is a server-side script that runs when a record is displayed, inserted, updated, or deleted, or when a table is queried. Use business rules to accomplish tasks like automatically changing values in form fields when certain conditions are met, or to create events for email notifications and script actions. Set up the desired business rules for the Work Order Task Type table.

</td></tr><tr><td>

Set Up UI Actions

</td><td>

UI actions include the buttons, links, and context menu items that appear on forms and lists. Because a Work Order Task Type is an extension of Work Order Task, the Work Order Task Type inherits the Work Order UI actions.

</td></tr><tr><td>

Set Up Roles

</td><td>

Create one or more roles to control access to the Work Order Task Type features and capabilities. Then grant these roles access to the desired applications and modules.

</td></tr><tr><td>

Set Up ACLs

</td><td>

Use Access Control List rules \(ACLs\) to restrict access to data.

</td></tr><tr><td>

Set Up Work Categories

</td><td>

Create a category for different work types that would share similar field service configuration.

</td></tr><tr><td>

Set Up Work Types

</td><td>

Create a work type for same repeated tasks your business performs. For example, a heater installation company can create work types names Install Heater, Repair Heater, and Replace Heater.

</td></tr><tr><td>

Set up Field Service Management Configuration \(SM Config\)

</td><td>

Optionally, create a new Field Service Management Configuration \(SM Config\) if needed for a work configuration. Configure several different settings to determine how daily operations, including business processes, task assignment methods, notifications, and other task activities are handled in the work configuration.

</td></tr><tr><td>

Set Up Work Configuration

</td><td>

Enables the customer to setup different work configurations for field service workflows as needed by a business unit or department.

 Each Work configuration enables the business or department to setup the required data fields by mapping to the Work Order Task type table. Also Work configuration can be setup with the correct Service Management Application Configuration \(SM Config\).

 Optionally, the work configuration would be mapped to the correct work category so that the only the work types relevant to a given work configuration are available to selection on work order task.

</td></tr></tbody>
</table>3.  To perform a task, click **Configure**.

    This button opens the page in your instance where the configuration is completed.


