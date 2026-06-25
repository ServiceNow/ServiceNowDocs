---
title: Reopen an incident in Service Operations Workspace
description: Reopen a resolved incident from the incident record in Service Operations Workspace \(SOW\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/service-operations-workspace/reopen-incident-sow.html
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Incident Management in Service Operations Workspace, Operating IT services in your organization, Service Operations Workspace for ITSM, IT Service Management]
---

# Reopen an incident in Service Operations Workspace

Reopen a resolved incident from the incident record in Service Operations Workspace \(SOW\).

## Before you begin

An incident must be created and set to **Resolved** state. For more information, see [Create an incident in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/create-incident-sow.md).

Role required: itil or sn\_incident\_write

## About this task

An agent with incident write \(sn\_incident\_write\) access can view and use the **Reopen** option on the incident record page in SOW to reopen any incident that is assigned to them or other agents. However, on the Portal UI’s such as Service Portal and Employee Service Center \(ESC\) portal, an agent can only view and use the **Reopen** option to reopen an incident if they are the caller or **Opened by** \(Requester\) end user for that incident.

Both the caller and the **Opened by** \(Requester\) users can view and use the **Reopen incident** option on the Portal UIs, such as Service Portal and Employee Service Center \(ESC\) portal to reopen a resolved incident.

If an incident state is set to **Closed**, the incident cannot be reopened. However, if you request to reopen the incident by replying to the resolution notification email, a new incident is opened with selected field values that are copied from the closed incident. For more information on reopening an incident, see [Reopening an incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/incident-management/reopening-incident.md).

## Procedure

1.  Open an incident with **Resolved** state.

2.  Select **Reopen**.

    A dialog-box opens.

3.  Enter **Additional comments \(Customer visible\)**.

4.  Select **Reopen**.


## Result

A success notification message pop-up appears on the banner. The incident record state is set to **In progress**.

**Parent Topic:**[Incident Management in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/incident-sow.md)

**Related topics**  


[Create an incident in Service Operations Workspace]()

[View and update incident information on the Overview tab in SOW]()

[Viewing incident record information using the Contextual side panel]()

[Work on an incident list page in Service Operations Workspace]()

[Work on an incident record in Service Operations Workspace]()

[Remedial actions using Playbook]()

[Close resolved incident]()

[Incident Management in Service Operations Workspace reference]()

