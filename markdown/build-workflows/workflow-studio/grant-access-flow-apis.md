---
title: Create a client callable flow, subflow, or action
description: Enable a client script to trigger a flow, subflow, or action.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [API access to Workflow Studio flows, Configuring flows, Configuring Workflow Studio, Workflow Studio, Build workflows]
---

# Create a client callable flow, subflow, or action

Enable a client script to trigger a flow, subflow, or action.

## Before you begin

-   Role required: security\_admin
-   Consider the implications of making a flow, subflow, or action client callable, such as whether it exposes protected data or bypasses validation logic.

## About this task

By default, the flows, subflows, and actions can only be called by the FlowAPI within a server script. Flow and action designers can make individual flows, subflows, or actions available to client calls by enabling the **Client callable** option during the design process.

## Procedure

1.  Elevate privileges to security\_admin.

2.  Navigate to **System Security** &gt; **Access Control \(ACL\)**.

3.  Click **New**.

4.  Create an access control.

    |Field|Description|
    |-----|-----------|
    |Type|client\_callable\_flow\_object|
    |Operation|execute|
    |Admin overrides|Selected|
    |Name|Enter a name for the ACL.|
    |Requires role|Create a role to provide access to the APIs. For example, create a flow\_api\_access role.|

5.  Assign the role to the user you would like to grant access to.

6.  Enable a client script to trigger the flow, subflow, or action.

    1.  Open the flow, subflow, or action you want to make client callable.

    2.  In the **More Actions** menu, select **Manage security**.

    3.  Select **Callable by Client API**.

    4.  Add the access control record created earlier to the **ACLs** field.

    5.  Click **Update**.


## Result

The user with the designated permissions can trigger a client callable flow, subflow, or action from a client script using the GlideFlow API.

**Parent Topic:**[API access to Workflow Studio flows](../concept/api-access-flow-designer.md)

