---
title: Configure dashboard deletion actions in the Workflow Studio
description: Using the Workflow Studio, you can add actions to the dashboard deletion process. Actions may include sending an email to the dashboard's users or generating an approval request.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Delete a dashboard, Working with in-line dashboards, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Configure dashboard deletion actions in the Workflow Studio

Using the Workflow Studio, you can add actions to the dashboard deletion process. Actions may include sending an email to the dashboard's users or generating an approval request.

## Before you begin

Prior to invoking the flow, the instance checks that the dashboard exists and that the initiating user has the correct role.

Role required: You can delete any dashboard that you created. Users with the admin role can delete all dashboards. Administrators can grant and deny access to the Workflow Studio based on user roles. For more information, see [User access to Flow Designer](https://www.servicenow.com/docs/access?context=user-access-flow-designer&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**

2.  Select **Subflows**.

3.  Select the **Delete Dashboard** subflow.

4.  Select **Add an Action, Flow Logic, or Subflow**.

    For more information about the available possibilities, see [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

5.  Use the handle next to the action number to reorder the action.

    ![Flow designer action with the reorder handle highlighted](../image/flow-designer-handle.png)

6.  Test the flow with the actions that you added.

    For more information, see [Test a flow](https://www.servicenow.com/docs/access?context=flow-test&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

7.  Save the flow.


## Result

There are three possible outputs:

-   **Successful deletion**

    Output code 1. Indicates that the deletion process was successful.

-   **Failed to delete**

    Output code 2. Indicates that the deletion failed.

-   **Deletion has been initiated**

    Output code 3. Indicates that the deletion process has started, but that intermediate steps such as an approval are not complete.


For more information, see [Action error evaluation](https://www.servicenow.com/docs/access?context=action-error-evaluation&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

**Parent Topic:**[Delete a Platform Analytics dashboard](delete-db-in-ac.md)

