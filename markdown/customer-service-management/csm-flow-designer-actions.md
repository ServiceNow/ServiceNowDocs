---
title: Customer Service Management Workflow Studio actions
description: Use Workflow Studio actions as building blocks to create Customer Service Management business processes.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Administer Customer Service Management, Customer Service Management]
---

# Customer Service Management Workflow Studio actions

Use Workflow Studio actions as building blocks to create Customer Service Management business processes.

|Action|Description|
|------|-----------|
|Get Case|Retrieve a case record using the case number. If multiple records are found, only the first record is returned.|
|Create Case|Create a case using one or more attributes. This action mimics the structure of the Case table \(sn\_customerservice\_case\) and exposes all of the fields present on the Case table.|
|Create Quick Case|Create a case using the customer, description, channel, priority, and category attributes.|
|Create Task on Case|Create a case task and optionally associate it with a case.|
|Update Case|Update a case by providing the case reference and the fields that you want to update.|
|Assign Case|Assign a case using matching rules. To use this action, you must first define the matching rules that match cases with resources \(assignment groups, agents\).|
|Escalate Case|Request case escalation. This action does not automatically approve escalation. Approval is based on the selected escalation template.|
|Escalate Account|Request account escalation. This action does not automatically approve escalation. Approval is based on the selected escalation template.|
|Add Work Note to Task|Add a work note to a task or to task extended objects \(for example, a case or case task\).|
|Add Comment to Task|Add a comment to a task or to task extended objects \(for example, a case or case task\).|

**Related topics**  


[Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)

[Action Designer](https://www.servicenow.com/docs/access?context=actions&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)

