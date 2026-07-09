---
title: Field Service Management glossary
description: Learn about terms and concepts that are unique to Field Service Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/glossary-fsm.html
release: australia
topic_type: concept
last_updated: "2026-06-12"
reading_time_minutes: 8
breadcrumb: [Reference, Field Service Management]
---

# Field Service Management glossary

Learn about terms and concepts that are unique to Field Service Management.

Glossary terms are listed alphabetically.

**Parent Topic:**[Field Service Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/fsm-reference.md)

## access hours

The specific days and times when a customer location or asset is available for service. Access hours can be configured by account, location, or asset, and are automatically populated on the work order task.

## agent efficiency

A metric representing the pace at which a field service agent completes a work order task. It can be used as a factor in scheduling decisions.

## AI agent

An AI-powered assistant that uses skills, context, and rules to decide what actions to take and how to follow through, such as triggering workflows, creating or updating records, and coordinating multiple steps to achieve a goal. AI agents can be deployed out-of-box or built using AI Agent Studio.

## AI agent skill

A generative AI capability that performs a single task well, such as summarizing text, extracting data, classifying intent, or answering questions. Skills are invoked by a user or workflow and can be pre-built or custom-built using the Now Assist Skill Kit.

## appointment booking

A customer-facing feature that lets customers or agents book service appointments by selecting from available time windows, with the option to display optimal slots.

## Capacity Console

A centralized dashboard for monitoring, managing, and optimizing resource capacities across territories and demand channels in real time.

## capacity definition

A record defining how capacity is calculated, allocated, and reserved for a specific group or territory and task type, specifying the source, such as agent schedules or hours, and frequency, such as daily or weekly.

## capacity definition

A record defining how capacity is calculated, allocated, and reserved for a specific group or territory and task type, specifying the source, such as agent schedules or hours, and frequency, such as daily or weekly.

## capacity management

A method for planning and controlling work across a territory or group, measured in hours or task counts. It reserves portions of capacity for specific tasks to prevent overload and prioritize urgent needs.

## contractor management

A set of features for onboarding and managing external, third-party contractor companies and their agents to perform field service work.

## customer experience

A set of features focused on providing customers with transparency and timely updates about their service requests, including notifications and agent location tracking.

## customer service portal

A self-service web portal where customers can submit requests, view work order status, track agent locations, and provide feedback or signatures after work orders are completed.

## Dispatcher Workspace

A configurable, centralized interface where dispatchers manage all scheduling and dispatching activities, including tasks, agent schedules, calendars, and maps.

## domain separation

A platform feature that logically partitions data, processes, and UI for different entities, such as tenants or business units, within a single ServiceNow instance.

## dynamic scheduling

An automated scheduling method that assigns incoming tasks to the most suitable agent based on configurable criteria such as skills, availability, and location, while letting dispatchers handle exceptions and changes.

## equipment scheduling

The process of managing and scheduling physical equipment, such as a bucket truck or specialized diagnostic tool, as a resource with its own availability and skill requirements. Applicable with crews only. Also known as resource scheduling.

## extension points

Specific points in the Field Service Management application code where developers can insert custom logic to modify or extend standard behavior without altering the core application.

## Field Service crew operations

A feature for managing teams of agents \(crews\) and equipment that work together on complex tasks requiring multiple resources. It supports predefined Planned Crews assigned to recurring crew-based work and temporary Ad Hoc Crews assembled for a specific task.

## Field Service marketplace

A feature that lets dispatchers manually or automatically push tasks to a marketplace where onboarded contractors can view and bid on the work, supporting the outsourcing of non-critical tasks.

## FSM reporting and analytics

A suite of preconfigured dashboards and reporting tools that provide data visualizations to monitor and analyze service performance, including KPIs on work volume, SLA compliance, and agent utilization.

## integration

The capability of Field Service Management to connect with other ServiceNow applications, such as Customer Service Management \(CSM\), IT Service Management \(ITSM\), and Project Portfolio Management \(PPM\), so that a record such as a CSM case can be translated into a work order without manual data re-entry.

## intelligent task recommendation

A feature that suggests suitable tasks to dispatchers or agents to fill identified gaps in an agent's schedule, maximizing utilization.

## inventory management

The process of tracking and managing all physical parts and supplies, including their transfer between locations, consumption on tasks, and stock level adjustments.

## linear asset management

A specialized feature for managing work on assets that have a physical length or dimension, such as roads, railways, or pipelines, allowing work orders to be associated with specific segments of the asset.

## Now Assist for Field Service Management \(FSM\)

