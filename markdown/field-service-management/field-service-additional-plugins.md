---
title: Additional plugins for Field Service Management
description: After Field Service Management is activated, you can activate additional plugins that provide demo data and enable a variety of features.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Activate, Configure, Field Service Management]
---

# Additional plugins for Field Service Management

After Field Service Management is activated, you can activate additional plugins that provide demo data and enable a variety of features.

You must have the admin role to activate these additional plugins. For details, see [Activate a plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_ActivateAPlugin.md).

<table id="table_wp2_h15_2v"><thead><tr><th>

Plugin Name

</th><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Customer Service with Field Service Management

</td><td>

com.snc.csm\_fsm\_integration

</td><td>

This plugin provides an integration between the Customer Service Management and Field Service Management applications. Customers and consumers can view case-related work orders from the Customer Service and Consumer Service Portals. In the Field Service Management application, users can view account and contact information on work orders and work order tasks.

</td></tr><tr><td>

Performance Analytics - Content Pack - Field Service Management

</td><td>

com.snc.work\_management\_pa

</td><td>

Enables Performance Analytics for Field Service Management. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details. **Note:** If you have Performance Analytics installed, the Field Service Management Performance Analytics plugin \(com.snc.work\_management\_pa\) is automatically activated as part of the Field Service Management plugin.

</td></tr><tr><td>

Field Service with Project Management

</td><td>

com.snc.wm\_ppm

</td><td>

Field Services Integration with Project Management. This plugin activates the Project Management application and may require additional licenses.

</td></tr><tr><td>

Field Service with Project Management Demo Data

</td><td>

com.snc.wm\_ppm\_demo

</td><td>

Demo plugin for the Field Services Integration with Project Management.

</td></tr><tr><td>

Field Service with Service Locations

</td><td>

com.snc.fsm\_service\_locations

</td><td>

Enables users to create a new service location from the WO/WOT whenever the preferred location does not exist among the stored locations.

</td></tr><tr><td>

Field Service Management - Customer Experience

</td><td>

com.snc.fsm\_customer\_experience

</td><td>

Enables customers to receive SMS notification to know the status of their work order tasks and also track the location of agents when they start to travel to the customer location.

</td></tr><tr><td>

Field Service - Contractor Management

</td><td>

com.snc.fsm\_contractor\_management

</td><td>

Enables the contractor management portal to support the third-party workforce operations. This plugin activates Field Service Management and Service Contractor Base plugins.

</td></tr><tr><td>

Predictive Intelligence for Field Service Management

</td><td>

com.snc.fsm\_ml

</td><td>

Enables customers to leverage machine learning algorithms for availing its various capabilities. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td></tr><tr><td>

Field Service Capacity and Reservations Management

</td><td>

com.snc.fsm\_capacity\_management

</td><td>

Provides capabilities to manage task capacity for groups and field agents. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td></tr><tr><td>

sn-fsm-components

</td><td>

com.sn\_fsm\_components

</td><td>

Repository to store the FSM Custom Components to be used in the UIB Central Dispatch page

</td></tr><tr><td>

Field Service Management Configurable Dispatcher Workspace

</td><td>

com.snc.uib.fsm\_dispatcher\_workspace

</td><td>

Provides the FSM components and pages to support dispatcher flows on CSM Configurable Workspace.

</td></tr><tr><td>

Field Service Management Configurable Workspace

</td><td>

com.snc.uib.fsm\_agent\_workspace

</td><td>

Provides the FSM components, lists, and forms to support FSM on CSM Configurable Workspace.

</td></tr><tr><td>

Field Service Virtual Agent Conversations

</td><td>

com.sn\_fsm.virtualagent

</td><td>

Enables Field Service agents to get quick answers to their work-related queries by interacting with a Virtual Agent through the Now Agent mobile application

</td></tr><tr><td>

Field Service Management Virtual Conferencing Integration

</td><td>

com.snc.fsm\_vci

</td><td>

Enables Field Service agents to provide timely support to customers while away from their office or desktop computer.

</td></tr><tr><td>

Field Service Management Access Hours Management

</td><td>

com.snc.fsm\_access\_hours

</td><td>

Enables Field Service administrators to schedule work order tasks based on the access hours defined in the task.

</td></tr><tr><td>

Field Service Multi-Day Task Scheduling

</td><td>

com.snc.fsm\_multiday\_tasks

</td><td>

Enables Field Service Management dispatchers to assign work order tasks spanning across multiple schedule entries to agents or crews within their defined working hours if they are available throughout the task duration.

</td></tr><tr><td>

Field Service Management Intelligent Task Recommendations

</td><td>

com.snc.fsm\_task\_recommendations

</td><td>

Improves agent utilization by recommending tasks to fill agent schedules.

</td></tr><tr><td>

Field Service Crew Operations

</td><td>

com.snc.fsm\_crew\_scheduling

</td><td>

Enables organizations to assign the same set of resources repeatedly to different tasks.

</td></tr><tr><td>

Field Service Territory Planning

</td><td>

com.snc.fsm\_territory\_planning

</td><td>

Filters the best matched territories for a work order or task for better scheduling of work order or work order task.

</td></tr><tr><td>

Field Service Advanced Parts Sourcing

</td><td>

com.snc.fsm\_advanced\_parts\_sourcing

</td><td>

Enables Field Service agents to request and source multiple parts. Agents can receive mobile notifications when part requests are raised by their peers. **Note:** This plugin installs several system components such as tables, business rules, and scripts. For more information, see [Advanced Part Sourcing components](advanced-part-souring-components.md).

</td></tr><tr><td>

Template Management for Field Service Management

</td><td>

com.snc.fsm\_template\_management

</td><td>

Enables the advanced configurations for work order templates to dynamically fetch information for work orders and create tasks independently for work orders.

</td></tr><tr><td>

Customer Service Install Base Management

</td><td>

com.snc.install\_base

</td><td>

Enables customer service agents to easily trace issues back to the right product or instances of that product. Associates upstream entities such as interactions and cases with downstream entities such as work order or work order task.

</td></tr><tr><td>

Process Mining Content Pack for FSM

</td><td>

com.snc.fsm\_process\_optimization

</td><td>

Process Mining for Field Service Management creates business process flows from the work order task data in audit trails, allowing process owners to perform in-depth analysis and discover process insights to improve business outcomes.

</td></tr><tr><td>

Agent Schedule

</td><td>

com.snc.agent\_schedule

</td><td>

Enables customer service agents and field service technicians to see work schedules and assignments and also add personal events such as meetings or appointments.

</td></tr><tr><td>

Appointment Booking

</td><td>

com.snc.appointment\_booking

</td><td>

Enables setup and configuration for the appointment booking feature.

</td></tr><tr><td>

Assignment Workbench

</td><td>

com.snc.assignment\_workbench

</td><td>

Use workbench to assign work to individual agents easily so that work gets done efficiently and effectively.

</td></tr><tr><td>

Service Management Core

</td><td>

com.snc.service\_management.core

</td><td>

Adds the core Service Management items that enable other service-related plugins to work, such as Field Service Management, Facilities Service Management, and the custom-app creator.

</td></tr><tr><td>

Special Handling Notes

</td><td>

com.sn\_shn

</td><td>

Enables users to quickly view important information about records.

</td></tr></tbody>
</table>**Related topics**  


[Components installed with additional plugins for Field Service Management](components-inst-additional-plugin.md)

