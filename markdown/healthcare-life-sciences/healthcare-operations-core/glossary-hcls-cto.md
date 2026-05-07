---
title: Healthcare and Life Sciences Operations glossary
description: Learn about the terms and concepts that are unique to Healthcare and Life Sciences Operations.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.
locale: en-US
release: australia
product: Healthcare Operations Core
classification: healthcare-operations-core
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 20
keywords: [glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms]
breadcrumb: [Reference, Healthcare Operations Core, Healthcare Operations, Healthcare and Life Sciences]
---

# Healthcare and Life Sciences Operations glossary

Learn about the terms and concepts that are unique to Healthcare and Life Sciences Operations.

## A

Glossary terms are grouped alphabetically.

### Asset Tag Scanning

A Care Team Mobile feature that allows care team members to scan QR codes or barcodes on medical equipment to retrieve the asset record, view its history and status, and create associated support requests.

For example, a nurse scans the barcode on an infusion pump using Care Team Mobile and sees its maintenance history before submitting a new repair request.

To learn how to scan asset tags, see [Asset Scan in Care Team Mobile](../concept/cto-mobile-asset-scan.md).

### Assignment Group

A group of users associated with a healthcare organization that determines which agents are responsible for fulfilling cases or work orders for that organization. Multiple assignment groups can be linked to a single organization.

For example, the Biomed Dispatcher assignment group is associated with the Biomed Support organization so that device repair work orders are routed to the correct agents.

To learn how to associate assignment groups, see:

-   [Associate assignment groups with a healthcare organization in Healthcare Operations Core](../task/hco-assign-roles-responsibilities-members.md)
-   [Set up assignment groups for Care Team Operations for Biomed](../task/cto-biomed-set-up-assignment-groups.md)
-   [Set up assignment groups for Care Team Operations for Environmental Services](../task/cto-evs-assignment-groups.md)
-   [Set up assignment groups for Care Team Operations for Facilities](../task/cto-facilities-assignment-groups.md)
-   [Create assignment groups for Care Team Work Management](../task/ctwm-create-assignment-groups.md)
-   [Set up assignment groups for Care Team Operations for Healthcare IT](../task/cto-it-assignment-groups.md)

## B

Glossary terms are grouped alphabetically.

### Business Location

A service organization record that is automatically created when a healthcare organization is created. A bidirectional reference exists between the healthcare organization and its business location, linking the HCLS data model to CSM service management structures.

For example, when the "Cardiology Department" healthcare organization is created, an associated internal business location with the same name is auto-generated.

To learn more about business locations, see [Setting up healthcare locations and healthcare organizations](../concept/understanding-healthcare-locations-and-healthcare-organizations.md).

## C

Glossary terms are grouped alphabetically.

### Care Team Manager

A user role that inherits all Care Team Member permissions and additionally allows the user to add or remove members within their healthcare organizations. Role name: sn\_hco.care\_team\_manager

For example, a unit manager uses the Care Team Portal to add a newly hired nurse to the ICU team and assign them the Team Member responsibility.

To learn more about Care Team Manager and other responsibilities, see [Setting up roles and responsibilities for Healthcare Operations users](../concept/cto-setting-up-roles-responsibilities.md).

### Care Team Member

A user role \(sn\_hco.care\_team\_member\) that grants access to create and view Healthcare Operations cases. Members must also be associated with a healthcare organization and assigned responsibilities to access specific records.

For example, a registered nurse is added to the HCO Team Members group and then associated with the Cardiology Unit organization as a Care Team Member.

To learn more about this role, related responsibilities, and access scoping, see [Setting up roles and responsibilities for Healthcare Operations users](../concept/cto-setting-up-roles-responsibilities.md).

### Care Team Mobile

A mobile application that extends Healthcare Operations Core to smartphones and tablets, allowing care team members to create and track support requests, scan asset tags, and browse healthcare locations while on the move.

