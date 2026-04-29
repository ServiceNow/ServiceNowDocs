---
title: Setting up Incident Management for Field Service
description: Install and set up the Incident Management for Field Service application to track work order progress.
locale: en-US
release: australia
product: Field Service Integrations
classification: field-service-integrations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integration with Incident Management, Integrating Field Service Management with other applications, Configure, Field Service Management]
---

# Setting up Incident Management for Field Service

Install and set up the Incident Management for Field Service application to track work order progress.

Integration with the Incident Management application enables ITIL agents to create a work order from incident record. After the qualification of this work order, the related work order tasks are created so that dispatcher can assign these tasks to the field service agents. Any work note to the task or update the state of the task added by an agent is reflected in the related work order and can be tracked directly from the associated incident record.

This integration provides the following benefits for ITIL agents:

-   Ability to create a work order from a incident request either on the ServiceNow AI Platform or the CSM Configurable Workspace.
    -   For information about creating a work order from an incident record in ServiceNow AI Platform, see [Create a work order](../../planning-and-policy/task/t_CreateAWorkOrder.md).
    -   For more information about creating a work order from incident record in CSM Configurable Workspace, see [Create a work order from a change request in the CSM Configurable Workspace](../task/create-wo-from-chng-config-wrkspc.md).
-   Enables the ITIL agent to track the progress of a work order directly from its parent incident record.

This integration automates your system to provides the following benefits:

-   Auto-fills some work order fields with relevant information from the incident record.
-   Synchronizes work order task schedule start and end dates with the incident record planned start and end dates.
-   Enables field service agents to view the related incident record details and related lists in the Mobile Agent application.
-   Auto-close a change request when all related work orders are closed as completed.

    **Note:** You must enable the auto-close function in the extension point of a IncidentWorkOrderIntegration script to close the Incident record automatically when the related work order is closed. For more information, see [Using an extension point to synchronize work orders with change requests](../reference/using-extention-point-for-chnge-mngmnt.md).


## Synchronizing data between the work order and the incident record

Work notes are synchronized from work order to the incident record when:

-   The work order task state is updated.
-   Work notes are added to the work order tasks.
-   The work order task is closed either as complete or incomplete.

-   **[Using extension point for incident management](../reference/using-extension-point-for-incident-mngmnt.md)**  
Extension points enable you to extend the functionality of an application and integrate customizations without altering the application code. Extension points are stored in the Extension Point \[sys\_extension\_point\] table.

**Parent Topic:**[Integration with Incident Management](incident-for-fsm.md)

