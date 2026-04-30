---
title: Associate Record to Email action
description: Associate a record with an Email \[sys\_email\] record so that you can track which record is affected by the email.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Workflow Studio actions, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Associate Record to Email action

Associate a record with an Email \[sys\_email\] record so that you can track which record is affected by the email.

## Roles and availability

Available as a Workflow Studio ServiceNow core action. Users with the flow\_designer or admin role can add an action to a flow and define configuration details.

## Fields

|Field|Description|
|-----|-----------|
|Email Record|Email \[sys\_email\] record that the Target Record associates with.|
|Target Record|Record to associate to the email record|

## Output

This action updates the **Target** field on the Email \[sys\_email\] record.

## Example

In the following example, a process owner adds the Associate Record to Email action under an inbound email trigger. The user has also added a Create Catalog Task action in the flow. In the **Email Record** field, the user selects to associate a record to the email that triggered the flow. In the **Target Record** field, the user selects to associate the Catalog Task \[sc\_task\] record that is created in the Create Catalog Task action.

![Using the Associate to Email action](../images/associate-to-email-example.png "Using the Associate to Email action")

**Parent Topic:**[Workflow Studio actions](../concept/flow-actions.md)

