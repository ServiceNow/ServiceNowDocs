---
title: Tutorial: add a new change management state
description: This tutorial provides an example of adding a new state to the existing state model.
locale: en-US
release: xanadu
product: Change Management
classification: change-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Reference section for Change Management, Change Management, IT Service Management]
---

# Tutorial: add a new change management state

This tutorial provides an example of adding a new state to the existing state model.

## Before you begin

Role required: script\_include\_admin, ui\_policy\_admin, ui\_action\_admin, or admin

## About this task

Consider the following scenario:

Based on your organization's requirements, you must add a new state, **Complete**, between the existing **Implement** and **Review** states. You must also add the ability to decide if the **Review** state is needed.

Perform the following steps:

## Procedure

1.  Open the **Change Request** form.


1.  [Create a new choice](t_CreateNewChoice.md)  
Create a new choice for the change request state.
2.  [Create a custom field](t_CreateCustomField.md)  
Create a custom choice field to indicate whether a change request must go through the **Review** state.
3.  [Add a UI policy](t_AddUIPolicy.md)  
Add a UI policy to display the **Needs review** field for **Normal** change requests when it reaches the **Complete** state.
4.  [Create an ACL](t_CreateNewACL.md)  
Create an access control rule \(ACL\) to prevent the **Needs review** field from being modified after it has been set.
5.  [Update the state handler script include](t_UpdateStateHandlerScriptInclude.md)  
Update the ChangeRequestStateHandler script include with the new **Complete** state.
6.  [Update the state model script include](t_UpdateStateModelScriptInclude.md)  
Update the ChangeRequestStateModel\_normal script include to add new functions for the **Complete** state.
7.  [Create a UI action](t_CreateNewUIAction.md)  
Create a UI action to display a button on a change request for the **Complete** state.
8.  [Create a process flow record](t_CreateNewProcessFlowRecord.md)  
Create and add a process flow record for the **Complete** state. The process flow formatter displays at the top of the Change Request form.
9.  [Update the change request workflow](t_UpdateWorkflow.md)  
Update the change request workflow to reflect the addition of the **Complete** state.

**Parent Topic:**[Reference section for Change Management](../concept/reference-change-management.md)

