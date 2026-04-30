---
title: Create a subflow to reclaim a user
description: Create a subflow to reclaim a user subscription.
locale: en-US
release: zurich
product: SaaS License Management
classification: saas-license-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [SaaS License Connections, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Create a subflow to reclaim a user

Create a subflow to reclaim a user subscription.

## Before you begin

This subflow requires an action to remove a user. For more information, see [Create an action to remove a user](create-data-stream-remove-user.md).

Role required: flow\_designer or admin

## About this task

**Note:** For examples of subflows to reclaim a user, see the Jira Reclaim Subscription and Webex Reclaim Subscription subflows.

## Procedure

1.  Navigate to **All** &gt; **Flow Designer** &gt; **Designer**.

2.  Click **New** and then select **Subflow**.

3.  On the form, fill in the fields.

<table id="table_dk4_brb_njb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of your choice. For example, *Application* Reclaim Subscription, where *Application* is the name of the SaaS application you are integrating with.

</td></tr><tr><td>

Application

</td><td>

**Software Asset Management - SaaS License Management Integrations**.**Note:** If you save the subflow in the Software Asset Management - SaaS License Management Integrations application, it's included with your Software Asset Management subscription. If you save the subflow in any other application, you may be charged for ServiceNow® Integration Hub transactions. If you're publishing your custom spoke application on the ServiceNow Store, select your custom app instead.

</td></tr><tr><td>

Accessible From

</td><td>

**All application scopes**.

</td></tr><tr><td>

Category

</td><td>

Leave this field empty.

</td></tr><tr><td>

Protection

</td><td>

**None**.

</td></tr><tr><td>

In-Flow Annotation

</td><td>

Leave this field empty.

</td></tr><tr><td>

Description

</td><td>

Description of your choice.

</td></tr><tr><td>

Run As

</td><td>

**User who initiates session**.

</td></tr></tbody>
</table>4.  Add an integration profile input and a user subscription input.

    |Label|Name|Type|Mandatory|
    |-----|----|----|---------|
    |Integration profile|integration\_profile|Reference.Integration Profile|Yes|
    |User subscription|user\_subscription|Reference.Software Subscription|Yes|

5.  Add an error message output and a status output.

    |Label|Name|Type|
    |-----|----|----|
    |Error message|error\_message|String|
    |Status|status|String|

6.  In the Actions section, click the plus icon and then click **Action** to add a new action.

7.  In the list of installed spokes, select the spoke for the SaaS application that you're integrating with.

    **Note:** To add additional spokes to your list of installed spokes, request them on the [ServiceNow Store](https://store.servicenow.com). For a complete list of available spokes, see [IntegrationHub available spokes](https://www.servicenow.com/docs/access?context=spokes-list&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US). If there's no existing spoke for the SaaS application that you want to integrate with, you can [create a new spoke](create-saas-spoke.md).

8.  To remove a user, select an action.

    1.  Define the value to pass as the **User ID** input.

        The value that you use depends on the API that you're working with, but it will generally be the **External user ID** or **User principal name** field from the **User subscription** input for this subflow.

    2.  Define the values to pass for any user authentication inputs for the action.

9.  To check if the Remove User action returns an error, add an If flow logic.

10. Add a child flow logic to assign subflow outputs.

    |Name|Data|
    |----|----|
    |Error message|Error message output from the Remove User action|
    |Status|failure|

11. Add an Else flow logic at the same level as the If logic for cases when the Remove User action doesn't return an error.

12. Add a child flow logic to assign subflow outputs.

    |Name|Data|
    |----|----|
    |Status|success|

    The following image shows a completed example of a subflow to reclaim a user subscription. The example shown is the Webex Reclaim Subscription subflow.

    ![Example subflow to reclaim a user subscription](../image/slc-remove-user-flow.png)

13. To test your subflow, click **Test**.

    1.  View the test results and system logs for details about any errors.

        To view system logs, navigate to **System Logs** &gt; **System Log** &gt; **All**.

    **Note:** When testing, remember that this subflow deactivates a user. Test this subflow in a sub-production environment. If only a production environment is available, you can create fake users for testing.

14. After verifying that the subflow is working as expected, click **Publish**.

    **Tip:** You can still edit the subflow after it's published.


