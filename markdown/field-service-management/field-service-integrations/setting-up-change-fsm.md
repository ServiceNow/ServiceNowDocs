---
title: Setting up Change Management for Field Service
description: Install and set up the Change Management for Field Service application to track work order progress directly in the change request.
locale: en-US
release: yokohama
product: Field Service Integrations
classification: field-service-integrations
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Integration with Change Management, Integrating Field Service Management with other applications, Configuring Field Service Management, Field Service Management]
---

# Setting up Change Management for Field Service

Install and set up the Change Management for Field Service application to track work order progress directly in the change request.

Integration with the Change Management application enables ITIL agents to create a work order from change request. After the qualification of this work order, the related work order tasks are created for dispatcher to assign these tasks to the field service agents. Any work note to the task or update the state of the task added by an agent is reflected in the related work order and can be tracked directly from the associated change request.

This integration provides the following benefits for ITIL agents:

-   Ability to create a work order from a change request either on the ServiceNow AI Platform or the CSM Configurable Workspace.
    -   For information on creating a work order from a change request in ServiceNow AI Platform, see [Create a work order](../../planning-and-policy/task/t_CreateAWorkOrder.md).
    -   For information about creating a work order from a change request in CSM Configurable Workspace, see [Create a work order from a change request in the CSM Configurable Workspace](../task/create-wo-from-chng-config-wrkspc.md).
-   Enables the ITIL agent to track the progress of a work order directly from its parent change request.

This integration automates your system to provide the following benefits:

-   Auto-fills some work order fields with relevant information from the change request.
-   Synchronizes work order task schedule start and end dates with the change schedule planned start and end dates.
-   Enables field service agents to view the related change request details and related lists in the Mobile Agent application.
-   Auto-close a change request when all related work orders are closed as completed.

    **Note:** You must enable the auto-close function in the extension point of a ChangeWorkOrderIntegration script to close the change request automatically when the related work order is closed. For more information, see [Using an extension point to synchronize work orders with change requests](../reference/using-extention-point-for-chnge-mngmnt.md).


## Synchronizing data between the work order and the change request

Work notes are synchronized from a related work order to the change request when:

-   The work order task state is updated
-   Work notes are added to the work order tasks
-   The work order task is closed either as complete or incomplete