For example, a nurse assistant uses Care Team Mobile to scan a barcode on an IV pump, view its service history, and submit a repair request from the bedside.

To learn more about Care Team Mobile, see [Exploring Care Team Mobile](../concept/care-team-mobile-exploring.md).

### Care Team Operations for Biomed

A plugin \(sn\_cto\_biomed\) that extends Healthcare Operations Core with case types for reporting medical device issues and other biomedical engineering service requests. Cases generate work orders when Field Service Management is installed.

For example, a nurse reports a malfunctioning infusion pump using the "Report a medical device issue" catalog item, which creates a Biomed case and dispatches a work order.

To learn more about Care Team Operation for Biomed, see [Exploring Care Team Operations for Biomed](../concept/exploring-cto-biomed.md) and [Configuring Care Team Operations for Biomed](../concept/configuring-cto-biomed.md).

### Care Team Operations for Environmental Services

A plugin \(sn\_cto\_evs\) that extends Healthcare Operations Core with case types for reporting environmental services issues such as housekeeping, waste management, linen services, and hazardous material handling.

For example, a care team member requests a terminal room cleaning after a patient discharge by selecting Create a request &gt; Request environmental service &gt; Terminal Cleaning Request.

To learn more about Care Team Operations for Environmental Services, see [Exploring Care Team Operations for Environmental Services](../concept/cto-evs-exploring.md)and [Configuring Care Team Operations for Environmental Services](../concept/cto-evs-configuring.md).

### Care Team Operations for Facilities

A plugin \(sn\_cto\_facilities\) that extends Healthcare Operations Core with case types for reporting facilities issues such as HVAC problems, plumbing leaks, electrical faults, and safety hazards. Includes a preconfigured service catalog of common facilities requests.

For example, a nurse reports a temperature issue by selecting Create a request &gt; Request Facilities service &gt; Temperature and Humidity Control and setting the category to "Room Climate Issues."

To learn more about Care Team Operations for Facilities, see [Exploring Care Team Operations for Facilities](../concept/cto-facilities-exploring.md) and [Configuring Care Team Operations for Facilities](../concept/cto-facilities-configuring.md).

### Care Team Operations for Healthcare IT

A plugin \(sn\_cto\_hcit\) that extends Healthcare Operations Core with case types for reporting and fulfilling IT issues, including EMR problems and other technology requests. IT cases generate incidents for ITIL fulfillers.

For example, a unit secretary reports a printer malfunction by navigating to Create a request &gt; Request IT service &gt; Request other IT service in the Care Team Portal.

To learn more about Care Team Operations for Healthcare IT, see [Care Team Operations for Healthcare IT](../concept/hcls-cto-it-app.md).

### Care Team Portal

A responsive web portal within Healthcare Operations Core where care team members create support requests for ancillary departments, track request statuses, manage team membership, and view knowledge articles. It can run standalone or be embedded in EMR systems such as Epic Hyperspace.

For example, a nurse navigates to https:// .service-now.com/careteam to submit a request for a linen change in a patient room.

To learn more about Care Team Portal, see [Care Team Portal](../concept/hcls-cto-care-team-portal.md) and [Navigate the Care Team Portal](../concept/hcls-cto-using-portal.md).

### Care Team Work Management

An application that streamlines task creation, assignment, and tracking for care team internal operations using task plan templates. Care team cases and tasks are generated from predefined work plans submitted through the Care Team Portal.

For example, a unit manager creates a "Shift Readiness" task plan template that generates a care team case with individual safety check tasks for each nurse at shift change.

To learn more about Care Team Work Management, see [Exploring Care Team Work Management](../concept/ctwm-exploring.md) and [Configuring Care Team Work Management](../concept/ctwm-configuring.md).

### Common Location

A record in the cmn\_location table that provides the foundational location data across the ServiceNow platform. Healthcare locations extend common locations to add healthcare-specific attributes like altitude and physical type.

