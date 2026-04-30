---
title: Customer Service Spoke
description: Provides actions for flow designers to use when creating Customer Service Management business processes. Requires the Customer Service Management \[com.sn\_customerservice\] plugin.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Spokes, Workflow Studio flow integrations, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Customer Service Spoke

Provides actions for flow designers to use when creating Customer Service Management business processes. Requires the Customer Service Management \[com.sn\_customerservice\] plugin.

|Action|Description|
|------|-----------|
|Get Case|Retrieve a case record using the case number. If multiple records are found, only the first record is returned.|
|Create Case|Create a case using one or more attributes. This action mimics the structure of the Case table \(sn\_customerservice\_case\) and exposes the fields present on the Case table. |
|Create Quick Case|Create a case using the customer, description, channel, priority, and category attributes.|
|Create Task on Case|Create a case task and optionally associate it with a case.|
|Update Case|Update a case by providing the case reference and the fields that you want to update. |
|Assign Case|Assign a case using matching rules. To use this action, you must first define the matching rules that match cases with resources \(assignment groups, agents\).|
|Escalate Case|Request case escalation. This action does not automatically approve escalation. Approval is based on the selected escalation template.|
|Escalate Account|Request account escalation. This action does not automatically approve escalation. Approval is based on the selected escalation template. |
|Add Work Note to Task|Add a work note to a task or to task extended objects \(for example, a case or case task\).|
|Add Comment to Task|Add a comment to a task or to task extended objects \(for example, a case or case task\).|

**Parent Topic:**[Spokes](../concept/spokes.md)

