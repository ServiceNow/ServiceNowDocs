---
title: Adding Declarative Actions on the Standard Record Page
description: Adding declarative actions on the Incident page and the tabs inside the incident record page using the Standard Record Page \(SRP\) in the Service Operations Workspace.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Standard Record Page in Service Operations Workspace, Configuring record pages in Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM to improve your experience, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Adding Declarative Actions on the Standard Record Page

Adding declarative actions on the Incident page and the tabs inside the incident record page using the Standard Record Page \(SRP\) in the Service Operations Workspace.

## Before you begin

Role required: admin

## About this task

Declarative actions help you to modify the list actions, related list actions, and field decorators available in the Service Operations Workspace. For more information about creating declarative actions and how to use them, see Declarative actions.

Along with the declarative actions customizations, the SRP or Standard Record Page also modifies the add-on events in the Incident records and the tabs inside the records.

## Procedure

1.  Navigate to **All** &gt; **sys\_ux\_addon\_event\_mapping.list**.

2.  From the UX Add-on Event Mappings list, go to the required event mapping.

    You can add two types of declarative actions mappings.

    -   Declarative action mappings without using the parent macroponent. This option uses the controllers for the mappings.
    -   Declarative action mapping using the source element ID and the parent macroponent. This option doesn’t use the controllers.
    For example, to modify the form declarative action to create a change, go to the **Form Create Change task** for which the **Parent Macroponent** is empty. Similarly, you can add the declarative action for inline tabs inside an incident. For example, to add a declarative action to add a change request to the Related Records list, go to **SOW Related list Add Change Request** for which the **Parent Macroponent** is empty.

    **Note:** To add declarative action to page collection tabs such as Overview, add Handled events in the UI Builder. Map this event to the event in the UX Add-on Event Mappings list using the Source element ID.

3.  Add the following information to modify the action.

    |Field|Description|
    |-----|-----------|
    |Source Component|The component emits the source event. For example, the Action bar.|
    |Source Declarative Action|Declarative actions used as the source event|
    |Controller|A controller that handles the target event. For example, Form.|
    |Target Event|Handled event that the mapping in **Target Payload mapping** targets|
    |Target Payload Mapping|The binding of the container and the type of the event|


**Parent Topic:**[Configuring Standard Record Page in Service Operations Workspace](../concept/srp-service-operations-workspace.md)