For example, an administrator sets up a common location for "Building A" and then creates a healthcare location that references it and adds the physical type "Building."

To learn more about Common Locations, see [Setting up healthcare locations and healthcare organizations](../concept/understanding-healthcare-locations-and-healthcare-organizations.md).

### CSM/FSM Configurable Workspace

The ServiceNow workspace used by department agents and support staff to view, manage, and fulfill Healthcare Operations cases and work orders. It provides configurable views, related records, and action menus for case resolution.

For example, a Facilities support agent opens the CSM/FSM Configurable Workspace to accept, update, and close a plumbing repair work order dispatched from a Healthcare Facilities case.

## D

Glossary terms are grouped alphabetically.

### Decision Builder

A ServiceNow tool used to modify state decision tables that map the state transitions between Healthcare Operations cases and their associated work orders or incidents. It controls how state changes in one record propagate to the linked record.

For example, for example, an administrator uses Decision Builder to configure that when a work order state changes to "Closed Complete," the associated Healthcare Biomed case state updates to "Closed."

To learn more about Decision Builder, see [Modify state decision tables in Care Team Operations for Biomed](../concept/cto-biomed-modify-states.md).

### Department Agent

A user who creates, views, edits, and fulfills service requests on behalf of a hospital’s ancillary department such as IT, Biomed, Facilities, or Environmental Services. Agents are assigned the location support agent role specific to their department.

For example, a Biomed agent with the sn\_cto\_biomed.loc\_support\_agent role receives and fulfills a medical device repair work order in the CSM/FSM Configurable Workspace.

To learn more about Department Agent, see [Exploring Healthcare Operations Core](../concept/hcls-cto-exploring.md).

### Domain Separation

A ServiceNow platform feature that separates data at runtime across multiple tenants, including user interface elements, cache keys, reporting, and aggregations. In Healthcare Operations, it ensures that healthcare requests and fulfillment tasks are isolated to the correct customer domain.

For example, a service provider managing IT for two hospital systems uses domain separation so Hospital A’s cases are invisible to Hospital B’s care team.

## E

Glossary terms are grouped alphabetically.

### Epic Hyperspace via Hyperdrive

An integration method for embedding the Care Team Portal within the Epic Hyperspace EMR interface using Hyperdrive technology. This allows clinicians to access ServiceNow’s Care Team Portal without leaving the EMR, with support for tokenized data capture from Epic launch contexts.

For example, a nurse opens a patient chart in Epic Hyperspace, and the Care Team Portal loads in an embedded frame with the workstation ID and patient context automatically populated.

To learn more about Epic Hyperspace via Hyperdrive, see [Embedding Care Team Portal in Epic Hyperspace via Hyperdrive](../concept/configure-care-team-portal.md).

## F

Glossary terms are grouped alphabetically.

### Field Service Management Plugin

The ServiceNow plugin \(com.snc.work\_management\) required for automatic work order creation from Healthcare Operations cases. Without it, agents fulfill cases directly rather than through synchronized work orders.

For example, after installing the Field Service Management plugin, Healthcare Biomed cases automatically generate work orders with qualifier, dispatcher, and agent fulfillment workflows.

## H

Glossary terms are grouped alphabetically.

### Healthcare Location

A record in the sn\_hcls\_location table representing a physical or virtual place where care and operational work occurs, such as a campus, building, wing, unit, room, or bed. Locations are organized hierarchically and associated with healthcare organizations.

For example, an IT agent identifies a broken monitor in PICU Room 204 because the healthcare location hierarchy shows Campus → Hospital Building → Pediatrics Wing → PICU → Room 204.

To learn more about Healthcare Location, see [Setting up healthcare locations and healthcare organizations](../concept/understanding-healthcare-locations-and-healthcare-organizations.md).

### Healthcare Operations Case

An abstract, extendable case record \(table: sn\_hco\_case\) that stores healthcare operations-related requests. It serves as the base from which specific case types such as Healthcare IT, Biomed, Facilities, and EVS cases are extended.

