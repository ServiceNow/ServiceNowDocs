---
title: Create an action to remove a user
description: Create an action to deactivate or delete a user account in the SaaS application.
locale: en-US
release: yokohama
product: SaaS License Management
classification: saas-license-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [SaaS License Connections, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Create an action to remove a user

Create an action to deactivate or delete a user account in the SaaS application.

## Before you begin

If you're using an existing ServiceNow® Integration Hub spoke, find out if it has an action to remove a user that you can use instead of creating one.

Role required: flow\_designer or admin

## About this task

This action is used to reclaim unused subscriptions to reduce your company's software expenses.

## Procedure

1.  Navigate to **All** &gt; **Flow Designer** &gt; **Designer**.

2.  Click **New** and then select **Action**.

3.  On the form, fill in the fields.

    |Field|Value|
    |-----|-----|
    |Name|Name of your choice. For example, **Remove User**.|
    |Accessible From|**All application scopes**.|
    |Category|Leave this field empty.|
    |Protection|**None**.|
    |Application|Spoke app to integrate with the SaaS application. This can be an existing Integration Hub spoke or a new spoke that you created.|
    |In-Flow Annotation|Leave this field empty.|
    |Description|Description of your choice.|

4.  Click **Submit**.

5.  In the Inputs section of the Action Outline, click **Create Input**.

6.  Add a user ID input.

    This is how the action gets the user ID of the user to delete.

    |Label|Name|Type|Mandatory|
    |-----|----|----|---------|
    |User ID|userID|String|Yes|

7.  If the API that you're working with requires user authentication for requests, add inputs for authentication.

    Examples of common user authentication inputs are admin user id and site name. See the documentation for your chosen API to learn about the requirements for user authentication in your specific case. If the API requires an access token, a *Credential Value* variable is automatically created later so you don't need to add it as an input.

    When you use your completed action in a subflow, you define what values to pass as these inputs.

8.  Add a **SOAP step** or **REST step** to the action outline.

    Your choice will depend on the API for the SaaS application that you're integrating with.

9.  If you selected **SOAP**, fill in the form as shown.

<table id="table_o2c_w4j_rjb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td colspan="2">

Connection Details

</td></tr><tr><td>

Connection

</td><td>

**Use Connection Alias**.

</td></tr><tr><td>

Connection Alias

</td><td>

Connection alias that you created when you created the integration profile. If you have not yet created an integration profile, follow the steps to [create a custom integration profile with a connection alias.](create-integration-custom.md)

</td></tr><tr><td>

Endpoint

</td><td>

This value is automatically populated when you select the connection alias. It's set to the Connection URL from the HTTP\(s\) Connection record linked to the alias.

</td></tr><tr><td colspan="2">

Request Details

</td></tr><tr><td>

Build Envelope

</td><td>

**Manually**.

</td></tr><tr><td>

SOAP Action

</td><td>

API request to delete or deactivate a user. See the documentation for your chosen API to select the appropriate request.

</td></tr><tr><td>

SOAP Envelope

</td><td>

XML request message to delete a user. See the documentation for your chosen API to learn how to write an XML request message. In general, the header should have your input variables for user authentication as well as the *Credential Value* variable as the access token. The body should include the request to delete a user and the user ID input. **Note:** For an example of a SOAP envelope, see the Remove User action used in the Webex Reclaim Subscription subflow.

</td></tr></tbody>
</table>10. If you selected **REST,** fill in the form as shown.

    |Field|Value|
    |-----|-----|
    |Connection Details|
    |Connection|**Use Connection Alias**.|
    |Connection Alias|Connection alias that you created when you created the integration profile. If you have not yet created an integration profile, follow the steps to [create a custom integration profile with a connection alias.](create-integration-custom.md)|
    |Base URL|This value is automatically populated when you select the connection alias. It's set to the Connection URL from the HTTP\(s\) Connection record linked to the alias.|
    |Request Details|
    |Build Request|**Manually**.|
    |Resource Path|Path to the resource. This value gets appended to the Base URL. See the documentation for the API that you're working with to learn how to construct the resource path.|
    |HTTP Method|**DELETE**.|
    |Query Parameters|Add a parameter for user ID. Set the value as the user ID input.|

11. Add a **Script step** to the Action Outline for error handling.

    1.  For **Required Runtime**, select **Instance**.

    2.  Create input variables.

        |Name|Value|
        |----|-----|
        |response|Response Body output from the SOAP or REST step|
        |status\_code|Status Code output from the SOAP or REST step|

    3.  Create output variables.

        |Label|Name|Type|Mandatory|
        |-----|----|----|---------|
        |status|status|Choice|Yes|
        |error\_message|error\_message|String|Yes|

    4.  In the **Script** field, write a script to assign values to the status and error message outputs.

        -   Use the **status\_code** input to check if there is an error. Set the status output equal to **Error** if there is an error and **Success** if there is no error.
        -   In cases where there is an error, use the **response** input to get information about the kind of error. Set the **error message** output to a description of the error so that a user can understand what went wrong.
12. In the Action Outline, click **Outputs**.

13. Create output variables.

    |Label|Name|Type|Mandatory|
    |-----|----|----|---------|
    |Status|status|Choice|No|
    |Error message|error\_message|String|No|

14. Assign values to the output variables.

    |Label|Value|
    |-----|-----|
    |Status|**status** output variable from the script step|
    |Error message|**error\_message** output variable from the script step|

15. To test your action, click **Test**.

    1.  View the test results and system logs for details about any errors.

        To view system logs, navigate to **System Logs** &gt; **System Log** &gt; **All**.

    2.  If your action has errors, make sure that you're using the correct endpoints and that the API request is structured as expected.

    **Note:** When testing, remember that this action deactivates a user. Test this action in a sub-production environment. If only a production environment is available, you can create fake users for testing.

16. After verifying that the action is working as expected, click **Publish**.


