---
title: ITSM spoke
description: Provides flow and actions associated with ITSM. Requires the ITSM application suite.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Spokes, Flow integrations, Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# ITSM spoke

Provides flow and actions associated with ITSM. Requires the ITSM application suite.

|Action|Description|
|------|-----------|
|Add Comment|Adds a comment to a task record.|
|Add Worknote|Adds a work note to a task record.|
|Apply Change Approval Policy|Controls the approval process for a change request by creating user and group approvals according to a change approval policy record. Multiple actions can be used in a flow, where each action references the same or different Change Approval Policies.|
|Assign Incident to CI Support Group|Updates an incident record to assign it to the CI Support Group.|
|Cancel Change Tasks from Flow|Cancels all related pending and open change tasks that are created from Flow.|
|Check Change for User Approval|Checks if the specified user has already approved the change request.|
|Create Catalog Task on Request|Creates a Catalog Task record from a Request record.|
|Create Catalog Task on Request Item|Creates a Catalog Task record from a Request Item record.|
|Create Change Task on Change Request|Creates a Change Task record from a Change Request record.|
|Create Emergency Change Request|Creates a Change Request record of type Emergency.|
|Create Emergency Request from Incident|Creates a Change Request record of type Emergency from an Incident record.|
|Create Incident|Creates an Incident record.|
|Create Incident Task on Incident|Creates an Incident Task record from an Incident record.|
|Create Normal Change Request from Incident|Creates a Change Request record of type Normal from an Incident record.|
|Create Outage|Creates a cmdb\_ci outage record for a configuration item. The **Task** field is populated only if the source is a task record. If the source is non-task record such as an alert record, the **Task** field is empty.|
|Create Problem from Incident|Creates a Problem record from an Incident record.|
|Create Request|Creates a Request record.|
|Create Standard Change Request|Creates a Change Request record of type Standard. For more information, see [IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/r_ITServiceManagement.md).|
|Create Task|Creates a child task record for a Task table record. For example, creates an Incident Task record for an Incident record.|
|Create Task Outage Relationship|Creates a Task Outage Relationship record where cmdb\_ci outage record and task record are inputs to the action.|
|Create Standard Change Request from Incident|Creates a Change Request record of type Standard from an Incident record.|
|Disregard Change Approvals|Sets all related pending approvals to no longer required.|
|Update Assignee|Updates the Assigned to field of a Task table record.|
|Update Assignment Group|Updates the Assignment Group field of a Task table record.|

## Data mappings

Users with the admin, flow\_designer, or action\_designer roles can open and view the steps of ITSM Spoke actions. To view data mappings between ITSM data types, view the Create Record step of the ITSM Spoke action. Most ITSM Spoke data is stored in extensions of the Task \[task\] table, which means that many of the data types share common fields.

![Field values used to create an Change Request from an Incident record](../images/example-itsm-spoke-create-change-from-incident.png "Create Record step for the Create Normal Change Request from Incident action")

For example, the Create Normal Change Request from Incident action uses the common Task table fields for Short description, Configuration Item, Priority, Domain, Company, and Description to create a Change Request from an Incident.

**Parent Topic:**[Spokes](../concept/spokes.md)