For example, an administrator creates a child table from sn\_hco\_case to build a custom case type for pharmacy supply requests.

To learn more about Healthcare Operations Case, see [Healthcare Operations Case overview](../concept/hcls-cto-hco-case.md).

### Healthcare Operations Core

The foundational ServiceNow application that enables hospitals to streamline and automate operational processes. It provides the framework for care teams to report and track issues related to day-to-day operations through integrated service departments such as IT, Biomed, Facilities, and Environmental Services.

For example, a hospital installs Healthcare Operations Core to give nurses a single portal for reporting broken equipment, IT outages, and facility issues instead of using disconnected systems.

To learn more about Healthcare Operations Core, see [Exploring Healthcare Operations Core](../concept/hcls-cto-exploring.md).

### Healthcare Organization

A record in the sn\_hcls\_organization table that defines an entity within a healthcare delivery network, such as a hospital, department, or organizational team. Organizations are arranged in parent-child hierarchies that control visibility, responsibility, and case routing.

For example, a hierarchy is configured as: HQ → City Hospital → Nursing Department → ICU Unit, where each level is a healthcare organization.

To learn more about Healthcare Organization, see [Setting up healthcare locations and healthcare organizations](../concept/understanding-healthcare-locations-and-healthcare-organizations.md).

### Healthcare Organization Location Association

A table \(sn\_hcls\_organization\_location\_association\) that links healthcare organizations to healthcare locations, determining which organization is responsible for a particular location and limiting the locations shown to care team members when they report issues.

For example, the ICU unit organization is associated with rooms 301–310 so that ICU nurses only see those rooms when creating a request.

To learn more about Healthcare Organization Location Association, see [Setting up healthcare locations and healthcare organizations](../concept/understanding-healthcare-locations-and-healthcare-organizations.md).

## I

Glossary terms are grouped alphabetically.

### Incident Auto-creation

A feature of Care Team Operations for Healthcare IT where an ITSM incident is automatically generated from a Healthcare IT case, carrying over all case information for IT agents to fulfill using standard incident management.

For example, a nurse reports an EMR login failure through the Care Team Portal, and an incident is automatically created in the IT department’s Service Operations workspace.

To learn more about Incident Auto-creation, see [Healthcare IT case overview](../concept/hcl-cto-it-case.md).

## R

Glossary terms are grouped alphabetically.

### Record Producer

A service catalog item configured to create a specific type of record, such as a Healthcare Biomed case or Healthcare IT case. Record producers define the form fields, variable sets, and catalog client scripts that appear when a care team member submits a request.

For example, the "Report a Medical Device Issue" record producer creates an sn\_cto\_biomed\_case record and includes fields for asset tag, location, urgency, and description.

To learn more about Record Producer, see the following:

-   [Add custom record producers to the service catalog in Care Team Operations for Biomed](../task/cto-biomed-add-record-producers.md)
-   [Add custom record producers to the service catalog in Care Team Operations for Environmental Services](../task/cto-evs-add-custom-record-producers.md)
-   [Add custom record producers to the service catalog in Care Team Operations for Facilities](../task/cto-facilities-add-customer-record-producer.md)

### Responsibility

A record-level access control that determines which specific records a user can view or edit within tables they already have role access to. Responsibilities in Healthcare Operations are based on Service Model Foundation and are assigned through Related Party Configurations.

For example, a nurse with the Care Team Member responsibility can only see cases for the ICU, not cases belonging to the Emergency Department.

To learn more about Responsibilities, see [Setting up roles and responsibilities for Healthcare Operations users](../concept/cto-setting-up-roles-responsibilities.md).

### Role

A permission set that defines table-level access in ServiceNow, determining which objects a user can interact with and what CRUD \(Create, Read, Update, Delete\) actions they can perform within Healthcare Operations applications.

