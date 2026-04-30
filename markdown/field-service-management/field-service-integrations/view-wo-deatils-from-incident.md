---
title: View work order details from the incident record using the CSM Configurable Workspace
description: View or track the progress of work order in the associated incident record from CSM Configurable Workspace.
locale: en-US
release: zurich
product: Field Service Integrations
classification: field-service-integrations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integration with Incident Management, Integrating Field Service Management with other applications, Configure, Field Service Management]
---

# View work order details from the incident record using the CSM Configurable Workspace

View or track the progress of work order in the associated incident record from CSM Configurable Workspace.

## Before you begin

Enable the activity function using the IncidentWorkOrderIntegration extension point. For more information, see [Using extension point for incident management](../reference/using-extension-point-for-incident-mngmnt.md).

Role required: itil, wm\_admin, and sn\_change\_read

## About this task

ITIL agents can view the progress of a work order directly from a related incident record. The incident record tracking is updated whenever the following updates are made to the work order or related work order tasks:

-   Work notes added to the task
-   State of the task updated

## Procedure

1.  Log in to CSM Configurable Workspace.

2.  Click the **List** icon \(![List icon](../../../administer/workspace/image/list-icon-black.png)\).

3.  In the Lists panel, navigate to **Incident** &gt; **All**

4.  Open a incident record for which you want to track the progress.

5.  Click the Details related list.

6.  View the work order progress in the **Activity** section.


**Parent Topic:**[Integration with Incident Management](../concept/incident-for-fsm.md)