A suite of generative AI features that improves productivity by automating tasks such as creating work orders and generating work order summaries, closure notes, and knowledge articles.

## Now Mobile Agent

The ServiceNow mobile application that serves as the primary interface for field service agents and contractors to manage their work.

## offline mode

A capability of the Now Mobile Agent app that lets technicians continue working, updating tasks, and recording data without an internet connection. Data syncs automatically once connectivity is restored.

## part requirement

A record created on a work order task that specifies a part needed to complete the work, triggering the sourcing and logistics process.

## planned work management

An application for creating and managing recurring work activities that occur at regular intervals, such as maintenance, inspections, or audits.

## playbooks for Field Service Management

A feature that provides step-by-step, guided workflows within the mobile app to help agents complete complex or critical tasks correctly and consistently.

## predictive intelligence

A feature that uses machine learning to analyze historical data and provide recommendations, such as identifying clusters of similar work orders or suggesting required parts.

## quality management

A feature that enables a designated Reviewer to review and audit soft-closed work order tasks before they are officially closed, ensuring that all the necessary data is captured accurately.

## questionnaire

A configurable set of questions attached to a work order task to gather information or verify compliance, such as completing a safety checklist before starting work or an inspection form before closing a task. There are two types of questionnaires- survey-based and Smart Assessment questionnaires.

## route optimization

A feature that calculates and suggests the most efficient travel route for a single agent's set of assigned tasks for the day, reordering tasks to reduce travel time.

## schedule optimization

An automated process that creates the most efficient schedules by applying defined policies and scheduling attributes to assign tasks and minimize travel time. Optimization can be performed in batches, such as at the start of the day, intraday to rebalance schedules, or on demand.

## Service Level Agreement \(SLA\)

A contractual agreement defining the expected timelines for responding to and resolving a work order or task. Field Service Management tracks performance against these SLAs.

## skills

Attributes assigned to agents, crews, or equipment that define their capabilities, such as HVAC Certified or Crane Operator. They are a primary criterion for matching tasks to resources.

## stockroom

A physical or virtual location used to store and manage inventory. Types include Personal \(an agent's vehicle\), Warehouse, PUDO \(Pick Up Drop Off\), and FSL \(Forward Shipping Location\).

## task bundling

A feature that groups multiple small, short-duration tasks in the same location into a single unit, which scheduling engines treat as one optimized stop. It reduces administrative overhead and travel time for high-volume tasks in dense areas.

## territory

A defined service area to which resources such as agents, contractors, or crews are assigned. Territories can be mapped using attributes, such as postal codes.

## territory planning

A feature that lets organizations define service areas or territories and assign resources to them, helping manage and optimize resource allocation. It provides the first constraint for scheduling engines by limiting tasks to agents who service that area.

## transfer order

A record used to manage the movement of parts from one stockroom to another, such as from a central warehouse to an agent's personal stockroom.

## virtual agent for Field Service Management

A conversational chatbot, accessible through the mobile app, that lets agents get quick answers and perform actions using natural language.

## work configurations

A feature that allows customization of process configurations for different types of field service work, which can then be applied to work order templates or dynamic scheduling.

## work order

A record that stores information about requested work, including customer details, location, and associated assets. It serves as the primary container for one or more work order tasks and must contain at least one work order task.

## work order sign and confirm PDF

A feature that enables a customer digitally sign a completed work order. A PDF summary of the work — including tasks, parts, expenses, time required, and the customer's signature is generated and attached to the record.

## work order states

The sequential statuses a work order progresses through during its lifecycle, such as Draft, Awaiting Qualification, Assigned, Work in Progress, and Closed Complete.

## work order task

A specific, actionable item that must be completed as part of a larger work order, containing details such as required skills, parts, and dependencies.

## work order task states

The sequential statuses a work order task progresses through, such as Pending Dispatch, Scheduled, Accepted, Work in Progress, and Closed Complete.

## work order template

A reusable template that automatically populates a new work order with predefined information, including a short description, tasks, required parts, and necessary skills.

## work plan

A flexible plan that defines how and when recurring work should be performed for a given activity, based on criteria such as product model, location, or asset.

## work schedule

A component of a work plan that dictates the specific timing of maintenance, such as how often and on what days the work is performed.

## work type

A classification that categorizes the kind of work to be performed for a task, such as install, break-fix, or planned maintenance. It can be used to pre-configure task requirements, such as needing a crew or a specific assignment group.

## workforce optimization for Field Service Management

A comprehensive application for managing workforce productivity, including team scheduling, performance monitoring \(KPIs\), and automated coaching and training.

