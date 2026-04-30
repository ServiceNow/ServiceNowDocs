---
title: Activate Field Service Management
description: The Field Service Management \(com.snc.work\_management\) is available as a separate subscription. This plugin activates related plugins, if they are not already active. After Field Service Management is activated, you can also activate additional plugins that provide demo data and enable a variety of features.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Configure, Field Service Management]
---

# Activate Field Service Management

The Field Service Management \(com.snc.work\_management\) is available as a separate subscription. This plugin activates related plugins, if they are not already active. After Field Service Management is activated, you can also activate additional plugins that provide demo data and enable a variety of features.

## Before you begin

Role required: admin

## About this task

The Field Service Management activates the following plugins, if they are not already active.

<table id="table_qgs_xqm_jt"><thead><tr><th>

Plugin name

</th><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Automatic Assignment

</td><td>

com.snc.automatic\_assignment

</td><td>

Automatically assigns tasks to agents based on specified criteria.

</td></tr><tr><td>

Field Service Mobile

</td><td>

com.sn\_fsm\_mobile

</td><td>

Manages the Field Service mobile components on an iOS or an Android mobile device. Field service agents and dispatchers can execute work order tasks, manage assets, and close work order tasks on their mobile device in online or offline mode.For more information, see [Setting up Field Service Mobile Agent](../../field-service-management/concept/setting-up-field-service-mobile-agent.md).

</td></tr><tr><td>

FSM Agent Workspace \(Deprecated\)

</td><td>

com.snc.agent\_workspace.fsmThe deprecated plugin is replaced by com.snc.uib.fsm\_agent\_workspace.

</td><td>

Enables users to manage work orders and tasks within the agent workspace. The plugin has been deprecated in Vancouver release.For more information, see [Activate Dispatcher Workspace](../../field-service-management/task/activate-dispatcher_workspace.md).

</td></tr><tr><td>

Field Service Management Demo Data

</td><td>

com.snc.work\_management.demo

</td><td>

Adds demonstration data for the Field Service Management application covering the medical and telecommunication domains. **Note:** Installing this plugin adds new Configuration Item tables and relationships to the database.

For more information, see [Quick start tests for Field Service Management](../../../administer/atf-quick-start-tests/reference/quick-start-tests-fsm.md).

</td></tr><tr><td>

Field Service – Questionnaire

</td><td>

com.snc.wm\_questionnaire

</td><td>

Create questionnaire for work orders or work order tasks.For more information, see [Activate Field Service Questionnaire](../../field-service-management/task/Activate-fsm-questionnaire.md).

</td></tr><tr><td>

Field Service Management Mobile \(Deprecated\)

</td><td>

com.snc.work\_management\_mThe deprecated plugin is replaced by sn\_fsm\_mobile.

</td><td>

Manages the Field Service classic mobile components. Agents and dispatchers can manage field service tasks using the dispatch map when the device is online and can access read-only tasks when the device is not connected to the Internet. This plugin has been deprecated.For more information, see [Setting up Field Service Mobile Agent](../../field-service-management/concept/setting-up-field-service-mobile-agent.md).

</td></tr><tr><td>

Field Service Map \(Deprecated\)

</td><td>

com.snc.fsm\_mapThe deprecated plugin is replaced by com.snc.uib.fsm\_dispatcher\_workspace.

</td><td>

Field Service Map to view Agents, Tasks and Agent Routes.For more information, see [Additional plugins for Field Service Management](../../field-service-management/reference/field-service-additional-plugins.md).

</td></tr><tr><td>

Central Dispatch \(Deprecated\)

</td><td>

com.snc.central\_dispatchThe deprecated plugin is replaced by sn\_fsm\_disp\_wrkspc.

</td><td>

Allows visually allocating tasks to agents for a logged in dispatcher. Installs the core Service Management items used to allow other service-related plugins to work, such as Field Service Management and Facilities Service Management.For more information, see [Activate Dispatcher Workspace](../../field-service-management/task/activate-dispatcher_workspace.md).

</td></tr><tr><td>

Time Recording Core

</td><td>

com.snc.wm\_time\_recording

</td><td>

Enables time card and time recording functions for Customer Service Management and Field Service Management.For more information, see [Activate Time Recording for Field Service](../../field-service-management/task/Activate-time-recording.md).

</td></tr><tr><td>

Time Recording for Field Service

</td><td>

com.snc.time\_recording\_fsm

</td><td>

Extends the functionality of the Time Card Management and Cost Management applications to Field Service Management.

</td></tr><tr><td>

Field Service – Signature Pad

</td><td>

com.snc.wo\_signature\_pad

</td><td>

Captures a customer signature for closed work orders. Creates a PDF of the work order that includes a summary of the completed work and the name and signature of the customer.For more information, see [Signed PDF summaries for closed work orders](../../field-service-management/concept/work-order-sign-and-confirm-pdf.md#).

</td></tr><tr><td>

Blackout and Maintenance Scheduling

</td><td>

com.snc.blackout\_maintenance\_scheduling

</td><td>

Setup and configuration of blackout and maintenance schedules.

</td></tr><tr><td>

Dynamic Scheduling

</td><td>

com.snc.dynamic\_scheduling

</td><td>

Enables dynamic scheduling for Service Management applications and provides support for bulk task recommendations and interval-based auto assignment.For more information, see [Activate dynamic scheduling](../../field-service-management/task/activate-dynamic-scheduling-plugin.md).

</td></tr><tr><td>

Field Service Management CMS Portal

</td><td>

com.snc.work\_management.cms

</td><td>

Enables you to launch Field Service Management and other Service Management applications from a single CMS page. This plugin is being deprecated.

</td></tr><tr><td>

Field Service Management Geolocation Demo Data

</td><td>

com.snc.work\_management\_geolocation.demo

</td><td>

Enables geolocation capabilities for the Field Service Management application.

</td></tr></tbody>
</table>For more information, see [Additional plugins for Field Service Management](../../field-service-management/reference/field-service-additional-plugins.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated Admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/zurich-platform-administration/page/administer/plugins/task/find-components.html).


**Related topics**  


[Components installed with Field Service Management](../reference/r_InstalledWithFSM.md)

[Additional plugins for Field Service Management](../../field-service-management/reference/field-service-additional-plugins.md)

