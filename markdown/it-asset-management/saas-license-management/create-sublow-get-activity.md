---
title: Create a subflow to get user activity
description: Create a subflow to update the Software Subscription table with each user's most recent activity in the SaaS application.
locale: en-US
release: zurich
product: SaaS License Management
classification: saas-license-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [SaaS License Connections, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Create a subflow to get user activity

Create a subflow to update the Software Subscription table with each user's most recent activity in the SaaS application.

## Before you begin

This subflow requires a data stream action to get user activity. For more information, see [Create a data stream action to get user activity](create-data-stream-get-activity.md).

Role required: flow\_designer or admin

## About this task

**Note:** For examples of subflows to get user activity, see the Jira Update User Activity and Webex Update User Activity subflows.

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

Name of your choice. For example, *Application* Update User Activity, where *Application* is the name of the SaaS application you’re integrating with.

</td></tr><tr><td>

Application

</td><td>

**Software Asset Management - SaaS License Management** **Note:** If you save the subflow in the Software Asset Management - SaaS License Management application, it’s included with your Software Asset Management subscription. If you save the subflow in any other application, you may be charged for ServiceNow® Integration Hub transactions. If you’re publishing your custom spoke application on the ServiceNow Store, select your custom app instead.

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
</table>4.  Click **Submit**.

5.  Add an integration profile input and a look back time input.

    |Label|Name|Type|Mandatory|
    |-----|----|----|---------|
    |Integration profile|integration\_profile|Reference.Integration Profile|Yes|
    |Look back time|look\_back\_time|Date/Time|Yes|

6.  In the Actions section, click the plus icon and then click **Action** to add a new action.

7.  Select the spoke for the SaaS application that you want to integrate with from the list of installed spokes.

    **Note:** To add additional spokes to your list of installed spokes, request them on the [ServiceNow Store](https://store.servicenow.com). For a complete list of available spokes, see [IntegrationHub available spokes](https://www.servicenow.com/docs/access?context=spokes-list&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US). If there’s no existing spoke for the SaaS application that you want to integrate with, you can [create a new spoke](create-saas-spoke.md).

8.  Select a data stream action to get user activity.

9.  Add the **Look back time** subflow input as the value to pass to the **Look back time** input for the data stream action.

10. Define the values to pass for any user authentication inputs for the data stream action.

11. Add the **Update User Activity If Later Using User** action from the Software Asset Management spoke as a child of the get user activity data stream action.

12. Use values from the Data panel to complete the action.

    |Field|Value|
    |-----|-----|
    |Last activity|Date of most recent activity from the targetObject.|
    |Integration profile|Integration profile input that you created for the subflow.|
    |External user id|User id or account id from the user targetObject. This id is generally a numeric and non human-readable value. This value must be unique.|
    |User principal name|Email address from the user targetObject. If an email address isn’t available, use another value such as user name plus user id. This value should be human readable.|

13. If you want to use more than one data stream action to get multiple types of user activity, repeat steps 6 through 12 to add each data stream action to the subflow.

14. Click **Test** to test your subflow.

    1.  View the test results and system logs for details about any errors.

        To view system logs, navigate to **System Logs** &gt; **System Log** &gt; **All**.

15. After verifying that the subflow is working as expected, click **Publish**.

    **Tip:** You can still edit the subflow after it's published.


