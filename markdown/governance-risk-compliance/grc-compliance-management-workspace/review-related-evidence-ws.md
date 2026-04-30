---
title: Review related evidence using the Compliance Workspace
description: The Evidence Request feature includes a related list called Related Evidence that is not visible by default.
locale: en-US
release: xanadu
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Manage evidence requests using the Compliance Workspace, Using the Compliance Workspace, Performing compliance tasks in Compliance Workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Review related evidence using the Compliance Workspace

The Evidence Request feature includes a related list called Related Evidence that is not visible by default.

## Before you begin

Role required: admin

## About this task

This related list provides a list of evidence that is not directly requested for the current record, but is associated to a related record. For example, the Related Evidence list on the Control Objective form shows evidence requested for associated controls.

The Related Evidence related list is available to a wide variety of forms throughout the Evidence Request feature; however, it is not visible in the base system. You can personalize any of the forms in which it is available, but keep in mind that activating this related list can impact system performance.

|Table name|Type of related evidence displayed|
|----------|----------------------------------|
|Authority document|Evidence request tasks created on the citations mapped to this authority document.|
|Citation|Evidence request tasks created on the control objective associated to the citation.|
|Control|Evidence request tasks created on the control test mapped to the control and Issues created for the control.|
|Control objective|Evidence request tasks created on the controls associated to the control objective.|
|Control test|Evidence request tasks created on the controls associated to the control test.|
|Engagement|Evidence request tasks created on the entities, controls, control tests, audit tasks, control test issues, and issues mapped to the engagement are displayed.|
|Entity|Evidence request tasks created on the controls associated to the entity, Issues created on the entity.|
|Policy|Evidence request tasks created on the control objective associated to the policy.|

## Procedure

1.  Navigate to the form for which you want to display the **Evidence Request** related list.

2.  Right-click in the form header, and click **Configure** &gt; **Related Lists**.

3.  Locate the **Related Evidence** item in the **Available** box and move it to the **Selected** box.

4.  Click **Save**.