For example, a user assigned the sn\_hco.care\_team\_member role can create and view Healthcare Operations cases.

To learn more about Roles, see [Setting up roles and responsibilities for Healthcare Operations users](../concept/cto-setting-up-roles-responsibilities.md).

## S

Glossary terms are grouped alphabetically.

### Service Model Foundation \(SMF\)

The underlying ServiceNow framework that provides the base responsibility model used by Healthcare Operations. SMF responsibilities like "Service location business contributor" are relabeled for healthcare use through Related Party Configurations.

For example, the Care Team Member responsibility in HCO maps to the "Service location business contributor" responsibility from SMF.

To learn more about Service Model Foundation \(SMF\), see [Setting up roles and responsibilities for Healthcare Operations users](../concept/cto-setting-up-roles-responsibilities.md).

### SMART on FHIR Authentication

A standards-based authentication protocol used to enable single sign-on \(SSO\) for Epic users accessing the Care Team Portal embedded in Epic Hyperspace via Hyperdrive. Configuration requires a FHIR app on fhir.epic.com and an OIDC Identity Provider on the ServiceNow instance.

For example, an Epic user opens the Care Team Portal within Hyperspace and is automatically authenticated through the SMART on FHIR integration without a separate login.

To learn more about SMART on FHIR Authentication, see [Authenticate SMART on FHIR for use with the Care Team Portal in Hyperspace via Hyperdrive](../task/hco-authenticate-portal.md).

### State Synchronization

The mechanism that keeps the status of a Healthcare Operations case aligned with its linked work order or incident throughout the fulfillment lifecycle, including transitions like New, Open, Work in Progress, Resolved, and Closed.

For example, a care team member tracks their request in the Care Team Portal and sees it change from "Open" to "Resolved" in real time as the IT agent resolves the incident.

To learn more about State Synchronization, see the following:

-   [Healthcare EVS case overview](../concept/cto-evs-case-overview.md)
-   [Healthcare Facilities case overview](../concept/cto-facilities-case-overview.md)
-   [Healthcare IT case overview](../concept/hcl-cto-it-case.md)
-   [Healthcare Biomed case overview](../concept/hcls-cto-biomed-case.md)

## T

Glossary terms are grouped alphabetically.

### Task Plan Template

A reusable configuration in Care Team Work Management that defines a set of tasks and records to be automatically created when a care team agent initiates a work plan. Templates are published and cannot be edited once active.

For example, an administrator creates a task plan template called "Unit Safety/Readiness" containing work orders and child tasks for equipment checks, supply verification, and safety guidelines review.

## V

Glossary terms are grouped alphabetically.

### Virtual Agent

ServiceNow’s conversational bot platform, available in the Care Team Portal via a chat window icon. It helps care team members quickly obtain information, make decisions, and perform common work tasks through natural language interaction.

For example, a nurse opens the chat icon in the Care Team Portal and asks Virtual Agent to check the status of a pending IT request.

## W

Glossary terms are grouped alphabetically.

### Work Order

A task record automatically generated from a Healthcare Operations case when the Field Service Management plugin is installed. Work orders are assigned to support agents for fulfillment and remain synchronized with the originating case for state and comment updates.

For example, when a nurse reports a broken bed rail via the Care Team Portal, a work order is automatically created and dispatched to a Facilities agent.

To learn more about Work Order, see

-   [Healthcare EVS case overview](../concept/cto-evs-case-overview.md)
-   [Healthcare Facilities case overview](../concept/cto-facilities-case-overview.md)
-   [Healthcare Biomed case overview](../concept/hcls-cto-biomed-case.md)

### Work Order Synchronization

The automatic bidirectional syncing of state changes, comments, and updates between a Healthcare Operations case and its associated work order, enabled by the Field Service Management plugin.

For example, when a Facilities agent marks a work order as "Work in Progress," the associated Healthcare Facilities case automatically updates to the same state.

